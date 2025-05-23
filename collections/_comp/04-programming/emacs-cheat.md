---
title: Emacs Cheatsheet
categories: 02-Programming
tags: Cheatsheet
---

<!--
    Basic & File & Buffer & Minibuffer & Windows
    Edit & Marking & Transpose & Case
    Motion
    Search & Replace
    Help
    Programming
    Ediff
    Org-mode
    For-schemers
  -->
<!-- Basic & File & Buffer -->

<table> <!--  -->
  <tr>
    <td colspan="4"><span style="font-weight:bold">Basic</span></td>
  </tr>
  <tr>
    <td>Minimize </td>
    <td>C-z</td>
    <td>Exit Emacs</td>
    <td>C-x C-c</td>
  </tr>
  <tr>
    <td>Run command</td>
    <td>M-x</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">File</span></td>
  </tr>
  <tr>
    <td>Read a file</td>
    <td>C-x C-f</td>
    <td>Save a file</td>
    <td>C-x C-s</td>
  </tr>
  <tr>
    <td>Toggle read-only status</td>
    <td>C-x C-q</td>
    <td>Save all files</td>
    <td>C-x s</td>
  </tr>
  <tr>
    <td>Replace this file with..</td>
    <td>C-x C-v</td>
    <td>Save as..</td>
    <td>C-x C-w</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Buffer</span></td>
  </tr>
  <tr>
    <td>Switch to buffer..</td>
    <td>C-x b</td>
    <td>List all buffers</td>
    <td>C-x C-b</td>
  </tr>
  <tr>
    <td>Insert a file to buffer</td>
    <td>C-x i</td>
    <td>Kill buffer</td>
    <td>C-x k</td>
  </tr>
  <tr>
    <td>Kill some buffers</td>
    <td>M-x kill-some-buffers</td>
    <td>Last/Next buffer</td>
    <td>C-x ←/→</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Minibuffer</span></td>
  </tr>
  <tr>
    <td>Auto Complete</td>
    <td>TAB</td>
    <td>Complete and execute</td>
    <td>RET</td>
  </tr>
  <tr>
    <td>Fetch previous input</td>
    <td>M-p</td>
    <td>Fetch later input</td>
    <td>M-n</td>
  </tr>
  <tr>
    <td colspan="2">Regexp backward/forward search through history</td>
    <td>M-r</td>
    <td>M-s</td>
  </tr>
  <tr>
    <td>Abort minibuffer</td>
    <td>C-g</td>
    <td>Redo last command</td>
    <td>C-x Esc Esc</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Error Recovery</span></td>
  </tr>
  <tr>
    <td>Recover file</td>
    <td>M-x recover-session</td>
    <td>Undo tree</td>
    <td>C-x u</td>
  </tr>
  <tr>
    <td>Restore buffer</td>
    <td>M-x revert-buffer</td>
    <td>Undo once</td>
    <td>C-/ or C-_</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Windows</span></td>
  </tr>
  <tr>
    <td>Delete all other windows</td>
    <td>C-x 1</td>
    <td>Delete current window</td>
    <td>C-x 0</td>
  </tr>
  <tr>
    <td>Split horizontally</td>
    <td>C-x 2</td>
    <td>Split vertically</td>
    <td>C-x 3</td>
  </tr>
  <tr>
    <td>Scroll other window</td>
    <td>C-M-v</td>
    <td>Switch to &lt;a-z&gt;</td>
    <td>C-x o &lt;a-z&gt;</td>
  </tr>
  <tr>
    <td>Switch to &lt;1-9&gt;</td>
    <td>M-&lt;1-9&gt;</td>
    <td>Find file in other window</td>
    <td>C-x 4 f</td>
  </tr>
  <tr>
    <td>Open buffer in other window</td>
    <td>C-x 4 b</td>
    <td colspan="2"></td>
  </tr>
</table>

<!-- Editing & Marking -->

