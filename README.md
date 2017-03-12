<table width="100%">
              <tr responsive="true">
                <th scope="col" class="style3">主題</th>
                <th scope="col" class="style3">描述</th>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773561(v=vs.85).aspx"><strong>PathAddBackslash</strong></a></p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <ol style="list-style-type:none;">                    
                    <li><code>Adds a backslash to the end of a string to create the correct syntax for a path.</code></li>
                    <li><code>If the source path already has a trailing backslash, no backslash will be added.</code></li>                    
                    <li>將反斜線新增到字串的末尾做為新的路徑，如果原始路徑沒有反斜線則不會新增。</li>
                  </ol>
                  <code>
                  <ol>
                    <li>TCHAR szBackslashNot[_MAX_PATH] = _T("C:\\TEST\\FILE");</li>
                    <li>TCHAR szBackslashYes[_MAX_PATH] = _T("C:\\TEST\\FILE\\");</li>
                    <li>_tprintf(_T("%X = [%s]\r\n"), ::PathAddBackslash(szBackslashNot), szBackslashNot); // C:\TEST\FILE\</li>
                    <li>_tprintf(_T("%X = [%s]\r\n"), ::PathAddBackslash(szBackslashYes), szBackslashYes); // C:\TEST\FILE\</li>
                  </ol>
                  </code>
                  <div class="style5">
                    <strong>Note:</strong>
                    <span>Misuse of this function can lead to a buffer overrun. We recommend the use of the safer</span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707078(v=vs.85).aspx"><strong>PathCchAddBackslash</strong></a>
                    <span>or</span>                    
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707079(v=vs.85).aspx"><strong>PathCchAddBackslashEx</strong></a>                      
                    <span>function in its place.</span></br>          
                    <strong>注意:</strong>
                    <span>此功能濫用可能導致緩衝區溢出，建議使用更安全的</span>
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
                  <ol>
                    <li>TCHAR szFilePath[_MAX_PATH] = _T("C:\\TEST\\FILE");</li>
                    <li>TCHAR szExts[_MAX_EXT] = _T(".doc");</li>
                    <li>_tprintf(_T("%d = [%s]\r\n"), ::PathAddExtension(szFilePath, szExts), szFilePath); // C:\TEST\FILE.doc</li>
                  </ol>
                  </code>
                  <div class="style5">
                    <strong>Note:</strong>
                    <span>Misuse of this function can lead to a buffer overrun. We recommend the use of the safer</span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707080(v=vs.85).aspx"><strong>PathCchAddExtension</strong></a>
                    <span>function in its place.</span></br>          
                    <strong>注意:</strong>
                    <span>此功能濫用可能導致緩衝區溢出，建議使用更安全的</span>
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
                  <div class="style5">
                    <strong>Note:</strong>
                    <span>Misuse of this function can lead to a buffer overrun. We recommend the use of the safer</span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707081(v=vs.85).aspx"><strong>PathCchAppend</strong></a>
                    <span>or</span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707082(v=vs.85).aspx"><strong>PathCchAppendEx</strong></a>
                    <span>function in its place.</span></br>
                    <strong>注意:</strong>
                    <span>此功能濫用可能導致緩衝區溢出，建議使用更安全的</span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707081(v=vs.85).aspx"><strong>PathCchAppend</strong></a>
                    <span> 或 </span>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707082(v=vs.85).aspx"><strong>PathCchAppendEx</strong></a>
                    <span> 的函式。</span>
                  </div>
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
                    <li>串聯兩個字串到正確的路徑格式;此外將任何相對路徑元素連接在一起。</li>
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
                  <div class="style5">
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
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773574(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathCommonPrefix </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>比較兩個路徑以確定它們是否共享公共前綴。前綴是以下類型之一：“C：\\”，“。”，“..”，“.. \\”。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773575(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathCompactPath </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>通過用橢圓替換路徑組件來截斷檔案路徑以適合給定的像素寬度。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773578(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathCompactPathEx </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>通過用橢圓替換路徑組件來截斷路徑以適合一定數量的字符。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773581(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathCreateFromUrl </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>將檔案URL轉換為Microsoft MS-DOS路徑。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773583(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathCreateFromUrlAlloc </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>從檔案URL創建路徑。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773584(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathFileExists </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>確定檔案系統對象（例如檔案或檔案夾）的路徑是否有效。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773587(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathFindExtension </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  傳回副檔名。
                  <code>
                    <ol class="list-group">
                      <li>TCHAR szBuffer[_MAX_PATH] = _T("C:\\path\\file.exe");</li>
                      <li>LPTSTR pszRetval = ::PathFindExtension(szBuffer);</li>
                      <li>_tprintf(_T("%s\n"), pszRetval); // => _T(".exe");</li>
                      <li>_tprintf(_T("%s\n"), szBuffer); // => _T("C:\\path\\file.exe");</li>
                    </ol>
                  </code>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773589(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathFindFileName </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  傳回檔案名稱。
                  <code>
                    <ol class="list-group">
                      <li>TCHAR szBuffer[_MAX_PATH] = _T("C:\\path\\file.exe");</li>
                      <li>LPTSTR pszRetval = ::PathFindFileName(szBuffer);</li>
                      <li>_tprintf(_T("%s\n"), pszRetval); // => _T("file.exe");</li>
                      <li>_tprintf(_T("%s\n"), szBuffer); // => _T("C:\\path\\file.exe");</li>
                    </ol>
                  </code></td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773591(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathFindNextComponent </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>解析路徑並返回第一個反斜線之後的路徑部分。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773594(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathFindOnPath </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>搜索檔案。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773598(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathFindSuffixArray </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>確定給定檔案名稱是否具有後綴列表中的一個。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773602(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathGetArgs </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>查找給定路徑中的命令行參數。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773608(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathGetCharType</strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>確定與路徑相關的字符類型。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773612(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathGetDriveNumber </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>搜索“A”到“Z”範圍內的驅動器盤符的路徑，並返回相應的驅動器號。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773617(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsContentType </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>確定檔案的註冊內容類型是否與指定的內容類型匹配。此函數獲取指定檔案類型的內容類型，並將該字串與<em>pszContentType</em>進行比較。比較不區分大小寫。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773621(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsDirectory </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  是否為有效目錄。 
                  <code>
                  <ol>
                    <li>// (FILE_ATTRIBUTE_DIRECTORY & wfd.dwFileAttributes) = 0 / 16</li>
                    <li>_tprintf(_T("%d\n"), ::PathIsDirectory(_T("C:\\Windows"))); // 16</li>
                    <li>_tprintf(_T("%d\n"), ::PathIsDirectory(_T("C:\\Windows\\"))); // 16</li>
                    <li>_tprintf(_T("%d\n"), ::PathIsDirectory(_T("C:\\Windows\\sample.exe"))); // 0</li>
                  </ol>
                  </code>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773623(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsDirectoryEmpty </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">是否為空目錄。 <code>
                  <ol>
                    <li>_tprintf(_T("%d\n"), ::PathIsDirectoryEmpty(_T("C:\\Windows"))); // 0</li>
                    <li>_tprintf(_T("%d\n"), ::PathIsDirectoryEmpty(_T("C:\\Windows\\"))); // 0</li>
                    <li>_tprintf(_T("%d\n"), ::PathIsDirectoryEmpty(_T("C:\\Windows\\sample.exe"))); // 0</li>
                    <li>_tprintf(_T("%d\n"), ::PathIsDirectoryEmpty(_T("C:\\Windows\\tracing\\PowerTracker"))); // 1</li>
                  </ol>
                </code></td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773627(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsFileSpec </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  是否為純檔案名稱，不包含任何路徑分隔字符 (例如: &#39;:&#39; 或 &#39;\&#39;) 的路徑。
                  <code>
                    <ol>
                      <li>TRUE = ::PathIsFileSpec(_T("sample"));</li>
                      <li>TRUE = ::PathIsFileSpec(_T("sample.exe"));</li>
                      <li>FALSE = ::PathIsFileSpec(_T("C:\\TEST\\sample"));</li>
                      <li>FALSE = ::PathIsFileSpec(_T("C:\\TEST\\sample\\"));</li>
                      <li>FALSE = ::PathIsFileSpec(_T("C:\\TEST\\sample.exe"));</li>
                    </ol>
                  </code>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773631(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsHTMLFile </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>確定檔案是否為HTML檔案。根據為檔案副檔名註冊的內容類型進行確定。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773635(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsLFNFileSpec </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>確定檔案名稱是否為長格式。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773640(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsNetworkPath </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>確定路徑字串是否表示網絡資源。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773650(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsPrefix </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>搜索路徑以確定其是否包含由<em>pszPrefix</em>傳遞的類型的有效前綴。前綴是以下類型之一：“C：\\”，“。”，“..”，“.. \\”。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773660(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsRelative </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>搜索路徑並確定它是否為相對路徑。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773674(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsRoot </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>確定路徑字串是否是卷的根。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773687(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsSameRoot </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>比較兩個路徑以確定它們是否具有公共根組件。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773701(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsSystemFolder </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>確定現有檔案夾是否包含使其成為系統檔案夾的屬性。或者，此功能指示某些屬性是否將檔案夾限定為系統檔案夾。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773712(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsUNC </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>確定路徑字串是否是有效的通用命名約定（UNC）路徑，而不是基於驅動器號的路徑。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773722(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsUNCServer </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>確定字串是否是服務器路徑的有效UNC。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773723(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsUNCServerShare </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                <ul style="list-style-type:none;">
                  <li>是否為有效的 UNC 共用路徑。<em>\\server\\share</em>。</li>
                  <li><code>Determines if a string is a valid UNC share path,<em>\\server\share</em>.</li>
                  </ul>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773724(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathIsURL </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <ul style="list-style-type:none;">
                    <li>是否為有效的 URL 格式。</li>
                    <li><code>Tests a given string to determine if it conforms to a valid URL format.</code></li>
                  </ul>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773725(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathMakePretty </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">       
                  <ul style="list-style-type:none;">
                    <li>將大寫字元轉換為小寫字元。</li>
                    <li><code>Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance.</code></li>
                  </ul>
                  <code>
                    <ol>
                      <li>TCHAR szUppercase[_MAX_PATH] = _T("C:\\TEST\\FILE");</li>
                      <li>TCHAR szLowercase[_MAX_PATH] = _T("C:\\test\\sample");</li>
                      <li>TCHAR szMixedchar[_MAX_PATH] = _T("C:\\TEST\\Sample");</li>
                      <li>_tprintf(_T("%d = [%s]\r\n"), ::PathMakePretty(szUppercase), szUppercase); // 1 C:\test\sample</li>
                      <li>_tprintf(_T("%d = [%s]\r\n"), ::PathMakePretty(szLowercase), szLowercase); // 0 C:\test\sample</li>
                      <li>_tprintf(_T("%d = [%s]\r\n"), ::PathMakePretty(szMixedchar), szMixedchar); // 0 C:\TEST\Sample</li>
                    </ol>
                  </code>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773726(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathMakeSystemFolder </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>為現有檔案夾提供適當的屬性以成為系統檔案夾。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773727(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathMatchSpec </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>使用MS-DOS通配符匹配類型搜索字串。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773728(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathMatchSpecEx </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>將路徑中的檔案名稱與一個或多個檔案名稱模式匹配。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773737(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathParseIconLocation </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>解析包含檔案位置和圖標索引的檔案位置字串，並返回單獨的值。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773739(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathQuoteSpaces </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>搜索空格的路徑。如果找到空格，則整個路徑用引號括起來。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773740(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathRelativePathTo </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>創建從一個檔案或檔案夾到另一個檔案的相對路徑。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773742(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathRemoveArgs </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>從給定路徑中刪除任何參數。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773743(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathRemoveBackslash</strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  刪除路徑尾部的反斜線。
                  <code>
                    <ol>
                      <li>TCHAR szBufferNot[_MAX_PATH] = _T("C:\\TEST\\sample");</li>
                      <li>TCHAR szBufferYes[_MAX_PATH] = _T("C:\\TEST\\sample\\");</li> 
                      <li>_tprintf(_T("%s\r\n"), szBufferNot); // _T("C:\\TEST\\sample"); </li>
                      <li>_tprintf(_T("%s\r\n"), szBufferYes); // _T("C:\\TEST\\sample");</li>  
                    </ol>
                  </code>
                  <div class="style5">
                    <strong>注意 </strong>
                    此功能已棄用。我們建議在其位置使用
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707089(v=vs.85).aspx">
                    <strong xmlns="http://www.w3.org/1999/xhtml"> PathCchRemoveBackslash </strong>
                    </a>
                    或
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707090(v=vs.85).aspx">
                    <strong xmlns="http://www.w3.org/1999/xhtml">PathCchRemoveBackslashEx </strong>
                    </a>
                    函數。
                    </div>
                  <div></div>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773745(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathRemoveBlanks </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>刪除字串中的所有前導和尾隨空格。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773746(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathRemoveExtension </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  刪除檔案副檔名(如果存在)。 GetFileTitle
                  <code>
                    <ol>
                      <li>szBuff = _T("C:\\path\\file.exe");</li>
                      <li>::PathRemoveExtension(szBuff);</li>
                      <li>szBuff = _T("C:\\path\\file");</li>
                    </ol>
                  </code>
                  <div class="style5">
                    <strong>注意 </strong>
                    此功能已棄用。我們建議在其位置使用
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707091(v=vs.85).aspx">
                    <strong xmlns="http://www.w3.org/1999/xhtml"> PathCchRemoveExtension </strong>
                    </a>
                    。</div>
                  <div></div>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773748(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathRemoveFileSpec </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>從路徑中刪除尾部檔案名稱和反斜線（如果它們存在）。</p>
                  <div class="style5">
                    <strong>注意 </strong>
                    此功能已棄用。我們建議在其位置使用<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707092(v=vs.85).aspx"><strong
                      xmlns="http://www.w3.org/1999/xhtml"> PathCchRemoveFileSpec </strong>
                    </a>
                    函數。</div>
                  <div></div>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773749(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathRenameExtension </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>用新副檔名替換檔案名稱的副檔名。如果檔案名稱不包含副檔名，副檔名將附加到字串的結尾。</p>
                  <div class="style5">
                    <strong>注意 </strong>
                    此功能濫用可能導致緩衝區溢出。我們建議在其位置使用更安全的<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707093(v=vs.85).aspx"><strong
                      xmlns="http://www.w3.org/1999/xhtml"> PathCchRenameExtension </strong>
                    </a>
                    函數。</div>
                  <div></div>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773751(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathSearchAndQualify </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>確定給定路徑是否正確格式化和完全限定。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773752(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathSetDlgItemPath </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>使用<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773575(v=vs.85).aspx"><strong
                    xmlns="http://www.w3.org/1999/xhtml"> PathCompactPath </strong>
                  </a>
                    在窗口或對話框中設置子控件的文本，以確保路徑適合控件。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773754(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathSkipRoot </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>檢索指向驅動器號或UNC服務器/共享路徑元素後面路徑中第一個字符的指針。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773756(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathStripPath </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>刪除完全限定路徑和檔案的路徑部分。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773757(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathStripToRoot </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>刪除路徑中除根信息之外的所有檔案和目錄元素。</p>
                  <div class="style5">
                    <strong>注意 </strong>
                    此功能濫用可能導致緩衝區溢出。我們建議在其位置使用更安全的<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/hh707096(v=vs.85).aspx"><strong
                      xmlns="http://www.w3.org/1999/xhtml"> PathCchStripToRoot </strong>
                    </a>
                    函數。</div>
                  <div></div>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773759(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathUndecorate </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>從路徑字串中刪除裝飾。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773760(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathUnExpandEnvStrings </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>將完全限定路徑中的某些檔案夾名稱替換為其關聯的環境字串。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773762(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathUnmakeSystemFolder </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>從檔案夾中刪除使其成為系統檔案夾的屬性。此檔案夾實際上必須存在於檔案系統中。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773763(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">PathUnquoteSpaces </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>從路徑的開頭和結尾刪除引號。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/dd378431(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">SHSkipJunction </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>檢查綁定上下文以查看綁定到特定組件對像是否安全。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773766(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlApplyScheme </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>確定指定URL字串的方案，並返回具有適當前綴的字串。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773768(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlCanonicalize </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>將URL字串轉換為規範形式。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773770(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlCombine </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>當提供相對URL及其基址時，返回規範形式的URL。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773771(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlCompare </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>對兩個網址字串進行區分大小寫比較。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773773(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlCreateFromPath </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>將MS-DOS路徑轉換為規範化的URL。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773774(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlEscape </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>將可能在通過Internet傳輸期間更改的URL（“不安全”字符）中的字符或代理對轉換為其相應的轉義序列。代理對是U + 10000到U + 10FFFF（在UTF-32中）或DC00到DFFF（在UTF-16中）之間的字符。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773776(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlEscapeSpaces </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>將空格字符轉換為其對應的轉義序列的宏。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773780(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlGetLocation </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>從網址檢索位置。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773781(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlGetPart </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>接受URL字串並返回該URL的指定部分。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773783(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlHash </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>哈希URL字串。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773784(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlIs </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>測試URL是否為指定類型。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773786(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlIsFileUrl </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>測試URL以確定它是否是檔案URL。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773788(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlIsNoHistory </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>返回網址是否為瀏覽器通常不包含在導航歷史記錄中的網址。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773789(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlIsOpaque </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>返回網址是否不透明。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773791(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlUnescape </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>將轉義序列轉換回普通字符。</p>
                </td>
              </tr>
              <tr>
                <td data-th="Topic" class="style4" style="min-width: 80px;">
                  <p>
                    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/bb773792(v=vs.85).aspx">
                      <strong xmlns="http://www.w3.org/1999/xhtml">UrlUnescapeInPlace </strong>
                    </a>
                  </p>
                </td>
                <td data-th="Description" class="style4" style="min-width: 80px;">
                  <p>將轉義序列轉換回普通字符並覆蓋原始字串。</p>
                </td>
              </tr>
            </table>
