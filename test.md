<table responsive="true" summary="table">
              <tr responsive="true">
                <th scope="col">Topic</th>
                <th scope="col">Description</th>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773561(v=vs.85).aspx"><strong>PathAddBackslash</strong></a></p>
                </td>
                <td data-th="Description">
                  <ul style="list-style-type:none;">                    
                    <li><code>Adds a backslash to the end of a string to create the correct syntax for a path.</code></li>
                    <li><code>If the source path already has a trailing backslash, no backslash will be added.</code></li>
                    <li>將反斜線新增到字串的末尾做為新的路徑，如果原始路徑沒有反斜線則不會新增。</li>
                  </ul>
                  <code>
                  <ol>
                    <li>TCHAR szBackslashNot[_MAX_PATH] = _T("C:\\TEST\\FILE");</li>
                    <li>TCHAR szBackslashYes[_MAX_PATH] = _T("C:\\TEST\\FILE\\");</li>
                    <li>_tprintf(_T("%X = [%s]\r\n"), ::PathAddBackslash(szBackslashNot), szBackslashNot); // C:\TEST\FILE\</li>
                    <li>_tprintf(_T("%X = [%s]\r\n"), ::PathAddBackslash(szBackslashYes), szBackslashYes); // C:\TEST\FILE\</li>
                  </ol>
                  </code>
                  <div class="alert">
                    <strong>Note:</strong>
                    <span>Misuse of this function can lead to a buffer overrun. We recommend the use of the safer</span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707078(v=vs.85).aspx"><strong>PathCchAddBackslash</strong></a>
                    <span>or</span>                    
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707079(v=vs.85).aspx"><strong>PathCchAddBackslashEx</strong></a>                      
                    <span>function in its place.</span></br>          
                    <strong>注意:</strong>
                    <span>此功能濫用可能導致緩衝區溢出，建議使用更安全的 </span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707078(v=vs.85).aspx"><strong>PathCchAddBackslash</strong></a>
                    <span> 或 </span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707079(v=vs.85).aspx"><strong>PathCchAddBackslashEx</strong></a>
                    <span> 的函式。</span>
                   </div>         
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773563(v=vs.85).aspx"><strong>PathAddExtension</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Adds a file name extension to a path string.</code></li>               
                    <li>新增副檔名到路徑結尾。</li>
                  </ol>
                  <code>
                  <ul style="list-style-type:decimal;"> 
                    <li>TCHAR szFilePath[_MAX_PATH] = _T("C:\\TEST\\FILE");</li>
                    <li>TCHAR szExts[_MAX_EXT] = _T(".doc");</li>
                    <li>_tprintf(_T("%d = [%s]\r\n"), ::PathAddExtension(szFilePath, szExts), szFilePath); // C:\TEST\FILE.doc</li>
                  </ul>
                  </code>
                  <div class="alert">
                    <strong>Note:</strong>
                    <span>Misuse of this function can lead to a buffer overrun. We recommend the use of the safer</span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707080(v=vs.85).aspx"><strong>PathCchAddExtension</strong></a>
                    <span>function in its place.</span></br>          
                    <strong>注意:</strong>
                    <span>此功能濫用可能導致緩衝區溢出，建議使用更安全的 </span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707080(v=vs.85).aspx"><strong>PathCchAddExtension</strong></a>
                    <span> 的函式。</span>
                  </div>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773565(v=vs.85).aspx"><strong>PathAppend</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Appends one path to the end of another.</code></li>               
                    <li>附加一個路徑或檔案到路徑結尾。</li>
                  </ol>
                  <code>
                  <ol>
                    <li>TCHAR szFilePath[_MAX_PATH] = _T("C:\\TEST\\FILE");</li>
                    <li>TCHAR szFileName[_MAX_PATH] = _T("Demo.doc");</li>
                    <li>_tprintf(_T("%d = [%s]\r\n"), ::PathAppend(szFilePath, szFileName), szFilePath); // C:\TEST\FILE\Demo.doc</li>
                  </ol>
                  </code>
                  <div class="alert">
                    <strong>Note:</strong>
                    <span>Misuse of this function can lead to a buffer overrun. We recommend the use of the safer</span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707081(v=vs.85).aspx"><strong>PathCchAppend</strong></a>
                    <span>or</span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707082(v=vs.85).aspx"><strong>PathCchAppendEx</strong></a>
                    <span>function in its place.</span></br>
                    <strong>注意:</strong>
                    <span>此功能濫用可能導致緩衝區溢出，建議使用更安全的 </span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707081(v=vs.85).aspx"><strong>PathCchAppend</strong></a>
                    <span> 或 </span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707082(v=vs.85).aspx"><strong>PathCchAppendEx</strong></a>
                    <span> 的函式。</span>
                  </div>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773567(v=vs.85).aspx"><strong>PathBuildRoot</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Creates a root path from a given drive number.</code></li>               
                    <li>根據磁碟編號產生英文路徑，字串長度不得少於 4 個字元。</li>
                  </ol>
                  <code>
                  <ol>
                    <li>TCHAR szFilePath[_MAX_PATH] = {NULL};</li>
                    <li>_tprintf(_T("%d = [%s]\r\n"), ::PathBuildRoot(szFilePath, 2), szFilePath); // C:\</li>
                  </ol>
                  </code>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773569(v=vs.85).aspx"><strong>PathCanonicalize</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Simplifies a path by removing navigation elements such as "." and ".." to produce a direct, well-formed path.</code></li>               
                    <li>刪除路徑中句點符號字元，例如: "." 和 ".." 確保路徑格式正確。</li>
                  </ol>
                  <code>
                  <ol>
                    <li>TCHAR szFilePath[_MAX_PATH] = {NULL};</li>
                    <li>TCHAR szWellPath[_MAX_PATH] = _T("C:\\path\\.\\Ex\\..\\End");</li>
                    <li>_tprintf(_T("%d = [%s]\r\n"), ::PathCanonicalize(szFilePath, szWellPath), szFilePath); // [C:\path\End]</li>
                    <li>TCHAR szWellPath[_MAX_PATH] = _T("C:\\path\\..\\Ex\\.\\End");</li>
                    <li>_tprintf(_T("%d = [%s]\r\n"), ::PathCanonicalize(szFilePath, szWellPath), szFilePath); // [C:\Ex\End]</li>
                    <li>TCHAR szWellPath[_MAX_PATH] = _T("C:\\path\\Ex\\.\\Ext\\..\\End");
                    <li>_tprintf(_T("%d = [%s]\r\n"), ::PathCanonicalize(szFilePath, szWellPath), szFilePath); // [C:\path\Ex\End]</li>
                    <li>TCHAR szWellPath[_MAX_PATH] = _T("C:\\path\\.\\Ex\\.\\Ext\\..\\End\\..");
                    <li>_tprintf(_T("%d = [%s]\r\n"), ::PathCanonicalize(szFilePath, szWellPath), szFilePath); // [C:\path\Ex]</li>                     
                  </ol>
                  </code>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773571(v=vs.85).aspx"><strong>PathCombine</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Concatenates two strings that represent properly formed paths into one path; also concatenates any relative path elements.</code></li>               
                    <li>串聯兩個字串表示格式正確的路徑到一條路徑;此外將任何相對路徑元素連接在一起。</li>
                  </ol>
                  <code> 
                  <ol>
                    <li>TCHAR szFilePath[_MAX_PATH] = {NULL};</li>
                    <li>TCHAR szDriveRoot[_MAX_PATH] = _T("C:");</li>
                    <li>TCHAR szDriveLink[_MAX_PATH] = _T("TEST\\Drive");</li>
                    <li>_tprintf(_T("[%s]\r\n"), ::PathCombine(szFilePath, szDriveRoot, szDriveLink); // [C:\TEST\Drive] </li>
                    <li>// szFilePath = [C:\TEST\Drive]</li>
                  </ol>
                  </code>                  
                  <div class="alert">
                    <strong>Note:</strong>
                    <span>Misuse of this function can lead to a buffer overrun. We recommend the use of the safer</span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707085(v=vs.85).aspx"><strong>PathCchCombine</strong></a>
                    <span> or </span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707086(v=vs.85).aspx"><strong>PathCchCombineEx</strong></a>
                    <span> function in its place.</span></br>          
                    <strong>注意:</strong>
                    <span>此功能濫用可能導致緩衝區溢出，建議使用更安全的 </span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707085(v=vs.85).aspx"><strong>PathCchCombine</strong></a>
                    <span> 或 </span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707086(v=vs.85).aspx"><strong>PathCchCombineEx</strong></a>
                    <span> 的函式。</span>
                  </div>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773574(v=vs.85).aspx"><strong>PathCommonPrefix</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">
                    <li><code>Compares two paths to determine if they share a common prefix.</code></li>
                    <li><code>A prefix is one of these types: "C:\\", ".", "..", "..\\".</code></li>
                    <li>傳回兩個路徑中相同前綴字串。</li>
                    <li>前綴字串需是右列類型："C:\\", ".", "..", "..\\"。</li>                  
                  </ol>
                  <ol>
                    <li>TCHAR szFilePath[_MAX_PATH] = {NULL}</li>
                    <li>TCHAR szDriveRoot[_MAX_PATH] = _T("c:\\win\\tray\\sample.txt");</li>
                    <li>TCHAR szDriveLink[_MAX_PATH] = _T("C:\\win\\desktop\\temp.txt");</li>
                    <li>_tprintf(_T("%d [%s]\r\n"), ::PathCommonPrefix(szDriveRoot, szDriveLink, szFilePath); // 6  szFilePath =[C:\\win] </li>     
                  </ol>
                  </code>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773575(v=vs.85).aspx"><strong>PathCompactPath</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Truncates a file path to fit within a given pixel width by replacing path components with ellipses.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773578(v=vs.85).aspx"><strong>PathCompactPathEx</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Truncates a path to fit within a certain number of characters by replacing path components with ellipses.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773581(v=vs.85).aspx"><strong>PathCreateFromUrl</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Converts a file URL to a Microsoft MS-DOS path.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773583(v=vs.85).aspx"><strong>PathCreateFromUrlAlloc</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Creates a path from a file URL.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773584(v=vs.85).aspx"><strong>PathFileExists</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines whether a path to a file system object such as a file or folder is valid.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773587(v=vs.85).aspx"><strong>PathFindExtension</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Searches a path for an extension.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773589(v=vs.85).aspx"><strong>PathFindFileName</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Searches a path for a file name.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773591(v=vs.85).aspx"><strong>PathFindNextComponent</strong></a></p>
                </td>     
                <td data-th="Description">
                  <ol style="list-style-type:none;">
                    <li><code>Parses a path and returns the portion of that path that follows the first backslash.</code></li>
                    <li>傳回第一個反斜線後面的路徑字串。</li>
                  </ol>
                  <code>
                  <ol>
                     <li>// szFilePath = 字串不該變</li>
                    <li>TCHAR szFilePath[_MAX_PATH] = _T("C:\\TEST\\Drive");</li>
                    <li>_tprintf(_T("[%s]\r\n"), ::PathFindNextComponent(szFilePath); // [TEST\\Drive]</li>                    
                    <li>TCHAR szFilePath[_MAX_PATH] = _T("\\TEST\\Drive");</li>
                    <li>_tprintf(_T("[%s]\r\n"), ::PathFindNextComponent(szFilePath); // [TEST\Drive] </li>     
                    <li>TCHAR szFilePath[_MAX_PATH] = _T("TEST\\Drive");</li>
                    <li>_tprintf(_T("[%s]\r\n"), ::PathFindNextComponent(szFilePath); // [Drive] </li>
                  </ol>
                  </code>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773594(v=vs.85).aspx"><strong>PathFindOnPath</strong></a></p>
                </td>
                <td data-th="Description">    
                  <ol style="list-style-type:none;">
                    <li><code>Searches for a file.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773598(v=vs.85).aspx"><strong>PathFindSuffixArray</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines whether a given file name has one of a list of suffixes.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773602(v=vs.85).aspx"><strong>PathGetArgs</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Finds the command line arguments within a given path.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773608(v=vs.85).aspx"><strong>PathGetCharType</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines the type of character in relation to a path.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773612(v=vs.85).aspx"><strong>PathGetDriveNumber</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Searches a path for a drive letter within the range of 'A' to 'Z' and returns the corresponding drive number.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773617(v=vs.85).aspx"><strong>PathIsContentType</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines if a file's registered content type matches the specified content type.
                    This function obtains the content type for the specified file type and compares
                    that string with the <em>pszContentType</em>. The comparison is not case-sensitive.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773621(v=vs.85).aspx"><strong>PathIsDirectory</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Verifies that a path is a valid directory.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773623(v=vs.85).aspx"><strong>PathIsDirectoryEmpty</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines whether a specified path is an empty directory.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773627(v=vs.85).aspx"><strong>PathIsFileSpec</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Searches a path for any path-delimiting characters (for example, ':' or '\' ).</code></li>
                    <li><code>If there are no path-delimiting characters present, the path is considered to be a File Spec path.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773631(v=vs.85).aspx"><strong>PathIsHTMLFile</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines if a file is an HTML file. The determination is made based on the content type that is registered for the file's extension.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773635(v=vs.85).aspx"><strong>PathIsLFNFileSpec</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines whether a file name is in long format.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773640(v=vs.85).aspx"><strong>PathIsNetworkPath</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines whether a path string represents a network resource.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773650(v=vs.85).aspx"><strong>PathIsPrefix</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Searches a path to determine if it contains a valid prefix of the type passed by
                    <em>pszPrefix</em>. A prefix is one of these types: "C:\\", ".", "..", "..\\".</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773660(v=vs.85).aspx"><strong>PathIsRelative</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Searches a path and determines if it is relative.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773674(v=vs.85).aspx"><strong>PathIsRoot</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines whether a path string refers to the root of a volume.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773687(v=vs.85).aspx"><strong>PathIsSameRoot</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Compares two paths to determine if they have a common root component.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773701(v=vs.85).aspx"><strong>PathIsSystemFolder</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines if an existing folder contains the attributes that make it a system folder.</code></li> 
                    <li><code>Alternately, this function indicates if certain attributes qualify a folder to be a system folder.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773712(v=vs.85).aspx"><strong>PathIsUNC</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773722(v=vs.85).aspx"><strong>PathIsUNCServer</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines if a string is a valid UNC for a server path only.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773723(v=vs.85).aspx"><strong>PathIsUNCServerShare</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines if a string is a valid UNC share path, \\<em>server</em>\<em>share</em>.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773724(v=vs.85).aspx"><strong>PathIsURL</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Tests a given string to determine if it conforms to a valid URL format.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773725(v=vs.85).aspx"><strong>PathMakePretty</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773726(v=vs.85).aspx"><strong>PathMakeSystemFolder</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Gives an existing folder the proper attributes to become a system folder.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773727(v=vs.85).aspx"><strong>PathMatchSpec</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Searches a string using a MS-DOS wildcard match type.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773728(v=vs.85).aspx"><strong>PathMatchSpecEx</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Matches a file name from a path against one or more file name patterns.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773737(v=vs.85).aspx"><strong>PathParseIconLocation</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Parses a file location string that contains a file location and icon index, and returns separate values.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773739(v=vs.85).aspx"><strong>PathQuoteSpaces</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Searches a path for spaces. If spaces are found, the entire path is enclosed in quotation marks.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773740(v=vs.85).aspx"><strong>PathRelativePathTo</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Creates a relative path from one file or folder to another.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773742(v=vs.85).aspx"><strong>PathRemoveArgs</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Removes any arguments from a given path.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773743(v=vs.85).aspx"><strong>PathRemoveBackslash</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Removes the trailing backslash from a given path.</code></li>
                    <li>中譯文</li>
                  </ol>
                  <div class="alert">
                    <strong>Note:</strong>
                    This function is deprecated. We recommend the use of the
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707089(v=vs.85).aspx"><strong>PathCchRemoveBackslash</strong></a>
                    or
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707090(v=vs.85).aspx"><strong>PathCchRemoveBackslashEx</strong></a>
                    function in its place.</div>
                  <div></div>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773745(v=vs.85).aspx"><strong>PathRemoveBlanks</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Removes all leading and trailing spaces from a string.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773746(v=vs.85).aspx"><strong>PathRemoveExtension</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Removes the file name extension from a path, if one is present.</code></li>
                    <li>中譯文</li>
                  </ol>
                  <div class="alert">
                    <strong>Note:</strong>
                    This function is deprecated. We recommend the use of the
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707091(v=vs.85).aspx"><strong>PathCchRemoveExtension</strong></a>
                    in its place.</div>
                  <div></div>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773748(v=vs.85).aspx"><strong>PathRemoveFileSpec</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Removes the trailing file name and backslash from a path, if they are present.</code></li>
                    <li>中譯文</li>
                  </ol>
                  <div class="alert">
                    <strong>Note:</strong>
                    This function is deprecated. We recommend the use of the
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707092(v=vs.85).aspx"><strong>PathCchRemoveFileSpec</strong></a>
                    function in its place.</div>
                  <div></div>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773749(v=vs.85).aspx"><strong>PathRenameExtension</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Replaces the extension of a file name with a new extension. If the file name does not contain an extension, the extension will be attached to the end of the string.</code></li>
                    <li>中譯文</li>
                  </ol>
                  <div class="alert">
                    <strong>Note:</strong>
                    Misuse of this function can lead to a buffer overrun. We recommend the use of the
                    safer
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707093(v=vs.85).aspx"><strong>PathCchRenameExtension</strong></a>
                    function in its place.</div>
                  <div></div>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773751(v=vs.85).aspx"><strong>PathSearchAndQualify</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines if a given path is correctly formatted and fully qualified.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773752(v=vs.85).aspx"><strong>PathSetDlgItemPath</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Sets the text of a child control in a window or dialog box, using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773575(v=vs.85).aspx"><strong>PathCompactPath</strong></a> to ensure the path fits in the control.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773754(v=vs.85).aspx"><strong>PathSkipRoot</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Retrieves a pointer to the first character in a path following the drive letter or UNC server/share path elements.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773756(v=vs.85).aspx"><strong>PathStripPath</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Removes the path portion of a fully qualified path and file.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773757(v=vs.85).aspx"><strong>PathStripToRoot</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Removes all file and directory elements in a path except for the root information.</code></li>
                    <li>中譯文</li>
                  </ol>
                  <div class="alert">
                    <strong>Note:</strong>
                    Misuse of this function can lead to a buffer overrun. We recommend the use of the
                    safer
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707096(v=vs.85).aspx"><strong>PathCchStripToRoot</strong></a>
                    function in its place.</div>
                  <div></div>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773759(v=vs.85).aspx"><strong>PathUndecorate</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Removes the decoration from a path string.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773760(v=vs.85).aspx"><strong>PathUnExpandEnvStrings</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Replaces certain folder names in a fully qualified path with their associated environment string.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773762(v=vs.85).aspx"><strong>PathUnmakeSystemFolder</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Removes the attributes from a folder that make it a system folder. This folder must actually exist in the file system.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773763(v=vs.85).aspx"><strong>PathUnquoteSpaces</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Removes quotes from the beginning and end of a path.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/dd378431(v=vs.85).aspx"><strong>SHSkipJunction</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Checks a bind context to see if it is safe to bind to a particular component object.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773766(v=vs.85).aspx"><strong>UrlApplyScheme</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Determines a scheme for a specified URL string, and returns a string with an appropriate prefix.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773768(v=vs.85).aspx"><strong>UrlCanonicalize</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Converts a URL string into canonical form.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773770(v=vs.85).aspx"><strong>UrlCombine</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>When provided with a relative URL and its base, returns a URL in canonical form.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773771(v=vs.85).aspx"><strong>UrlCompare</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Makes a case-sensitive comparison of two URL strings.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773773(v=vs.85).aspx"><strong>UrlCreateFromPath</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Converts a MS-DOS path to a canonicalized URL.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773774(v=vs.85).aspx"><strong>UrlEscape</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Converts characters or surrogate pairs in a URL that might be altered during transport across the Internet ("unsafe" characters) into their corresponding escape sequences.</code></li>
                    <li><code>Surrogate pairs are characters between U+10000 to U+10FFFF (in UTF-32) or between DC00 to DFFF (in UTF-16).</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773776(v=vs.85).aspx"><strong>UrlEscapeSpaces</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>A macro that converts space characters into their corresponding escape sequence.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773780(v=vs.85).aspx"><strong>UrlGetLocation</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Retrieves the location from a URL.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773781(v=vs.85).aspx"><strong>UrlGetPart</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Accepts a URL string and returns a specified part of that URL.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773783(v=vs.85).aspx"><strong>UrlHash</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Hashes a URL string.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773784(v=vs.85).aspx"><strong>UrlIs</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Tests whether a URL is a specified type.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773786(v=vs.85).aspx"><strong>UrlIsFileUrl</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Tests a URL to determine if it is a file URL.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773788(v=vs.85).aspx"><strong>UrlIsNoHistory</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Returns whether a URL is a URL that browsers typically do not include in navigation history.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773789(v=vs.85).aspx"><strong>UrlIsOpaque</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Returns whether a URL is opaque.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773791(v=vs.85).aspx"><strong>UrlUnescape</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Converts escape sequences back into ordinary characters.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
              <tr>
                <td data-th="Topic">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773792(v=vs.85).aspx"><strong>UrlUnescapeInPlace</strong></a></p>
                </td>
                <td data-th="Description">
                  <ol style="list-style-type:none;">                    
                    <li><code>Converts escape sequences back into ordinary characters and overwrites the original string.</code></li>
                    <li>中譯文</li>
                  </ol>
                </td>
              </tr>
            </table>
