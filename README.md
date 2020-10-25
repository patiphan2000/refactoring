# refactoring

Project reference [FlashGet](https://github.com/OOP2020/FlashGet/blob/master/src/DownloadTask.java)

 - extract method: eroorPopup was called many times but with different message, extract method make it more modular and more efficient
 ```
public static void errorPopup(String message) {
    Dialog errorURL = new Alert(Alert.AlertType.ERROR);
    errorURL.setContentText(message);
    errorURL.show();
}
 ```