<table>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Marking</span></td>
  </tr>
  <tr>
    <td>Set mark point</td>
    <td>C-@</td>
    <td>Exchange point and mark</td>
    <td>C-x C-x</td>
  </tr>
  <tr>
    <td>Mark word by word</td>
    <td>M-@</td>
    <td>Mark paragraph</td>
    <td>M-h</td>
  </tr>
  <tr>
    <td>Mark page</td>
    <td>C-x C-p</td>
    <td>Mark sexp</td>
    <td>C-M-@</td>
  </tr>
  <tr>
    <td>Mark function</td>
    <td>C-M-h</td>
    <td>Mark entire buffer</td>
    <td>C-x h</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Copy and Paste</span></td>
  </tr>
  <tr>
    <td>Cut region to kill ring</td>
    <td>C-w</td>
    <td>Copy region to kill ring</td>
    <td>M-w</td>
  </tr>
  <tr>
    <td>Cut through next char</td>
    <td>M-z &lt;char&gt;</td>
    <td>Paste (yank back)</td>
    <td>C-y</td>
  </tr>
  <tr>
    <td colspan="3">Replace last paste (yank) with previous kill</td>
    <td>M-y</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Transpose</span></td>
  </tr>
  <tr>
    <td>Transpose characters</td>
    <td>C-t</td>
    <td>Transpose words</td>
    <td>M-t</td>
  </tr>
  <tr>
    <td>Transpose lines</td>
    <td>C-x C-t</td>
    <td>Transpose sexps</td>
    <td>C-M-t</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Case Change</span></td>
  </tr>
  <tr>
    <td>Uppercase word</td>
    <td>M-u</td>
    <td>Lowercase word</td>
    <td>M-l</td>
  </tr>
  <tr>
    <td>Capitalize word</td>
    <td>M-c</td>
    <td>Uppercase region</td>
    <td>C-x C-u</td>
  </tr>
  <tr>
    <td>Lowercase region </td>
    <td>C-x C-l</td>
    <td colspan="2"></td>
  </tr>
</table>

<!-- Motion -->

