# game_of_life
bacterial growth simulation with java

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package game_of_life;
//import javax.swing.JOptionPane;
//import java.util.Map
/**
 *
 * @author Michael
 */
import java.io.*;
import java.util.Arrays;
class Game_of_life {
 
    public int[] petri_map(int a, int b) {
        int[] array_map = new int[a];
        array_map[b] = 1;
        return array_map;
    }
     
    public static void main(String args[]) throws IOException {
        Game_of_life mapping = new Game_of_life();
        int a,b;
        BufferedReader din = new BufferedReader(new InputStreamReader(System.in)); //read input from console 1 at a time
        System.out.println("Enter the size of the petri dish, a: ");
        a=Integer.parseInt(din.readLine());
        System.out.println("Enter the position of the cell: ");
        b=Integer.parseInt(din.readLine());
        int[] petri_map_result = mapping.petri_map(a,b);
    System.out.println("The petri dish looks like : "+ Arrays.toString(petri_map_result) );
  }
}



