static int[] Counting(int[] a)
        {
            //Tim max cua mang a
            int max = -1;
            for ( int i = 0; i < a.Length; i++ )
                if (max < a[i])
                    max = a[i];
            //Khoi tao mang dem gom max + 1 phan tu va cho  tat ca phan tu bang 0
            int[] count = new int[max + 1];
            for (int i = 0; i < count.Length; i++)
                count[i] = 0;
            //Xu ly mang dem de biet so lan xuat hien cac gia tri trong cua mang
            for (int i = 0; i < a.Length; i++)
                count[a[i]]++;
            return count;

        }
        static void InMang(int[]a)
        {
            Console.WriteLine("Mang: ");
            for (int i = 0;i < a.Length;i++)
                Console.Write(a[i] + " ");
            Console.WriteLine();
        }
        static void Main(string[] args)
        {
            int[] a = { 1, 4, 5, 0, 4, 3, 1, 5, 3, 5 };
            int[] c = Counting(a);
            InMang(a);
            InMang(c);
        }
