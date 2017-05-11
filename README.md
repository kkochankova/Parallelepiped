# Parallelepiped
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace parallelepiped
{
    class Program
    {
        static void Main(string[] args)
        {
            var N = int.Parse(Console.ReadLine());
            Console.Write("+");
            var tilda = N - 2;
            Console.Write(new string('~', tilda));
            Console.Write("+");
            var points = (3 * N + 1) - N;
            Console.WriteLine(new string('.', points));
            var pointsInside = 0;
            for (int i = 0; i < 2 * N + 1; i++)
            {
                Console.Write("|");
                Console.Write(new string('.', pointsInside));
                Console.Write("\\");
                Console.Write(new string('~', tilda));
                Console.Write("\\");
                points--;
                Console.WriteLine(new string('.', points));
                pointsInside++;
            }
            for (int i = 0; i < 2 * N + 1; i++)
            {
                Console.Write(new string('.', points));
                Console.Write("\\");
                pointsInside--;
                Console.Write(new string('.', pointsInside));
                Console.Write("|");
                Console.Write(new string('~', tilda));
                Console.WriteLine("|");
                points++;
            }
            Console.Write(new string('.', points));
            Console.Write("+");
            Console.Write(new string('~', tilda));
            Console.WriteLine("+");
        }
    }
}
