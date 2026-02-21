# Programacion_III

package com.david3.Mavenprueba;

import java.util.ArrayList;
import java.util.Arrays;

@SuppressWarnings("unused")
public class Arraysdemo {
    
    public static void main(String[] args) {
        // 4.1 ¿Cómo se declara un arreglo en Java?

        // Forma 1: Declarar y crear el arreglo
        int[] numeros = new int[5]; // crea un arreglo con 5 posiciones (inicializadas en 0)

        // Forma 2: Declarar e inicializar directamente
        int[] valores = {1, 2, 3, 4, 5}; // el tamaño se define automáticamente

        // Forma 3: Declarar primero y asignar después
        int[] edades;
        edades = new int[]{18, 20, 22}; // inicialización posterior

        // Acceso a elementos
        System.out.println(valores[0]); // muestra el primer elemento → 1

        // 4.2 Métodos y utilidades principales para arreglos

        // Ordenar un arreglo → Arrays.sort()
        int[] datos = {5, 2, 8, 1};
        Arrays.sort(datos); 
        System.out.println(Arrays.toString(datos)); // [1, 2, 5, 8]

        // Buscar un elemento → Arrays.binarySearch()
        int posicion = Arrays.binarySearch(datos, 5);
        System.out.println(posicion); // índice donde se encuentra el 5

        // Copiar un arreglo → Arrays.copyOf()
        int[] copia = Arrays.copyOf(datos, datos.length);

        // Llenar un arreglo → Arrays.fill()
        int[] arreglo = new int[4];
        Arrays.fill(arreglo, 9); 
        System.out.println(Arrays.toString(arreglo)); // [9, 9, 9, 9]

        // Comparar arreglos → Arrays.equals()
        int[] a = {1,2,3};
        int[] b = {1,2,3};
        System.out.println(Arrays.equals(a,b)); // true si son iguales

        // Mostrar contenido → Arrays.toString()
        System.out.println(Arrays.toString(a)); // [1, 2, 3]

        // Usar programación funcional → Arrays.stream()
        // Arrays.stream(a).forEach(System.out::println);

        // 4.3 ¿Cómo se recorren los arreglos en Java?

        // For tradicional
        for (int i = 0; i < valores.length; i++) {
            System.out.println(valores[i]);
        }

        // For-each
        for (int numero : valores) {
            System.out.println(numero);
        }

        // Streams (Java 8+)
        // Arrays.stream(valores).forEach(n -> System.out.println(n));

        // 4.4 Diferencias entre arreglos y ArrayList en Java

        // Arreglos
        int[] numeros1 = {1,2,3};
        System.out.println(numeros1.length); // tamaño fijo

        // ArrayList
        ArrayList<Integer> lista = new ArrayList<>();
        lista.add(10);
        lista.add(20);
        lista.remove(0);
        System.out.println(lista.size()); // tamaño dinámico

        /*
        Diferencias principales:
        Característica   Arreglos   ArrayList
        Tamaño           Fijo       Dinámico
        Tipos            Primitivos y objetos   Solo objetos (Integer, Double, etc.)
        Métodos          Limitados  add(), remove(), size(), contains(), etc.
        Rendimiento      Más rápido Ligeramente más lento
        Memoria          Menor consumo Mayor consumo
        */

        int[] arr = new int[3]; // tamaño fijo
        ArrayList<Integer> list = new ArrayList<>();
        list.add(1); // tamaño crece automáticamente

        int[] arr1 = {1,2,3};          // tipo primitivo
        ArrayList<Integer> list1;      // usa clase envolvente Integer

        /*
        ¿Cuándo usar cada uno?

        ✅ Usa arreglos cuando:
        - El tamaño no cambiará.
        - Necesitas mayor rendimiento.
        - Trabajas con datos primitivos.

        ✅ Usa ArrayList cuando:
        - Necesitas agregar o eliminar elementos.
        - El tamaño puede cambiar.
        - Requieres métodos integrados.
        */
    }
}
