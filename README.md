<h1>Exploratory Testing Report</h1>

<p>The results of exploratory testing of a <a href="https://awilum.github.io">software development portal </a> by <a href="https://github.com/Awilum">@Awilum</a> using <a href="https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2013/jj620911(v=vs.120)?redirectedfrom=MSDN#exploratory-testing-tours">J.Whittaker's tours</a>.</p>
<p>Вы также можете ознакомиться с результатами проведения исследовательского тестирования на <a href="README-RU.md">русском языке</a>.</p>

<h2>Which tours are selected</h2>
<p>Аfter viewing and analyzing the functions of the portal, I chose three tours:</p>
<ul>
<li><a href="#the_supermodel_tour">The Supermodel Tour</a> to view the structure of the portal, interface.  </li>
<li><a href="#the_garbage_collector’s_tour">The Garbage Collector’s Tour</a> to quickly check the transition through the internal structure of the projects presented on the portal. </li>
<li><a href="#the_landmark_tour">The Landmark Tour</a>  for a detailed review of the links and navigation in the documentation (project "Flextype")</li>
 </ul>
 <p>Links to the general description of the tours:
 <br><a href="https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2013/jj620911(v=vs.120)?redirectedfrom=MSDN#the-supermodel-tour">The Supermodel Tour</a><br>
 <a href="https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2013/jj620911(v=vs.120)?redirectedfrom=MSDN#the-garbage-collectors-tour">The Garbage Collector’s Tour</a><br>
 <a href="https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2013/jj620911(v=vs.120)?redirectedfrom=MSDN#the-landmark-tour">The Landmark Tour</a></p>
 

<h3 id="the_supermodel_tour">The Supermodel Tour</h3>
<p>Goal of the tour: watch the interface elements</p>
<p>Environment:  оpera v. 93.0.4585.37</p>
  <table style='width:100%' >
    <thead>
      <tr align='center'>
        <th>Tested</th>
        <th>Noticed</th>
        <th>Attachment</th>
      </tr>
    </thead>
    <tr align='justify'>
      <td>Main page</td>
      <td align='justify'>There are links to sections of the portal located next to the titles about the author and projects. The image isn't displayed in the open source contributions section (attachment 1).</td>
      <td align='centrer'><img src="img/image_isn't_displayed.jpg"><p>attachment 1</p></td>
    </tr>
     <tr align='justify'>
      <td>Menu</td>
      <td>The active section of the site is highlighted. Sections are highlighted when you hover the cursor over them. When changing a section, the selected section of the site is highlighted.</td>
      <td></td>
    </tr>
    <tr align='justify'>
      <td>Projects</td>
      <td rowspan="">
      <p>When a link points to an external site, it open in a separate tab. <b>Feature suggestion:</b> to open external site in a separate tab.</p>
      <p>Project "Master Blocks": The formatting of the header with the project's name is different from other projects headers.</p>
      <p>Project "Cheatsheets": large free space on the right side of the page. User can share the cheat sheet. <b>Feature suggestion:</b> add a hint for a user above the social sharing links, for example "Share cheatsheet on". When sending a link to telegram, the site address is duplicated
      (attachment 2).</p>
      <p>Project "Thermage": large space between headers. Выделяется пустое простраство в блоках features.The open element is not highlighted when switching between sections (attachment 3).<b> Feature suggestion:</b> add highlighting of an open element .</p>
      <p>Projects "Flextype" and "Glowy PHP": when you hover over the sections, there is a backlight. When other selecting sections, the first section remains highlighted (with the main page of the project)(attachment 4). <b> Feature suggestion:</b> add highlighting of an open menu item.</p></td>
      <td><img src="img/double_link_tg.jpg"><p align='centrer'>attachment 2</p> <img src="img/ui_ux_THERMAGE.gif"><p>attachment 3</p><img src="img/highlighted_subsection_is't_highlighted.gif"><p>attachment 4</p></td> 
    </tr>
    <tr align='justify'>
      <td  align='center'>Links</td>
      <td >When clicking on the links "Elements", "Shortcodes API", "and more ..." the pages open with errors.</td>
      <td></td>
    </tr>
    <tr align='center'>
      <td colspan="5">Timeframe : 40 min</td>
    </tr>
  </table>
  
  <p>Links to bug reports:<br>
  <a href="https://github.com/Awilum/dev/issues/32">Internal Server Error: the image isn't displayed on main page</a><br>
  <a href="https://github.com/Awilum/dev/issues/30">404 File not found clicking on the link "Elements" in the feature "Component system" of the project "Thermage"</a><br>
  <a href="https://github.com/Awilum/dev/issues/31">404 File not found clicking on the link "Shortcodes API" in the feature "Shortcodes" of the project "Thermage"</a><br>
  <a href="https://github.com/Awilum/dev/issues/34">Two identical links to the cheat sheet in the Telegram message </a></p>
 
  <p>Links to feature suggestions:</p>

