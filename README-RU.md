<h1> Исследовательское тестирование </h1>
 Результаты проведения исследовательского тестирования <a href="https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2013/jj620911(v=vs.120)?redirectedfrom=MSDN#exploratory-testing-tours">по турам Дж.Уитаккера</a> <a href="https://awilum.github.io">портала о разработке программного обеспечения </a> от <a href="https://github.com/Awilum">@Awilum</a>.

<h2>Какие туры выбраны </h2>
<p>Для тестирования выбраны 3 тура:</p>
<p>Тур супермодели - для просмотра структуры сайта, интерфейса.  </p>
<p>Тур сборщика мусора - для проверки навигации по внутренней структуре проектов, представленных на портале. </p>
<p>Тур по ориентирам - для детального рассмотрения связей в документации проекта Flextype.</p>

<h3>Тур супермодели</h3>
<p>Цель тура: проверить как выглядит портал и какое первое впечатление производит.</p>
<p>Окружение:  оpera v. 93.0.4585.37</p>
  <table style='width:100%' >
    <thead>
      <tr align='center'>
        <th >Что успели протестировать?</th>
        <th>На что обратили внимание?</th>
        <th>Приложения</th>
      </tr>
    </thead>
    <tr align='justify'>
      <td>Главная страница сайта</td>
      <td align='justify'>Возможен переход по ссылкам рядом с заголовками к таким разделам сайта, как информация об авторе и проектах. В разделе "Opensource contributions" не отображается изображение (рис.1).</td>
      <td align='centrer'><img src="img/image_isn't_displayed.jpg"><p>Рис.1</p></td>
    </tr>
     <tr align='justify'>
      <td>Меню</td>
      <td>Выделен активный раздел сайта. Разделы подсвечиваются при наведении на них курсора. При изменении раздела подсвечивается выбранный раздел сайта.</td>
      <td></td>
    </tr>
    <tr align='justify'>
      <td>Вкладка "Projects"</td>
      <td rowspan="">
      <p>Есть ссылки, ведущие на внешние сайты с информацией о проектах, заменяя вкладку сайта. <b>Предложение по улучшению:</b> если ссылка ведет на внешний сайт, сделать открытие в новом окне.</p>
      <p>Проект "Master Blocks": форматирование загаловка отличается от заголовков других проектов.</p>
      <p>Проект "Cheatsheets": в области. Также представлена возможность поделится чит-листом по ссылкам. Не очевидно,для чего эти ссылки. <b>Предложение по улучшению:</b> добавить подсказку для поьзователя, напремер "Share cheat sheet on". <b>Возможный баг:</b> при отправлении ссылки в телеграм дублируется адрес сайта (рис.2).</p>
      <p>Проект "Thermage": большое расстояние между загаловками. Выделяется пустое простраство в блоках features. Также при переключении между разделами не выделяется открытый элемент (рис.3).<b> Предложение по улучшению:</b> добавить выделение открытого элемента.</p>
      <p>На странице с проектами "Flextype" и "Glowy PHP" при наведении на разделы меню идет подсветка выбранного раздела. При переходе к отличному от первого раздела, посвеченным остается первый раздел (рис.4). <b>Предложение по улучшению:</b> добавить выделение открытого элемента</p></td>
      <td><img src="img/double_link_tg.jpg"><p align='centrer'>Рис.2</p> <img src="img/ui_ux_THERMAGE.gif"><p>Рис.3</p><img src="img/highlighted_subsection_is't_highlighted.gif"><p>Рис.4</p></td> 
    </tr>
    <tr align='justify'>
      <td  align='center'>Переход по ссылкам</td>
      <td >При переходе по ссылкам "Elements", "Shortcodes API" сраницы с кодом ответа 404 File not found</td>
      <td></td>
    </tr>
    <tr align='center'>
      <td colspan="5">Затраченное время: 40 мин</td>
    </tr>
  </table>
  
  <p>Ссылка на баг-репорты:<br>
  <a href="https://github.com/Awilum/dev/issues/32">Internal Server Error: the image isn't displayed on main page</a><br>
  <a href="https://github.com/Awilum/dev/issues/30">404 File not found clicking on the link "Elements" in the feature "Component system" of the project "Thermage"</a><br>
  <a href="https://github.com/Awilum/dev/issues/31">404 File not found clicking on the link "Shortcodes API" in the feature "Shortcodes" of the project "Thermage"</a><br>
  <a href="https://github.com/Awilum/dev/issues/34">Two identical links to the cheat sheet in the Telegram message </a>
  </p>
  Ссылка на предложенные улучшения:




