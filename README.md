Código feito para estudar sobre Classes em C# 💻

    class Produto
    {
        void Formatacao(string Titulo)
        {
            for (int i = 0; i < Titulo.Length; i++)
            {
                Console.Write('*');
            }

        Console.WriteLine($"\n{Titulo}");

        for (int i = 0; i < Titulo.Length; i++)
        {
            Console.Write('*');
        }
        Console.WriteLine("\n");
    }

    private double price;
    private int Est;

    public string Nome;
    public string Marca;
    public double Preco { get => price;
        set
        {
            if (value > 0)
            {
                price = value;
            }
            else
            {
                Console.Clear();
                Console.WriteLine("Valor Inválido para Preço");
            }
        }
    }
    public int Estoque
    {
        get => Est;
        set
        {
            if (value > 0)
            {
                Est = value;
            }
            else
            {
                Est = 0;
            }
        }
    }

    public void Detalhes()
    {
        Formatacao("Lista de Produtos");
        Console.WriteLine($"Nome: {Nome}");
        Console.WriteLine($"Marca: {Marca}");
        Console.WriteLine($"Estoque: {Estoque}");
        Console.WriteLine($"Preço: {Preco}");
    }
}