<h3 id="the_garbage_collector’s_tour">The Garbsge Collection Tour</h3>
<p>Goal of the tour:  go screen by screen, not stopping to test in detail, but checking the obvious things </p>
<p>Environment:  оpera v. 93.0.4585.37</p>
<table style='width:100%'>
    <thead>
        <tr align='center'>
        <th>Tested</th>
        <th>Noticed</th>
        <th>Attachment</th>
        </tr>
    </thead>
    <tr align='justify'>
        <td rowspan="2" align='center'>Projects "Cheatsheets" </td>
        <td>There is no link to return to the main page of the section in the path under the heading of the section with the cheat sheet. It can be assumed that it should be  since in the other projects("Flextype" and "Glowy PHP") under the heading of the subsection there is a path.</td>
        <td></td>
    </tr>
        <tr align='justify'>
        <td >Section headers with commands refer to themselves. <b> Feature suggestion:</b>remove links from the block header, or add a list of all commands before the command blocks, with links to similar blocks below.</td>
        <td></td> 
      </tr> 
    <tr align='justify'>
        <td align='center'>Projects "Thermage" </td>
        <td>In the Shortcuts tab there is an example of usage and methods and only after the page with the shortcodes. When going to the page of one of the shortcodes, I noticed a duplicate of the Shortcodes page containing only a list of shortcodes. <b> Feature suggestion: </b>move the table of shortcodes to the beginning of the page, remove the duplicate one. There is also can be bug in project's path: in other project's page below header path don't contain current page (attachment 5).</td>
        <td><img src="img/shortcodes_path.gif"><p>attachment 5</p></td>
    </tr>
     <tr align='justify'>
        <td align='center'>Projects "Flextype"</td>
        <td>The object of the link type without an added link (attachment 6). Also noteworthy is the smaller line spacing of the enumeration in comparison with the main text.</td>
        <td align='centrer'><img src="img/the_link_to_the_author_doesn't_work.gif"><p>attachment 6</p></td>
    </tr>
    <tr align='justify'>
        <td align='center'>Projects "Glowy PHP"</td>
        <td>When going to the installation tabs, I paid attention to the path. In the menu  "Getting Started" item is not a linked section, clicking on this section in the path opened a page with two headings(attachment 7).</td>
        <td align='centrer'><img src="img/page_with_titles.jpg"><p>attachment 7</p></td>
    </tr>
  <tr align='center'>
    <td colspan="5">Timeframe : 30 min</td>
  </tr>
</table>

<p>Links to bug reports:<br>
<a href="https://github.com/Awilum/dev/issues/25">404 File not found clicking on the link "sharing" in the list on the page "View" of the project "Glowy PHP".</a></p>

<p>Links to feature suggestions:</p>

<h3 id="the_landmark_tour">The Landmark Tour</h3>
<p>Goal of the tour:  going from landmark to landmark (
landmark - links in the project documentation)</p>
<p>Environment:  оpera v. 93.0.4585.37</p>
<table style='width:100%'>
  <thead>
    <tr align='centrer' >
      <th>Tested</th>
      <th>Noticed</th>
      <th>Attachment</th>
    </tr>
  </thead>
    <tr align='justify'>
        <td rowspan="3" align='center'>Moving through sections</td>
        <td>the current section is not selected in the side menu. To navigate through the sections, it would be convenient to see which tab from the menu is open (attachment 8).
        <td align='centrer'><img src="img/no_selection_of_the_current_menu_item.gif"><p>attachment 8</p></td>
    </tr>
    <tr align='justify'>
        <td>There is a long time to scroll from bottom to top of some pages. It would be convenient to use the button to move to the top of the page.</td>
        <td></td>
    </tr>
        <tr align='justify'>
        <td>Page "Query" has no content (attachment 9).</td>
        <td align='centrer'><img src="img/emty_page_query.jpg"><p>attachment 9</p></td>
    </tr>
    <tr align='justify'>
        <td align='center'>Arrangement of elements</td>
        <td >"Getting help" provides a link to the overall project. Perhaps should be indicated that this is a link to a common project, or place the link in the header (attachment 10).</td>
        <td align='centrer'><img src="img/indent_top_after_moving_from_menu.jpg"><p>attachment 10</p></td>
    </tr>
    <tr align='justify'>
        <td   align='center'>Links </td>
        <td>The page is opened with error clicking on "MAMP" in "Requirements".</td>
        <td></td>
    </tr>
    <tr align='center'>
      <td colspan="3">Timeframe: 30 min</td>
    </tr>
</table>

<p>Links to bug reports:<br>
<a href="https://github.com/Awilum/dev/issues/34">404 File not found clicking on the link "MAMP" in the "Thermage" documentation point "Requirements"</a>

<p>Links to feature suggestions:</p>