<h3>Тур сборщика мусора (The garbsge collection tour)</h3>
<p>Цель тура: не останавливаясь для детального тестирования перемещаться по разделам проектов</p>
<p>Окружение:  оpera v. 93.0.4585.37</p>
<table style='width:100%'>
    <thead>
        <tr align='center'>
        <th>Что успели протестировать?</th>
        <th>На что обратили внимание?</th>
        <th>Приложения</th>
        </tr>
    </thead>
    <tr align='justify'>
        <td rowspan="2" align='center'>Проект "Cheatsheets" </td>
        <td><b>Возможный баг:</b> в пути под заголовком раздела с чит-листом по Linux не активна ссылка возвращения к общей странице раздела. Можно предположить, что она должна быть активна - так как в ранее расcмотренных проектах ("Flextype", "Glowy PHP") под заголовком подраздела находился путь к текущей вкладке. </td>
        <td></td>
    </tr>
        <tr align='justify'>
        <td >Заголовки блоков названия команд ссылаются на самих себя. <b> Предложение по улучшению:</b>убрать ссылки из заголовка блоков, или добавить перед блоками команд список всех команд с сылками на аналогичные блоки ниже</td>
        <td></td> 
      </tr> 
    <tr align='justify'>
        <td align='center'>Проект "Thermage" </td>
        <td>Во вкладке Shortcodes сначала идет пример использования и методы и только после страница с шорткодами. При переходе к странице одного из шорт кодов обратила внимание на дубликат страницы Shortcodes, содержащей только список шорткодов. <b> Предложение по улучшению: </b>перенести таблицу шорткодов в начало страницы, убрать дублирующуюся. Также возможный баг в оставлении страницы в пути (рис. 5)</td>
        <td><img src="img/shortcodes_path.gif"><p>Рис. 5</p></td>
    </tr>
     <tr align='justify'>
        <td align='center'>Проект "Flextype"</td>
        <td>Объект типа ссылка без добавленной ссылки (рис. 6). Также обращает на себя внимание меньший межстрочный интервал перечисления в сравнении с основным текстом</td>
        <td align='centrer'><img src="img/the_link_to_the_author_doesn't_work.gif"><p>Рис. 6</p></td>
    </tr>
    <tr align='justify'>
        <td align='center'>Проект "Glowy PHP"</td>
        <td>Переход к компаненту сисетмы из общей вкладки проекта. При прохождении на вкладки установки, обратила внимание на путь. В меню пункт начала использования не  является отдельным разделом, нажав в пути на этот раздел открылась страница с двумя заголовками (рис. 7)</td>
        <td align='centrer'><img src="img/page_with_titles.jpg"><p>Рис. 7</p></td>
    </tr>
  <tr align='center'>
    <td colspan="5">Затраченное время: 30 мин</td>
  </tr>
</table>

Ссылка на баг-репорты:
<a href="https://github.com/Awilum/dev/issues/25">404 File not found clicking on the link "sharing" in the list on the page "View" of the project "Glowy PHP"</a>

Ссылка на предложенные улучшения:



<h3>Тур по ориентирам</h3>
<p>Цель тура: в проекте проверить функции, которые не главные, но находятся рядом с ними пройтись по документации ради ссылок</p>
ориентир - пройти по документации, проверяя ссылки
Время 30 мин
<p>Окружение:  оpera v. 93.0.4585.37</p>
<table style='width:100%'>
  <thead>
    <tr align='centrer' >
      <th >Что успели протестировать?</th>
      <th>На что обратили внимание?</th>
      <th>Приложения</th>
    </tr>
  </thead>
    <tr align='justify'>
        <td align='center'>Переход к документации </td>
        <td>При переключении между разделами, выделенным остается проект.Возможно стоит выделить каким либо цветом раздел, в котором находится пользователь, или перевести выделение на раздел в котором находится пользователь</td>
        <td></td>
    </tr>
    <tr align='justify'>
        <td rowspan="3" align='center'>Перемещение по разделам</td>
        <td>В боковом меню не выбранный раздел. Для навигации по разделам, было бы  удобно увидеть, какая вкладка из меню открыта (рис.8).</td>
        <td align='centrer'><img src="img/no_selection_of_the_current_menu_item.gif"><p>Рис. 8</p></td>
    </tr>
    <tr align='justify'>
        <td>При перемещении в длинных разделах долго прокручивать в начало страницы. Было бы удобно довать кнопку перемещения к началу страницы </td>
        <td></td>
    </tr>
        <tr align='justify'>
        <td>Пустая страница "Query" (рис. 9)</td>
        <td align='centrer'><img src="img/emty_page_query.jpg"><p>Рис. 9</p></td>
    </tr>
    <tr align='justify'>
        <td align='center'>Расположение элементов на странице</td>
        <td >В getting help дана ссылка на общий проект. Возможно стоит обозначить, что это ссылка на общий проект, или разместить ссылку в заголовке (рис. 10)</td>
        <td align='centrer'><img src="img/indent_top_after_moving_from_menu.jpg"><p>Рис. 10</p></td>
    </tr>
    <tr align='justify'>
        <td align='center'>Ссылки в документации Flextype </td>
        <td>При переходе по ссылке Requirements страница с ошибкой 404</td>
        <td></td>
    </tr>
    <tr align='center'>
      <td colspan="3">Затраченное время: 30 мин</td>
    </tr>
</table>

Ссылка на баг-репорты:
<a href="https://github.com/Awilum/dev/issues/34">404 File not found clicking on the link "MAMP" in the "Thermage" documentation point "Requirements"</a>

Ссылка на предложенные улучшения:
