namespace Application;

public static class Tasks
{
    public static IEnumerable<double> One(int n)
    {
        if (n <= 1)
            throw new ArgumentException($"The {nameof(n)} must be greater than 1.");

        for(var i = 1; i <= n; i++)
        {
            var temp = i + (1.0 / i);

            var current = 1d;
            for (var j = 0; j < i; j++)
                current *= temp;

            yield return current;
        }
    }

    public static void Two(int n)
    {
        if (n <= 0)
            throw new ArgumentException($"The {nameof(n)} must be positive number");

        for(var row = 1; row <= n; row++)
        {
            for(var leftCol = n; leftCol >= 1; leftCol--)
            {
                if (leftCol <= row)
                    Console.Write($"{leftCol} ");
                else
                    Console.Write("  ");
            }
            
            for (var rightCol = 2; rightCol <= n; rightCol++)
            {
                if (rightCol <= row)
                    Console.Write($"{rightCol} ");
                else
                    Console.Write("  ");
            }

            Console.WriteLine();
        }
    }

    public static IEnumerable<int> Three(int n)
    {
        if (n <= 1)
            throw new ArgumentException($"The {nameof(n)} must be a positive number and greater than 1.");

        for(var i = 1; i <= n; i++)
        {
            if(i % 2 == 0 && i % 3 == 0 && i % 5 == 0)
                yield return i;
        }
    }

    public static bool Four(int a, int b)
    {
        if (a <= 0 || b <= 0)
            throw new ArgumentException($"The {nameof(a)} and {nameof(b)} must be positive numbers.");

        var digitsAMultiplication = 1;
        var digitsBAddition = 0;

        while (a > 0)
        {
            digitsAMultiplication *= a % 10;
            a /= 10;
        }

        while (b > 0)
        {
            digitsBAddition += b % 10;
            b /= 10;
        }

        return digitsAMultiplication == digitsBAddition;
    }

    public static int FiveA()
    {
        var sum = 0;

        for(var i = 2; i <= 100; i += 3)
            sum += i;

        return sum;
    }

    public static int FiveB()
    {
        var sum = 0;
        var i = 2;

        while(i <= 100)
        {
            sum += i;
            i += 3;
        }
        
        return sum;
    }

    public static int FiveC()
    {
        var sum = 0;
        int i = 2;

        do
        {
            sum += i;
            i += 3;
        }
        while (i <= 100);

        return sum;
    }

    public static int Six(int start, int end, int n)
    {
        var i = 0;
        var sum = 0;

        var current = start + i * n;
        while((sum + current) < end)
        {
            sum += current;
            i++;

            current = start + i * n;
        }

        return sum;
    }

    public static int Seven(int n)
    {
        if (n <= 0)
            throw new ArgumentException($"The {nameof(n)} must be positive number.");

        var count = 0;

        while (n > 0)
        {
            n /= 10;
            count++;
        }

        return count;
    }

    public static bool Eight(int n)
    {
        if (n <= 0)
            throw new ArgumentException($"The {nameof(n)} must be positive number.");

        var sum = 0;
        while (n > 0)
        {
            sum += n % 10;
            n /= 10;
        }

        return sum % 3 == 0;
    }

    public static bool Nine(int n)
    {
        if (n <= 0)
            throw new ArgumentException($"The {nameof(n)} must be positive number.");

        var digitsCount = Seven(n);

        if (digitsCount % 2 != 0)
            throw new ArgumentException($"The {nameof(n)} must have an even number of digits.");

        var halfDigitsCount = digitsCount / 2;
        var digits = new int[halfDigitsCount * 2];

        for(var i = 0; n > 0; i++)
        {
            digits[i]= n % 10;
            n /= 10;
        }
        
        var sumFirstHalf = 0;
        var sumSecondHalf = 0;

        for(var i = 0; i < halfDigitsCount; i++)
        {
            sumFirstHalf += digits[i];
            sumSecondHalf += digits[digits.Length - 1 - i];
        }

        return sumFirstHalf == sumSecondHalf;
    }

    public static int Ten(int x, int y)
    {
        const int notFoundCode = 0;

        if (x <= 0)
            throw new ArgumentException($"The {nameof(x)} must be positive number.");

        for (var i = 0; x > 0; i++)
        {
            if (y == x % 10)
                return i + 1;
            
            x /= 10;
        }

        return notFoundCode;
    }

    public static void ElevenA()
    {
        const int rows = 7;

        for (var row = 0; row < rows; row++)
        {
            for (var col = 0; col < row + 1; col++)
                Console.Write($"{col + 1} ");

            Console.WriteLine();
        }
    }

    public static void ElevenB()
    {
        const int rows = 7;

        for (var row = rows; row > 0; row--)
        {
            for (var colOne = 0; colOne < rows - row; colOne++)
                Console.Write("  ");

            for (var col = 0; col < row; col++)
                Console.Write($"{col + 1} ");

            Console.WriteLine();
        }
    }

    public static void ElevenC()
    {
        const int maxNumber = 4;

        PrintRow(startRow: 0);

        static void PrintRow(int startRow)
        {
            if (startRow == maxNumber)
                return;

            PrintEmpty(startRow);
            PrintNumbers(startRow + 1);
            PrintEmpty(startRow);

            Console.WriteLine();

            PrintRow(startRow + 1);

            if(startRow + 1 == maxNumber)
                return;

            PrintEmpty(startRow);
            PrintNumbers(startRow + 1);
            PrintEmpty(startRow);

            Console.WriteLine();
        }

        static void PrintEmpty(int currentRow)
        {
            for (var colOne = 0; colOne < currentRow; colOne++)
                Console.Write("  ");
        }

        static void PrintNumbers(int start)
        {
            if (start > maxNumber)
                return;

            Console.Write($"{start} ");

            PrintNumbers(start + 1);

            Console.Write($"{start} ");
        }
    }

    public static int Twelve(int n)
    {
        if (n == 0 || n == 1)
            return n;

        return Twelve(n - 1) + Twelve(n - 2);
    }
}
