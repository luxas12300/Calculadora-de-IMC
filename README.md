# Calculadora-de-IMC
import java.util.Scanner;

public class Main{

    public static void calculoIMC(float peso, float altura){
        double[] pesosIMC = {18.5,24.9,29.9,39.9,9000};
        String[] classificacao = {"Magreza", "Normal", "Sobrepeso", "Obesidade", "Obesidade Grave"};
        float IMC = peso / (altura * altura);
        System.out.println("O IMC é: " + IMC);

        int i = 0;
        while (IMC > pesosIMC[i]) {i++;}
        System.out.println("A classificação é: "+ classificacao[i]);
    }

    public static void main(String[] args){

            Scanner entrada = new Scanner(System.in);
            String teste = "s";
            while(teste.equals("s")){
                System.out.println("Calcular novo IMC? (s/n)");
                teste = entrada.nextLine();
                if(teste.equals("s")){
                    System.out.println("Entre com o peso em Kg:");
                    float peso = entrada.nextFloat();
                    entrada.nextLine();
                    System.out.println("Entre com a altura em metros:");
                    float altura = entrada.nextFloat();
                    entrada.nextLine();
                    calculoIMC(peso,altura);
                }
            }
    }
}
