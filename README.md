# template
简易 JavaScrpt DOM 模板引擎

使用方法：
详情请查看源码；
<script src="xxxx/template.js"></script>
<script id="ul-template" type="text/template">
  <% data.forEach(funcntion(item){ %>
  <li><%= item.text %></li>
  <% }) %>
</script>

<script>
    var ulData = [
      {
        className: 'class1',
        text: 'text1'
      },
      {
        className: 'class2',
        text: 'text2'
      },
      {
        className: 'class3',
        text: 'text3'
      }
    ];
    var ul = document.getElementById('ul'),
        ulTemplate = document.getElementById('ul-template');
    ul.innterHTML = template(ulTemplate.innerHTML, ulData);
</script>
