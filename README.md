Teaching Fashion

A program to be able to help users be able to dress easier and more effortlessly with the help of an algorithm
to provide the user with options to choose between style and outfits and looking their best constantly. 
There are no doubts people want to always look the best, whether its for a presentation, special occasion, etc. 
In real life, people just don't have the time to accomplish it, the mindset, or the knowledge. This shuld help and make imagination flow.

A program that gives users a simple yet intuitive easy interface to look their sharpest and happiest while making it easy to style their life and clothing.

Week 1- understand how to use Git more fluidly.

(which algorithms and code works most efficiently to decipher and understand the task of exctacting key patterns of clothing and making
the process as easy and simple and intuitive)






Hiroshi Irizarry
Cara Sweeney



package application;
	
import javafx.application.Application;
import javafx.geometry.Insets;
import javafx.geometry.Pos;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.layout.HBox;
import javafx.scene.layout.VBox;
import javafx.scene.paint.Color;
import javafx.scene.shape.Circle;


public class Main extends Application {
	public static void main(String[] args) {
		launch(args);
	}
	
	@Override
	public void start(Stage primaryStage) throws Exception {
		VBox vb = new VBox();
		vb.setAlignment(Pos.CENTER);
		//create circle
		Circle c = new Circle(10);
		c.setStroke(Color.BLACK);
		c.setFill(Color.BLUE);
		
		vb. getChildren().add(c);
		
		//create 2 buttons
		HBox hb = new HBox();
		
		Button grow = new Button("Grow");
		grow.setOnAction(e -> {
			c.setRadius(c.getRadius() + 5);
		});
		
		Button shrink = new Button("Shrink");
		shrink.setOnAction(e -> {
			c.setRadius(c.getRadius() - 5);
		});
		
		Button green = new Button("Green");
		green.setOnAction(e -> {
		c.setStroke(Color.GREEN);
		c.setFill(Color.GREEN);
		});
		
		Button red = new Button("Red");
		red.setOnAction(e -> {
		c.setStroke(Color.RED);
		c.setFill(Color.RED);
		});
		
		hb.getChildren().addAll(grow, shrink, green, red);
		hb.setSpacing(15);
		hb.setAlignment(Pos.CENTER);
		hb.setPadding(new Insets(15));
		
		vb.getChildren().add(hb);
		
		
		primaryStage.setTitle("Circle");
		primaryStage.setScene(new Scene(vb, 200, 200));
		primaryStage.show();
		
		
		
		
		
	}
	
}