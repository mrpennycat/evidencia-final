# evidencia-final
evidencia final del curso java
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
73
74
75
76
77
78
79
80
81
82
83
84
85
86
87
88
89
90
91
92
93
94
95
96
97
98
99
100
101
102
103
104
105
106
107
108
109
110
111
112
113
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
 
public class Consultorio {
 
    /**
     * Metodo utilizado pare leer Strings
     *
     * @param mensaje
     * @return
     */
    public static String leer(String mensaje) {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String s = null;
        try {
            System.out.print(mensaje);
            s = br.readLine();
        } catch (IOException ex) {
            System.out.println("Hubo un error de lectura");
        }
        if (s == null) {
            s = leer(mensaje);
        }
        return s;
    }
 
    /**
     * Metodo utilizado para ller Integers
     *
     * @param mensaje
     * @return
     */
    public static Integer leerInt(String mensaje) {
        Integer i = null;
        try {
            i = Integer.parseInt(leer(mensaje));
        } catch (NumberFormatException ex) {
            System.out.println("Error de formato, vuelva a intentarlo");
        }
        if (i == null) {
            i = leerInt(mensaje);
        }
        return i;
    }
 
    /**
     * Metodo utilizado para leer Doubles
     *
     * @param mensaje
     * @return
     */
    public static Double leerDouble(String mensaje) {
        Double i = null;
        try {
            i = Double.parseDouble(leer(mensaje));
        } catch (NumberFormatException ex) {
            System.out.println("Error de formato, vuelva a intentarlo");
        }
        if (i == null) {
            i = leerDouble(mensaje);
        }
        return i;
    }
 
    public static void main(String[] args) {
        int opcion = -1;
        while (opcion != 7) {
            opcion = leerInt("Seleccione del siguiente menú:"
                    + "\n1.- Alta de médicos"
                    + "\n2.- Alta de Pacientes"
                    + "\n3.- Registro de consulta"
                    + "\n4.- Consulta de médicos"
                    + "\n5.- Consulta de Pacientes"
                    + "\n6.- Consulta de Consultas."
                    + "\n7.- Salir: ");
            switch (opcion) {
                case 1:
                    System.out.println("Alta medica");
                    //Aquí debes programar lo del alta médicos
                    break;
                case 2:
                    System.out.println("Alta pacientes");
                    //Aquí debes programar lo del alta de pacientes
                    break;
                case 3:
                    System.out.println("Registro de consulta");
                    //Aquí debes programar lo del registro de consultas
                    break;
                case 4:
                    System.out.println("Consulta de médicos");
                    //Aquí debes programar lo de la consulta de medicos
                    break;
                case 5:
                    System.out.println("Consulta de pacientes");
                    //Aquí debes programar lo de la consulta de pacientes
                    break;
                case 6:
                    System.out.println("Consulta de consultas");
                    //Aquí debes programar lo de "Consulta de consultas"
                    break;
                case 7:
                    System.out.println("Salir");
                    //Aquí se debe salir del while
                    break;
                default:
                    System.out.println("Opción incorrecta");
                    //Este es un mensaje que se le mostrará al usuario cuando ingrese una opción incorrecta
                    break;
            }
        }
    }
}
