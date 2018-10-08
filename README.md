# hello-world

package nutrientesiv;

import java.util.Scanner;


public class NutrientesIV {



Scanner teclado = new Scanner(System.in);
 String genero;
 double peso;
 double estatura;
 int edad;
 String factorActividad;
 double masa_corporal_magra;
 double indice_grasa;
 double totalKCalDieta;

    public NutrientesIV(String genero, double peso, double estatura, int edad, String factorActividad, double masa_corporal_magra, double indice_grasa, double totalKCalDieta) {
        this.genero = genero;
        this.peso = peso;
        this.estatura = estatura;
        this.edad = edad;
        this.factorActividad = factorActividad;
        this.masa_corporal_magra = masa_corporal_magra;
        this.indice_grasa = indice_grasa;
        this.totalKCalDieta = totalKCalDieta;
    }

    public NutrientesIV() {
         
    }

    public String getGenero() {
        
        do{
        System.out.println("Sos hombre o mujer?");
        genero = teclado.next();
        }while(genero!="H"||genero!="M");
        
        return genero;
    }

    public double getPeso() { 
        do{
        System.out.println("Ingresa tu peso en Kg");
        peso = teclado.nextInt();
        }while(peso<0);
        
         return peso;
    }

    public double getEstatura() {
        do{
        System.out.println("Ingresa tu estatura en metros");
        estatura = teclado.nextInt();
        }while(estatura<0);
        
        return estatura;
    }

    public int getEdad() {
        return edad;
    }

    public String getFactorActividad() {
        return factorActividad;
    }

    public double getMasa_corporal_magra() {
        return masa_corporal_magra;
    }

    public double getIndice_grasa() {
        return indice_grasa;
    }

    public double getTotalKCalDieta() {
        return totalKCalDieta;
    }

    public void setGenero(String genero) {
        this.genero = genero;
    }

    public void setPeso(double peso) {
        this.peso = peso;
    }

    public void setEstatura(double estatura) {
        this.estatura = estatura;
    }

    public void setEdad(int edad) {
        this.edad = edad;
    }

    public void setFactorActividad(String factorActividad) {
        this.factorActividad = factorActividad;
    }

    public void setMasa_corporal_magra(double masa_corporal_magra) {
        this.masa_corporal_magra = masa_corporal_magra;
    }

    public void setIndice_grasa(double indice_grasa) {
        this.indice_grasa = indice_grasa;
    }

    public void setTotalKCalDieta(double totalKCalDieta) {
        this.totalKCalDieta = totalKCalDieta;
    }
 
 
    public static void main(String[] args) {
        // TODO code application logic here
        int form = 0;
        
        System.out.println("Que onda guacho?");
        NutrientesIV usuario1 = new NutrientesIV();
        
        
        usuario1.factoresXActividad();   
        usuario1.getGenero();
        usuario1.getEstatura();
        usuario1.getPeso();
        usuario1.getIndice_grasa();
        
    }          
    
 public void factoresXActividad(){
     int casoActividad=0;

     do{ 
    System.out.println("1) poco o nada ejercicio\n2) ejercicios livianos, deporte 1-3 veces por semana\n3) ejercicio moderado, deporte 3-5 veces por semana\n4) ejercicios intensos, deporte 6-7 días por semana\n5) ejercicios muy intensos, trabajo físico, 2 horas diarias o más de deporte");
    switch(casoActividad){
    case 1: factorActividad = "Sedentario";
    break;
    case 2: factorActividad = "Levemente activo";
    break;
    case 3: factorActividad = "Moderadamente activo";
    break;
    case 4: factorActividad = "Muy_activo";
    break;
    case 5: factorActividad = "Hiperactivo";
    }}while(casoActividad>0 && casoActividad<5);
    
    }
  }

