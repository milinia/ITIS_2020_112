# Загрузка большой картинки.

1. В проекте `ImageLoadingProject` есть класс `ViewController`. Сделать ячейку для `largeImage` (можно использовать ту же ячейку, что и для просто ячейки `image`, на самом деле, выглядеть будет так же, плюс можно не создавать отдельный CellIdentifier). Картинка в этой ячейке должна загружаться из `previewUrlString`. Методы `UITableViewDataSource` в контроллере необходимо переделать, чтобы использовался массив `rows` (и можно было легко подменить данные и всё продолжало работать).
2. По тапу на ячейку `largeImage` должен открываться экран со Scroll view и progress view (он уже добавлен в `Main.storyboard`, осталось добавить для него класс и всё связать с помощью `IBOutlet`)
3. На этом экране должна загружаться картинка из `urlString`.
4. Прогресс загрузки должен вестись в progress view, чтобы у людей с не самым быстрым интернетом не было проблем с пониманием, что происходит на экране. Для отображения прогресса используйте `URLSessionDownloadDelegate`. Если не приходит `totalBytesExpectedToWrite`, то ок, просто не отображайте progress view.
