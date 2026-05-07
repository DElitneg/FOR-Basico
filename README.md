# FOR/SWITCH-Basico
Switch / Contador / Acumulador / FOR - Basico



// 6. Menú de Restaurante

using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {

            Console.WriteLine("Menu:");
            Console.WriteLine("(S). Sandwich:");
            Console.WriteLine("(P). Pizza:");
            Console.WriteLine("(H). Hamburguesa:");

            String opcion;
            opcion = Convert.ToString(Console.ReadLine());

            switch (opcion)
            {
                case "S" : Console.WriteLine("El precio de un Sandiwch es de 1000$ pesos");
                        break;

                case "P":
                    Console.WriteLine("El precio de una pizza es de 5000$ pesos");
                    break;

                case "H": Console.WriteLine("El precio de una hamburguesa es de 2500$ pesos");
                    break;

                default: Console.WriteLine("Producto no encontrado");
                    break;

            }

        }
    }
}

// 7. Selector de Idioma

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {

            Console.WriteLine("Seleccion de idioma:");
            Console.WriteLine("1. Ingles");
            Console.WriteLine("2. Frances ");
            Console.WriteLine("3. Aleman ");

            int opcion;
            opcion = int.Parse(Console.ReadLine());

            switch (opcion)
            {
                case 1 : Console.WriteLine("Hello! Greetings!");
                        break;

                case 2:
                    Console.WriteLine("Salut! Bonjour!");
                    break;

                case 3: Console.WriteLine("Hallo!   ");
                    break;

                default: Console.WriteLine("???");
                    break;

            }

        }
    }
}

// 8. Registro de Temperaturas

using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            int opcion;
            int acumulado;
            int contador;
            contador = 0;
            opcion = 0;
            acumulado = 0;
            int dias;
            dias = 0;

            Console.WriteLine("Reporte del clima semanal:");


            for (int i = 1; i<=7; i++)
            {
                Console.WriteLine("Temperatura del dia" + dias);
                opcion = int.Parse(Console.ReadLine());
                acumulado = acumulado + opcion;
                dias = dias + 1;
                if (opcion < 0)
                {
                    contador = contador + 1;
                }               
            }

            Console.WriteLine("En total en la semana hubo (?) " + acumulado+" grados acumulados y "+contador+" veces menor a 0 grados");
        }
    }
}

// 9. Gestión de Gastos

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            int opcion;
            int acumulado;
            int contador;
            contador = 0;
            opcion = 0;
            acumulado = 0;

            Console.WriteLine("5 Gastos del dia:");


            for (int i = 1; i<=5; i++)
            {
                Console.WriteLine("");
                opcion = int.Parse(Console.ReadLine());
                acumulado = acumulado + opcion;
                if (opcion > 500)
                {
                    contador = contador + 1;
                }               
            }
            Console.WriteLine("Gasto total: "+acumulado+"$, "+contador+" gastos de mas de 500$ pesos");
        }
    }
}

// 10. Análisis de Primalidad

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            int opcion;
            int contador;
            int noPrimos;
            contador = 0;
            noPrimos = 0;

            Console.WriteLine("Introduzca un numero entero positivo:");

            opcion = Convert.ToInt32(Console.ReadLine());

            for (int i = 1; i<opcion; i++)
            {
                contador = contador + 1;
                if (opcion%contador == 0)
                {
                    noPrimos = noPrimos + 1;
                    Console.WriteLine("Es divisible por " + contador);
                }               
            }

            if(noPrimos == 1)
            {
                Console.WriteLine(opcion+" Es primo");
            }
            else
            {
                Console.WriteLine("El numero no es primo, se puede dividir por " + noPrimos + " numeros");
            }
            

            Console.ReadKey();
            
        }
    }
}

