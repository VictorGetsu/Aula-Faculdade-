# Aula-Faculdade-
Este é um codigo que estou fazendo em sala de aula
Não tem muito segredo, este é um trabalho que estou fazendo em sala de aula, sou aluno do segundo periodo de ADS 

using System;
					
public class Program
		{
	public static void Main()
		{
		
		//  Declaração de variáveis.
		
		double np1,np2,pim,media,soma=0,maiornota=0,menornota=10,aprovado=0,reprovado=0,qtimaior=0,qtimenor=0;
		string nome;
		int i,n;
		
		Console.WriteLine("Quantos alunos serão avaliados? ");
		n = Convert.ToInt16(Console.ReadLine());
		
		// Ínicio do for.
		
		for (i=0; i<n; i++)
		{
			
		Console.WriteLine("Qual o seu nome? ");
		nome = Console.ReadLine();
		Console.WriteLine("Qual foi sua nota da NP1? ");
		np1 = Convert.ToDouble(Console.ReadLine());
		
		Console.WriteLine("Qual foi sua nota da NP2? ");
		np2 = Convert.ToDouble(Console.ReadLine());
		
		Console.WriteLine("Qual foi sua nota do PIM? ");
		pim = Convert.ToDouble(Console.ReadLine());
		
		media = (np1 + np2)/2 *0.8 + pim * 0.2;
		
		Console.Write(nome+" sua média é "+media);
			
		soma+=media;
			
		 // Verificar aprovação do aluno.
			
		if (media>=7)
			
		{
		Console.WriteLine(" e você foi aprovado");
			aprovado= aprovado+1;
		}
		else
		{
		Console.WriteLine(" e você foi reprovado");
			reprovado=reprovado+1;
		}
			
		// Verificar maior nota.
			
		if (media>maiornota)
		{
			maiornota=media;
			qtimaior=qtimaior+1;
		}
		if (media<menornota)
			
		{
		menornota=media;
		qtimenor=qtimenor+1;
		}
	}   
	    // Final do for.
		
		soma=soma/i;
		
		// Verificar média da sala.
		
		if (soma>7)
		{
		Console.WriteLine("A sala esta acima da média, nota"+soma);
		}
		else if (soma==7)
		{
		Console.WriteLine("A sala esta na média, "+soma);	
		}
		
		else
		{
		Console.WriteLine("A sala não atingiu a média desejada, nota "+soma);
		}
		Console.WriteLine("------------------------");
		Console.WriteLine("A menor nota entre os alunos é: "+menornota); Console.WriteLine("Alunos com a menor nota: "+qtimenor);
		Console.WriteLine("A maior nota entre os alunos é: "+maiornota); Console.WriteLine("Alunos com a maior nota: "+qtimaior);
		Console.WriteLine("Alunos aprovados: "+aprovado);
		Console.WriteLine("Alunos reprovados: "+reprovado);
		Console.WriteLine("------------------------");
		
		}  
	}  // Chaves do final do programa.
