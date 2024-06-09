## Implementación de un Sistema de Menús en una Aplicación JavaFX

Este código JavaFX crea una interfaz gráfica con varios controles (botón, casilla de verificación, hipervínculo, botón de alternancia, botón de radio, etiquetas, campo de texto, campo de contraseña, área de texto, indicador de progreso, barra de progreso y deslizador) organizados en una cuadrícula (GridPane). Cada control está acompañado por una etiqueta descriptiva. La aplicación se inicia en el método main y configura la ventana con un título y una escena que contiene el GridPane.

package Formulario;

import javafx.application.Application;
import javafx.geometry.Insets;
import javafx.scene.Scene;
import javafx.scene.control.*;
import javafx.scene.layout.ColumnConstraints;
import javafx.scene.layout.GridPane;
import javafx.stage.Stage;

public class AllControls extends Application {

    @Override
    public void start(Stage primaryStage) {
        GridPane gridPane = new GridPane();
        gridPane.setPadding(new Insets(10, 10, 10, 10));
        gridPane.setVgap(10);
        gridPane.setHgap(10);

        ColumnConstraints column1 = new ColumnConstraints();
        column1.setPrefWidth(150);
        gridPane.getColumnConstraints().add(column1);

        Label buttonLabel = new Label("Botón:");
        Button button = new Button("Botón");
        gridPane.add(buttonLabel, 0, 0);
        gridPane.add(button, 1, 0);

        Label checkBoxLabel = new Label("Casilla de verificación:");
        CheckBox checkBox = new CheckBox("Casilla de verificación");
        gridPane.add(checkBoxLabel, 0, 1);
        gridPane.add(checkBox, 1, 1);

        Label hyperlinkLabel = new Label("Hipervínculo:");
        Hyperlink hyperlink = new Hyperlink("Hipervínculo");
        gridPane.add(hyperlinkLabel, 0, 2);
        gridPane.add(hyperlink, 1, 2);

        Label toggleButtonLabel = new Label("Botón de alternancia:");
        ToggleButton toggleButton = new ToggleButton("Botón de alternancia");
        gridPane.add(toggleButtonLabel, 0, 3);
        gridPane.add(toggleButton, 1, 3);

        Label radioButtonLabel = new Label("Botón de radio:");
        RadioButton radioButton = new RadioButton("Botón de radio");
        gridPane.add(radioButtonLabel, 0, 4);
        gridPane.add(radioButton, 1, 4);

        Label labelLabel = new Label("Etiqueta:");
        Label label = new Label("Etiqueta");
        gridPane.add(labelLabel, 0, 5);
        gridPane.add(label, 1, 5);

        Label textFieldLabel = new Label("Campo de texto:");
        TextField textField = new TextField("algún texto...");
        gridPane.add(textFieldLabel, 0, 6);
        gridPane.add(textField, 1, 6);

        Label passwordFieldLabel = new Label("Campo de contraseña:");
        PasswordField passwordField = new PasswordField();
        passwordField.setText("contraseña");
        gridPane.add(passwordFieldLabel, 0, 7);
        gridPane.add(passwordField, 1, 7);

        Label textAreaLabel = new Label("Área de texto:");
        TextArea textArea = new TextArea("Leandro Paúl Muñoz Quinde.");
        textArea.setWrapText(true);
        gridPane.add(textAreaLabel, 0, 8);
        gridPane.add(textArea, 1, 8);

        Label progressIndicatorLabel = new Label("Indicador de progreso:");
        ProgressIndicator progressIndicator = new ProgressIndicator(0.49);
        Label progressIndicatorValue = new Label("49%");
        gridPane.add(progressIndicatorLabel, 0, 9);
        gridPane.add(progressIndicator, 1, 9);
        gridPane.add(progressIndicatorValue, 2, 9);

        Label progressBarLabel = new Label("Barra de progreso:");
        ProgressBar progressBar = new ProgressBar(0.9);
        gridPane.add(progressBarLabel, 0, 10);
        gridPane.add(progressBar, 1, 10);

        Label sliderLabel = new Label("Deslizador:");
        Slider slider = new Slider();
        gridPane.add(sliderLabel, 0, 11);
        gridPane.add(slider, 1, 11);

        Scene scene = new Scene(gridPane, 700, 560);
        primaryStage.setTitle("Todos los Controles");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}


## compilacion
![image](https://github.com/leandro0521/Implementaci-n-de-un-Sistema-de-Men-s-en-una-Aplicaci-n-JavaFX/assets/168586082/4ace6b9e-cfb0-45fc-96e0-2e49dc0518fa)
