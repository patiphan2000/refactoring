# refactoring

Project reference [FlashGet](https://github.com/OOP2020/FlashGet/blob/master/src/DownloadTask.java)

 - extract method: errorPopup was called many times but with different message, extract method make it more modular and more efficient.
 ```
public static void errorPopup(String message) {
    Dialog errorURL = new Alert(Alert.AlertType.ERROR);
    errorURL.setContentText(message);
    errorURL.show();
}
 ```
 - create helper method: DownloadManager used to handle all the download information so the user interface didn't need to access from DownloadTask.
 ```
public double getAllProgress() {
    double sum = 0;
    for (Task task : allTask) {
    sum += task.getProgress();
    }
    return sum / (double) allTask.size();
}
 ```
