# lista_3

br.com.brunomorais.lista03

1 Exercicio
import java.util.Scanner;

public class Ler_idades_classif {
 public static void main(String[] args) {
 //Ler a idade de uma pessoa e imprimir todas as classificações
 //que se aplicam a ela: 16 anos ou mais pode votar, 18 anos ou
 //mais pode dirigir, 60 anos ou mais é idoso. Uma pessoa de 65
 //anos deve receber as três mensagens.

 Scanner sc = new Scanner(System.in);

 System.out.println("Informe sua a idade: ");
 int idade = sc.nextInt();

 if (idade >= 16) {
 System.out.println("Pode votar");
 }
 if (idade >= 18) {
 System.out.println("Pode dirigir");
 }
 if (idade >= 60) {
 System.out.println("É idoso");

 }
 }
}

2 – Exercicio
import java.util.Scanner;

public class Ler_numero_impri {
 public static void main(String[] args) {
 //2.Ler um número inteiro e imprimir uma linha para cada
 //característica verdadeira: é positivo, é par, é múltiplo de 5, tem
 //dois dígitos.

 Scanner sc = new Scanner(System.in);

 System.out.println("Digite um número inteiro: ");
 int numero = sc.nextInt();

 if (numero > 0) {
 System.out.println("É positivo");
 }
 if (numero % 2 == 0) {
 System.out.println("É par");
 }
 if (numero % 5 == 0) {
 System.out.println("É múltiplo de 5");
 }
 if ((numero >= 10 && numero <= 99) || (numero <= -10 && numero >= -99)) {
 System.out.println("Tem dois dígitos");
 }
 }
}

3 – Exercicio
import java.util.Scanner;

public class Ler_temp_imprimir {
 public static void main(String[] args) {
        //3.Ler a temperatura em graus Celsius e a umidade relativa do
        //ar em porcentagem. Imprimir os alertas

        Scanner sc = new Scanner(System.in);

        System.out.println("Informe a temperatura: ");
        double temperatura = sc.nextDouble();

        System.out.println("Informe a umidade relativa do ar: ");
        double umidade = sc.nextDouble();

        if (temperatura >= 38) {
            System.out.println("Alerta de calor extremo! ");
    }

        if (umidade <= 30) {
            System.out.println("Umidade do ar baixa! ");
    }

        if (temperatura >= 35 && umidade < 20) {
            System.out.println("Alerta de risco de queimada");

        }
    }
}

4 – Exercicio
import java.util.Scanner;

public class Ler_doisnumeroInteiro {
 public static void main(String[] args) {
 //4. Ler dois números inteiros e informar se o primeiro é múltiplo
 //do segundo. Antes de calcular, verificar se o segundo número é
 //zero e, nesse caso, informar que a verificação não pode ser
 //feita.

 Scanner sc = new Scanner(System.in);

 System.out.println("Digite o primeiro numero: ");
 int num1 = sc.nextInt();

 System.out.println("Digite o segundo numero: ");
 int num2 = sc.nextInt();

 if (num2 == 0) {
 System.out.println("A verificação não pode ser feita porque o segundo número é zero.");
 } else {
 if (num1 % num2 == 0) {
 System.out.println(num1 + " é múltiplo de " + num2);
 } else {
 System.out.println(num1 + " não é múltiplo de " + num2);
 }
 }

 }
}

5 – Exercicio
import java.util.Scanner;

public class Ler_AnoBissexto {
 public static void main(String[] args) {
        //5. Ler um ano e informar se ele é bissexto. Um ano é bissexto
        //quando é divisível por 4 e não é divisível por 100, ou quando é
        //divisível por 400.

        Scanner input = new Scanner(System.in);

        System.out.println("Digite o ano de nascimento: ");
        int ano = input.nextInt();

        if ((ano % 4 == 0 && ano % 100 != 0) || (ano % 400 == 0)) {
            System.out.println(ano + " é um ano bissexto.");
        } else {
            System.out.println(ano + " não é um ano bissexto.");
        }
    }
}

6 – Exercicio
import java.util.Scanner;

