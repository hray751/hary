import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.layout.StackPane;
import javafx.scene.media.Media;
import javafx.scene.media.MediaPlayer;
import javafx.scene.media.MediaView;
import javafx.stage.Stage;

public class ResizeVideo extends Application {
    public static void main(String[] args) {
        launch(args);
    }

    @Override
    public void start(Stage primaryStage) {
        // 创建一个Media对象，并指定要播放的视频文件
        Media media = new Media("file:///path/to/video.mp4");

        // 使用Media对象创建一个MediaPlayer对象
        MediaPlayer player = new MediaPlayer(media);

        // 创建一个MediaView对象，并将它与MediaPlayer关联
        MediaView view = new MediaView(player);

        // 设置MediaView的宽度和高度
        view.setFitWidth(640);
        view.setFitHeight(480);

        // 将MediaView添加到布局中
        StackPane root = new StackPane();
        root.getChildren().add
