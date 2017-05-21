using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Pipes_in_the_pool
{
    class Program
    {
        static void Main(string[] args)
        {
            int v = int.Parse(Console.ReadLine());
            int p1 = int.Parse(Console.ReadLine());
            int p2 = int.Parse(Console.ReadLine());
            double h = double.Parse(Console.ReadLine());

            p1 = (int)(p1 * h);
            p2 = (int)(p2 * h);

            double fullPool = p1 + p2;

            if (fullPool < v)
            {

                double fullPercentage = (fullPool / v) * 100;
                double p1Percentage = (p1 / fullPool) * 100;
                double p2Percentage = (p2 / fullPool) * 100;
                int a = (int)fullPercentage;
                int b = (int)p1Percentage;
                int c = (int)p2Percentage;

                Console.WriteLine("The pool is {0}% full. Pipe 1: {1}%. Pipe 2: {2}%.", a, b, c);
            }
            else
            {
                double over = fullPool - v;

                Console.WriteLine($"For {h} hours the pool overflows with {over:f1} liters.");
            }
        }
    }
}