public class Ler_compras_frete {
 public static void main(String[] args) {
 //6.Ler o valor de uma compra. Compras de 199,00 ou mais têm
 //frete grátis; abaixo disso o frete é 24,90. Imprimir o valor do
 //frete e o total a pagar nos dois casos.

 Scanner sc = new Scanner(System.in);

 System.out.print("Digite o valor da compra: ");
 double valorCompra = sc.nextDouble();

 double frete;

 if (valorCompra >= 199.00) {
 frete = 0.0;
 } else {
 frete = 24.90;
 }

 double totalPagar = valorCompra + frete;

 System.out.printf("Valor do frete: R$ %.2f%n", frete);
 System.out.printf("Total a pagar: R$ %.2f%n", totalPagar);
 }
}

7 – Exercicio
import java.util.Scanner;

public class Ler_Hora_Saudacao {
 public static void main(String[] args) {
 //7. Ler a hora do dia como um inteiro de 0 a 23 e imprimir a
 //saudação correspondente: de 0 a 11 bom dia, de 12 a 17 boa
 //tarde, de 18 a 23 boa noite. Horas fora dessa faixa são
 //inválidas.

 Scanner scanner = new Scanner(System.in);

 System.out.println("Digite que hora é agora: ");
 String entrada = scanner.nextLine();

 try {
            String[] partes = entrada.split(":");
            int hora = Integer.parseInt(partes[0]);
            int minuto = Integer.parseInt(partes[1]);

            if (hora < 0 || hora > 23 || minuto < 0 || minuto > 59) {
                System.out.println("Hora invalida!");

            } else if (hora <= 11) {
                System.out.println("Bom dia Princesa!");

            } else if (hora <= 17) {
                System.out.println("Boa tarde Garota Linda!");

            } else {
                System.out.println("Boa noite Madame!");
            }

        } catch (Exception e) {
            System.out.println("Hora inválida.");
        }
    }
}

8 – Exercicio
import java.util.Scanner;

public class Ler_KM_Infracao {
 public static void main (String[] args) {
 //8. Ler a velocidade máxima da via e a velocidade do veículo.
 //Classificar a infração conforme o Código de Trânsito Brasileiro:
 //dentro do limite não há multa, até 20 por cento acima do limite
 //a infração é média, acima de 20 e até 50 por cento é grave,
 //acima de 50 por cento é gravíssima.

 Scanner sc = new Scanner(System.in);

 System.out.println("Digite a velocidade maxima da via: ");
 double velocidadeMaxima = sc.nextDouble();

 System.out.println("Digite a velocidade detectada do veiculo: ");
 double velocidadeDetectado = sc.nextDouble();

 if (velocidadeDetectado <= velocidadeMaxima) {
 System.out.println("Velocidade permitida. Não há multa!");
 } else {

 double acimaLimite = ((velocidadeDetectado -  velocidadeMaxima) / velocidadeMaxima * 100);
 System.out.printf("O veículo estava %.2f%% acima do limite.%n", acimaLimite);

 if (acimaLimite <= 20.0) {
 System.out.println("Classificação: Infração Média.");
 } else if (acimaLimite <= 50.0) {
 System.out.println("Classificação: Infração Grave.");
 } else {
 System.out.println("Classificação: Infração Gravíssima! Ta pensando que o Brian?");
 }
 }
 }
 }

9 – Exercicio
import java.util.Scanner;

public class Ler_Salario_Bonus {
 public static void main(String[] args) {
 //9. Ler o salário de um funcionário e o tempo de casa em anos.
 //Definir o bônus: menos de 1 ano não recebe, de 1 a 3 anos
 //recebe 5 por cento, acima de 3 e até 10 anos recebe 10 por
 //cento, acima de 10 anos recebe 15 por cento. Imprimir o
 //percentual e o valor do bônus.

 Scanner sc = new Scanner (System.in);

 System.out.println("Me informe seu salario mensal: ");
 double salario = sc.nextDouble();

 System.out.println("Por gentileza me informe quanto tempo de empresa você tem: ");
 double tempo = sc.nextDouble();

 int porcentagemBonus = 0;

 if (tempo < 1) {
 porcentagemBonus = 0;

 } else if (tempo <= 3) {
 porcentagemBonus = 5;

 }  else if (tempo <= 10) {
 porcentagemBonus = 10;

 } else {
 porcentagemBonus = 15;
 }

 double bonus = salario * (porcentagemBonus / 100.0);

 System.out.println("\n===== Holerite do Bônus =====");
 System.out.println("Porcentagem aplicada:" + porcentagemBonus + "%");
 System.out.printf("Valor do Bônus: R$ %.2f%n ", bonus);
 System.out.printf("Total Salario+Bônus: R$ %.2f%n ", (salario + bonus));
 }
}

