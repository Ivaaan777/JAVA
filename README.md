package repass.ud1;

import java.util.Scanner;

public class Ej39 {

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        double AbonoKM, Dietas, sueldoHACIENDA, sueldoIRPF = 0, sueldoFijo = 0.0, kilometraje, comision, ventas, sueldoFINAL;
        int diasDIETAS;

        System.out.println("Introduzca el sueldo del mes");
        sueldoFijo = in.nextDouble();
        System.out.println("Introduzca su kilometraje total SR : ");
        kilometraje = in.nextDouble();
        System.out.println("Dias de dietas, porfavor???");
        diasDIETAS = in.nextInt();
        ventas = sueldoFijo;
        comision = ventas * 0.05;
        AbonoKM = kilometraje * 0.19;
        Dietas = (double) diasDIETAS * 30.0;

        sueldoFINAL = ventas + comision + AbonoKM + Dietas;
        sueldoIRPF = sueldoFINAL * 0.19;

        sueldoHACIENDA = 150;

        sueldoFINAL = sueldoFINAL - sueldoIRPF - sueldoHACIENDA;
        System.out.println(sueldoFINAL);
    }

}