<table>
  <tr>
    <th rowspan="2">Cursor Motion<br></th>
    <td colspan="4"><span style="font-weight:bold">Operation</span></td>
  </tr>
  <tr>
    <td colspan="2">Move</td>
    <td colspan="2">Delete</td>
  </tr>
  <tr>
    <td>Amount</td>
    <td>Forward</td>
    <td><span style="font-weight:bold">B</span>ackward</td>
    <td>Forward</td>
    <td><span style="font-weight:bold">B</span>ackward</td>
  </tr>
  <tr>
    <td>Characters</td>
    <td>C-f</td>
    <td>C-b</td>
    <td>C-d</td>
    <td>DEL</td>
  </tr>
  <tr>
    <td>Words</td>
    <td>M-f</td>
    <td>M-b</td>
    <td>M-d</td>
    <td>M-DEL</td>
  </tr>
  <tr>
    <td>Lines</td>
    <td>C-n</td>
    <td>C-p</td>
    <td>C-k (to EOL)</td>
    <td>C-SPC C-a C-w</td>
  </tr>
  <tr>
    <td>Sentences</td>
    <td>M-e</td>
    <td>M-a</td>
    <td>M-k</td>
    <td>C-x DEL</td>
  </tr>
  <tr>
    <td>Expressions</td>
    <td>C-M-f</td>
    <td>C-M-b</td>
    <td>C-M-k</td>
    <td>C-M-DEL</td>
  </tr>
  <tr>
    <td>Section</td>
    <td>C-M-a</td>
    <td>C-M-e</td>
    <td colspan="2" rowspan="3"></td>
  </tr>
  <tr>
    <td>Paragraphs</td>
    <td>M-}</td>
    <td>M-{</td>
  </tr>
  <tr>
    <td>Screen</td>
    <td>M-v</td>
    <td>C-v</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">End or Start of</span></td>
  </tr>
  <tr>
    <td>Line</td>
    <td colspan="2">C-e</td>
    <td colspan="2">C-a</td>
  </tr>
  <tr>
    <td>Buffer</td>
    <td colspan="2">M-&gt;</td>
    <td colspan="2">M-&lt;</td>
  </tr>
  <tr>
    <td>Defun</td>
    <td colspan="2">C-M-a</td>
    <td colspan="2">C-M-e</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Special Motion</span></td>
  </tr>
  <tr>
    <td colspan="3">Go to line</td>
    <td colspan="2">M-g g</td>
  </tr>
  <tr>
    <td colspan="3">Go to Char</td>
    <td colspan="2">M-g c</td>
  </tr>
  <tr>
    <td colspan="3">Back to indentation</td>
    <td colspan="2">M-m</td>
  </tr>
  <tr>
    <td colspan="3">Scroll current line to center/top/bottom</td>
    <td colspan="2">C-l</td>
  </tr>
</table>
<!-- Search & Replace -->

<table>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Search</span></td>
  </tr>
  <tr>
    <td>Search forward</td>
    <td>C-s</td>
    <td>Search backward</td>
    <td>C-r</td>
  </tr>
  <tr>
    <td>Regexp forward</td>
    <td>C-M-s</td>
    <td>Regexp backward</td>
    <td>C-M-r</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Replace</span></td>
  </tr>
  <tr>
    <td>Start query replace</td>
    <td>M-%</td>
    <td>Query replace word</td>
    <td>C-u M-%</td>
  </tr>
  <tr>
    <td>Query replace by regexp</td>
    <td>M-x query-replace-regexp</td>
    <td>Replace once</td>
    <td>y</td>
  </tr>
  <tr>
    <td>Skip once </td>
    <td>n</td>
    <td>Replace all</td>
    <td>!</td>
  </tr>
  <tr>
    <td>Back up to previous match</td>
    <td>^</td>
    <td>Exit query Replace</td>
    <td>RET</td>
  </tr>
</table>

<!--  Help -->

<table>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Help</span></td>
  </tr>
  <tr>
    <td>Tutorial</td>
    <td>C-h t</td>
    <td>Search command by word</td>
    <td>C-h a</td>
  </tr>
  <tr>
    <td>Describe bindings</td>
    <td>C-h b</td>
    <td>Describe keys</td>
    <td>C-h k</td>
  </tr>
  <tr>
    <td>Describe functions</td>
    <td>C-h f</td>
    <td>Find function on keys</td>
    <td>C-h K</td>
  </tr>
  <tr>
    <td>Get mode information</td>
    <td>C-h m</td>
    <td>Describe packages</td>
    <td>C-h P</td>
  </tr>
</table>

<!-- Programming -->

<table>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Programming</span></td>
  </tr>
  <tr>
    <td>Toggle node</td>
    <td>C-,</td>
    <td>Comment a region</td>
    <td>C-M-;</td>
  </tr>
  <tr>
    <td>Insert comment line</td>
    <td>M-;</td>
    <td>Find next error</td>
    <td>C-x '</td>
  </tr>
  <tr>
    <td>Start a shell in a window</td>
    <td>C-x t</td>
    <td>Start slime</td>
    <td>C-x j</td>
  </tr>
  <tr>
    <td>Toggle &lt;xxx&gt;-mode</td>
    <td>M-x &lt;xxx&gt;-mode</td>
    <td>Compile window</td>
    <td>M-x compile</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Shell</span></td>
  </tr>
  <tr>
    <td>Execute a shell command</td>
    <td>M-!</td>
    <td>Execute asynchronously</td>
    <td>M-&amp;</td>
  </tr>
  <tr>
    <td>Run command on a region</td>
    <td>M-|</td>
    <td>filter a region through a command</td>
    <td>C-u M-|</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Paredit</span></td>
  </tr>
  <tr>
    <td colspan="2">Before</td>
    <td>After</td>
    <td>Key</td>
  </tr>
  <tr>
    <td colspan="2">(foo (bar |baz) quux zot)</td>
    <td>(foo (bar |baz quux) zot)</td>
    <td>C-&lt;right&gt;</td>
  </tr>
  <tr>
    <td colspan="2">(foo (bar |baz quux) zot)</td>
    <td>(foo (bar |baz) quux zot)</td>
    <td>C-&lt;left&gt;</td>
  </tr>
  <tr>
    <td colspan="2">(foo bar (baz| quux) zot)</td>
    <td>(foo (bar baz| quux) zot)</td>
    <td>C-M-&lt;left&gt;</td>
  </tr>
  <tr>
    <td colspan="2">(foo (bar baz |quux) zot)</td>
    <td>(foo bar (baz |quux) zot)</td>
    <td>C-M-&lt;right&gt;</td>
  </tr>
</table>

<!-- Ediff -->

<table>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Ediff</span></td>
  </tr>
  <tr>
    <td>Start ediff</td>
    <td>M-x ediff</td>
    <td>Suspend/Quit</td>
    <td>z/q</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Move Around</span></td>
  </tr>
  <tr>
    <td>Pervious diff</td>
    <td>p or DEL</td>
    <td>Next diff</td>
    <td>n or SPC</td>
  </tr>
  <tr>
    <td>Jump to diff</td>
    <td>j</td>
    <td>Goto X's point</td>
    <td>gx</td>
  </tr>
  <tr>
    <td>Recenter</td>
    <td>C-l</td>
    <td>Scroll up/down</td>
    <td>v/V</td>
  </tr>
  <tr>
    <td>Scroll lt/rt</td>
    <td>&lt;/&gt;</td>
    <td>Swap Variants</td>
    <td>~</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Toggle Features</span></td>
  </tr>
  <tr>
    <td>Vert/Horiz split</td>
    <td>|</td>
    <td>Highlighting</td>
    <td>h</td>
  </tr>
  <tr>
    <td>Auto-refinement</td>
    <td>@</td>
    <td>Ignore whitespaces</td>
    <td>##</td>
  </tr>
  <tr>
    <td>Ignore case</td>
    <td>#c</td>
    <td>Focus/hide regions</td>
    <td>#f/#h</td>
  </tr>
  <tr>
    <td>read-only in buf X</td>
    <td>X</td>
    <td>wide display</td>
    <td>m</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">Manipulate</span><br></td>
  </tr>
  <tr>
    <td>Copy A/B's region to B/A</td>
    <td>a/b</td>
    <td>Restore buf X's old diff</td>
    <td>rx</td>
  </tr>
  <tr>
    <td>Refine current region</td>
    <td>*</td>
    <td>Update diff regions</td>
    <td>!</td>
  </tr>
  <tr>
    <td>Save buf x</td>
    <td>wx</td>
    <td>Save diff output</td>
    <td>wd</td>
  </tr>
  <tr>
    <td colspan="4"><span style="font-weight:bold">System</span></td>
  </tr>
  <tr>
    <td>Show registry</td>
    <td>R</td>
    <td>Diff output</td>
    <td>D</td>
  </tr>
  <tr>
    <td>Status information</td>
    <td>i</td>
    <td>Compare regions</td>
    <td>=</td>
  </tr>
</table>


<!-- Todo: Org-Mode, For Schemers -->


在 **Emacs** 中输入特殊符号或非 ASCII 字符，你可以使用一些快捷键和命令来插入它们。以下是一些常见的输入特殊符号的方法和对应的快捷键：

### 1. **输入 Unicode 字符**
Emacs 提供了通过 Unicode 代码点直接插入字符的方法。

- **M-x insert-char** (按下 `Alt` + `x`，然后输入 `insert-char`，按回车)  
  - 这将允许你输入字符的 Unicode 代码点。
  - 你可以输入一个字符的十六进制 Unicode 编码（例如，`03A9` 代表希腊字母 Omega `Ω`）。
  
例如：
- 输入 `M-x insert-char` 然后输入 `03A9`，按回车，Emacs 会插入 `Ω`。

### 2. **使用 `C-x 8` 进行特殊字符输入**
Emacs 还支持通过 `C-x 8` (即 `Control` + `x`，然后按 `8`) 输入特殊字符。你可以按数字键选择符号，或直接输入符号名称。

- **C-x 8 <符号名或编码>**：使用符号的名称或 Unicode 编码来插入符号。
  - 例如，`C-x 8 α` 插入希腊字母 `α`。
  - `C-x 8 03A9` 插入 `Ω`。

### 3. **常用符号和特殊字符**
以下是一些常见的符号及其对应的输入方法：

#### 1. **希腊字母**
- `α` (希腊字母 Alpha)：`C-x 8 a`
- `β` (希腊字母 Beta)：`C-x 8 b`
- `Ω` (希腊字母 Omega)：`C-x 8 O`

#### 2. **数学符号**
- `∞` (无穷大)：`C-x 8 i`
- `√` (平方根)：`C-x 8 s`
- `∑` (求和符号)：`C-x 8 S`

#### 3. **货币符号**
- `€` (欧元符号)：`C-x 8 e`
- `£` (英镑符号)：`C-x 8 L`
- `¥` (日元符号)：`C-x 8 y`

#### 4. **箭头符号**
- `→` (右箭头)：`C-x 8 ->`
- `←` (左箭头)：`C-x 8 <-`
- `↑` (上箭头)：`C-x 8 ^`
- `↓` (下箭头)：`C-x 8 v`

#### 5. **数学符号**
- `≠` (不等于)：`C-x 8 !=`
- `≤` (小于等于)：`C-x 8 <=`
- `≥` (大于等于)：`C-x 8 >=`

#### 6. **其他符号**
- `©` (版权符号)：`C-x 8 c`
- `®` (注册商标符号)：`C-x 8 r`
- `™` (商标符号)：`C-x 8 t`
  
#### 7. **标点符号**
- `“ ”` (英文双引号)：`C-x 8 "`
- `‘ ’` (英文单引号)：`C-x 8 '`
- `•` (项目符号)：`C-x 8 *`

### 4. **字符输入法（`Quail`）**
你也可以使用 Emacs 的 **输入法** 来输入一些特殊字符。一个常用的输入法是 **Quail 输入法**，可以通过 `M-x set-input-method` 设置，支持多种语言和字符集。

### 5. **复制粘贴特殊字符**
如果某个特殊字符非常难以通过快捷键输入，你还可以从其他地方（如网页或文档）复制并粘贴到 Emacs 中。

---

### 总结
在 Emacs 中输入特殊符号，你可以通过以下方式：
- 使用 `M-x insert-char` 输入 Unicode 字符。
- 使用 `C-x 8` 输入常见的符号和特殊字符。
- 通过 `C-x 8` 加上符号名称或编码来插入特定字符。

通过这些方法，你可以在 Emacs 中方便地插入各种特殊符号。