10 – Exercicio
import java.util.Scanner;

public class Ler_UsuarioSenha {
 public static void main(String[] args) {
 //10. Ler o nome de usuário e a senha. Se o usuário for diferente
 //de admin, imprimir que o usuário não foi encontrado e não
 //verificar a senha. Se o usuário existir, verificar a senha: se for
 //java123, o acesso é liberado; caso contrário, a senha está
 //incorreta. São três saídas diferentes.

 Scanner sc = new Scanner (System.in);

 System.out.println("Digite o login: ");
 String login = sc.nextLine();

 System.out.println("Digite o senha: ");
 String senha = sc.nextLine();

 if (!login.equals("admin")) {
            System.out.print("Usuario não encontrado! ");

        } else {
            if (senha.equals("java123")) {
                System.out.print("Acesso permitido");

            } else {
                System.out.print("Senha incorreta");
            }
        }
    }
}

11 – Exercicio
import java.util.Scanner;

public class Ler_FrequenciaMedia {
 public static void main(String[] args) {
 //11. Ler a frequência em porcentagem e a média final de um
 //aluno. Se a frequência for menor que 75 por cento, o aluno está
 //reprovado por falta e a média não deve ser avaliada. Se a
 //frequência for suficiente, avaliar a média: média >= 7 aprovado,
 //média >= 5 e média < 7 recuperação, média < 5 reprovado por
 //nota.

 Scanner sc = new Scanner (System.in);

 System.out.println("Informe a frequência de presença do aluno: ");
 double frequencia = sc.nextDouble();

 System.out.println("Digite a media semestral do aluno: ");
 double media = sc.nextDouble();

 if (frequencia < 75.0){
 System.out.println("Aluno Reprovado por FALTAS!");

 } else {
 if (media >= 7.0){
 System.out.println("Aluno Aprovado! ");

 } else if (media >= 5.0){
 System.out.println("Aluno em recuperação! ");

 } else {
 System.out.println("Aluno Reprovado por NOTA(media final)! ");
 }
 }
 }
}

12 -Exercicio
package org.example;

import java.sql.SQLOutput;
import java.util.Scanner;

public class Ler_Saldo_Limite {
    public static void main(String[] args) {
        //12. Ler o saldo da conta, o limite diário de saque e o valor
        //solicitado. Se o saldo for menor que o valor, informar saldo
        //insuficiente e não realizar as verificações seguintes. Havendo
        //saldo, verificar o limite: se o valor ultrapassar o limite diário,
        //informar isso; caso contrário, efetuar o saque e imprimir o novo
        //saldo.

        Scanner input = new Scanner(System.in);

        final double LIMITE_DIARIO = 600.00;

        System.out.println("Seu saldo em conta é: ");
        double saldo = input.nextDouble();

        if (saldo >= 5000.00) {
            System.out.println("Ta bem de vida heim Jão, me empresta uns 300 conto? ");
        }

        System.out.println("Digite o valor que deseja sacar: ");
        double valor_sacar = input.nextDouble();

        if (saldo < valor_sacar) {
            System.out.println("Saldo insuficiente. Operação cancelada!");

        }  else {

        if (valor_sacar > LIMITE_DIARIO) {
            System.out.println("Operação não realizada: Valor solicitado maior que o limite! ");

        } else  {
            saldo -= valor_sacar;

            System.out.println("Saque realizado com sucesso!");
            System.out.printf("Saldo atual: R$ %.2f%n ", saldo);
        }
        }

    }
}

13 – Exercicio
package org.example;

import java.util.Scanner;

