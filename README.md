# wrongLang
Самое распространненое применение: поиск во время ввода текста в поле ``input``

*Пример*:

```
<input type="text" value="" id="inputText">
<div class="list">
    <div class="listItem"></div>
    <div class="listItem"></div>
    <div class="listItem"></div>
    <div class="listItem"></div>
</div>
```

js + jQuery: 

```
$('#inputText').on('input', function () {
    let text = $(this).val().toLowerCase(),
        wronLagText = wronLag($(this).val()).toLowerCase();
    $('.listItem').each((i, el) => {
        if ($(el).html().toLowerCase().indexOf(text) !== -1 || $(el).html().toLowerCase().indexOf(wronLagText) !== -1) {
            // что то делаем
        }
    });
});
```
