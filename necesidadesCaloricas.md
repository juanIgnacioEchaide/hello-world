
package nutrientesiv;


public class necesidadesCaloricas extends NutrientesIV{

    double MB;  
    
    

    public necesidadesCaloricas(double MB, String genero, double peso, double estatura, int edad, String factorActividad, double masa_corporal_magra, double indice_grasa, double totalKCalDieta) {
        super(genero, peso, estatura, edad, factorActividad, masa_corporal_magra, indice_grasa, totalKCalDieta);
        this.MB = MB;
    }

   
    public double getMB() {
        return MB;
        
    }

}


class metabolismoBasal extends necesidadesCaloricas{
 
   
    public metabolismoBasal(java.lang.Double MB, String genero, double peso, double estatura, int edad, String factorActividad, double masa_corporal_magra, double indice_grasa, double totalKCalDieta) {
        super(MB, genero, peso, estatura, edad, factorActividad, masa_corporal_magra, indice_grasa, totalKCalDieta);
    
    }

       
    public void formulaBasica(){ 
     // MB Hombre: 1 caloría x peso en Kg. x 24 Horas MB Mujer: 0,9 calorías x peso en Kg. x 24 Horas  

    }
    
    public void HarrisBenedict(){    
        /*MB Hombre: 66,473 + (13,751 x peso en kg) + (5,0033 x estatura en cm) - (6,7550 x edad en años) 
        
        MB Mujer: 655,1 + (9,463 x peso en kg) + (1,8 x estatura en cm) - (4,6756 x edad en años) Ejemplo B: 66,473 + (13,751 x 85) + (5,0033 x 180) - (6,55 x 30) = 1933,30 kcal 
                */
    }

    public void KatchMcArdle(){ 
        /*MB: 370 + (21.6 x masa corporal magra en Kg.) Ejemplo C: 370 + (21.6 x (85 x 0,86) = 1948,96 kcal*/
    }
}

class requerimientoCalorico extends necesidadesCaloricas {

    public requerimientoCalorico(double MB, String genero, double peso, double estatura, int edad, String factorActividad, double masa_corporal_magra, double indice_grasa, double totalKCalDieta) {
        super(MB, genero, peso, estatura, edad, factorActividad, masa_corporal_magra, indice_grasa, totalKCalDieta);
    }

    public void calcularRequerimientoCalorico(){
  /*Sedentario (poco o nada ejercicio): MB x 1,2
    Levemente activo (ejercicios livianos, deporte 1-3 veces por semana): MB x1.375
    Moderadamente activo (ejercicio moderado, deporte 3-5 veces por semana): MB x 1,55
    Muy activo (ejercicios intensos, deporte 6-7 días por semana) MB x 1,725
    Hiperactivo (ejercicios muy intensos, trabajo físico, 2 horas diarias o más de deporte): MB x 1.9 actividad ligera*/
  
        /*Ejemplo A: 2040 x 1.55 = 3162 Kcal Ejemplo B: 1933,30 x 1.55 = 2996,62 Kcal Ejemplo C: 1948,96 x 1.55 = 3020,88 Kcal*/
  
    }
}