public class Ler_Double_4option {
    public static void main(String[] args) {
        //13. Ler dois números do tipo double e uma opção de 1 a 4,
        //onde 1 é soma, 2 é subtração, 3 é multiplicação e 4 é divisão.
        //Usar switch para executar a operação escolhida e imprimir o
        //resultado. Qualquer outra opção cai no default como opção
        //inválida. Na divisão, verificar antes se o divisor é zero.

        Scanner input = new Scanner(System.in);
        System.out.println("O boca aberte digite o primeiro numero: ");
        double num1 = input.nextDouble();

        System.out.println("Digite o segundo número: ");
        double num2 = input.nextDouble();

        System.out.println("\n--- Escolha a Operação ---");
        System.out.println("1 - Soma");
        System.out.println("2 - Subtração");
        System.out.println("3 - Multiplicação");
        System.out.println("4 - Divisão");
        System.out.print("Opção: ");

        int opcao = input.nextInt();

        switch (opcao) {
            case 1:
                System.out.printf("Resultado da Soma: %.2f%n", (num1 + num2));
                break;
            case 2:
                System.out.printf("Resultado da Subtração: %.2f%n", (num1 - num2));
                break;
            case 3:
                System.out.printf("Resultado da multiplicação: %.2f%n", (num1 * num2));
                break;
            case 4:
                if (num2 == 0) {
                    System.out.println("Erro: Aprenda de uma vez Jão: Não é possivel dividir por zero! ");
                } else {
                    System.out.printf("Resultado da Divisão: %.2f%n", (num1 / num2));
                }
                break;
               default:
                   System.out.println("Opção invalida!");
            }

        }
    }

14 – Exercicio
package org.example;

import java.util.Scanner;

public class Ler_MesDias {
    public static void main(String[] args) {
        //14. Ler o número de um mês de 1 a 12 e imprimir a quantidade
        //de dias desse mês. Agrupar os meses de mesma duração em
        //um único case, separando os valores por vírgula. Considerar
        //fevereiro com 28 dias. Valores fora da faixa de 1 a 12 devem
        //ser tratados no default.

        Scanner input = new Scanner(System.in);

        System.out.println("Digite um numero do mês(1 a 12): ");
        int mes = input.nextInt();

        switch (mes) {
            case 1, 3, 5, 7, 8, 10, 12:
                System.out.println("Este mês tem 31 dias, se ligou Xomano? ");
                break;

            case 4, 6, 9, 11:
                System.out.println("Este mês tem 30 dias ");
                break;

            case 2:
                System.out.println("Este mês tem 28 dias, é o melhor mês, é carnaval Jão!");
                break;

            default:
                System.out.println("Mês inválido. Digite um numero entre 1 a 12: ");
        }
    }
}

15 – Exercicio
package org.example;

import java.util.Locale;
import java.util.Scanner;

public class Ler_Estac {
    public static void main(String[] args) {
        //15.Estacionamento!

        Scanner scanner = new Scanner(System.in).useLocale(Locale.US);

        System.out.println("--- Terminal de Estacionamento ---");
        System.out.println("1 - Carro\n2 - Moto");
        System.out.println("Escolha o tipo de veículo: ");
        int tipoVeiculo = scanner.nextInt();

        double tarifaPorHora = 0.0;

        switch (tipoVeiculo) {
            case 1:
                System.out.println("Carro.");
                tarifaPorHora = 8.00;
                break;

            case 2:
                System.out.println("Moto.");
                tarifaPorHora = 5.00;
                break;

            default:
                System.out.println("Opção inválida.");
                return;
        }
        System.out.print("Digite a quantidade de horas de permanência: ");
        double horas = scanner.nextDouble();
        double valorFinal = horas * tarifaPorHora;

        scanner.nextLine();
        System.out.print("O cliente possui cupom de desconto? (sim/nao): ");
        String possuiCupom = scanner.nextLine().trim().toLowerCase();

        if (possuiCupom.equals("sim")) {
            if (valorFinal >= 50.00) {
                valorFinal = valorFinal * 0.80;
                System.out.println("Cupom de 20% de desconto aplicado com sucesso!");
            } else {
                System.out.println("O cupom vale apenas para valores acima de R$ 50,00.");
            }
        }
        if (horas > 12) {
            System.out.println("Aviso: Permanência longa.");
        }
        if (horas > 24) {
            System.out.println("Aviso: Cobrança de diária.");
        }
        System.out.print("Classificação da permanência: ");
        if (horas <= 2) {
            System.out.println("Curta.");
        } else if (horas <= 6) {
            System.out.println("Média.");
        } else {
            System.out.println("Longa.");
        }
        System.out.printf("Valor final a pagar: R$ %.2f%n", valorFinal);
    }
}

