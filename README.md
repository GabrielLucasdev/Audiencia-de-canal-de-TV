    import java.util.Scanner;
    public class Main {
        public static void main(String[] args) {
            Scanner scan = new Scanner(System.in);
    
            int totalDePessoas = 0;
            int canal4 = 0, canal5 = 0, canal7 = 0, canal12 = 0;
            while (true) {
                
                // Solicita ao usuário que insira o número do canal
                System.out.print("Número do canal que está assistindo (4, 5, 7, 12): ");
                int canal = scan.nextInt();
                
                // Verifica se o usuário quer encerrar o programa
                if (canal == 0) {
                    System.out.println("PROGRAMA ENCERRADO");
                    break;
                    
                // Verifica se o número do canal é inválido
                }
                if (canal != 4 && canal != 5 && canal != 7 && canal != 12) {
                    System.out.println("OPÇÃO INVALIDA");
                    continue;
                }
                
                System.out.print("Número de pessoas assistindo: ");
                int pessoasAssistindo = scan.nextInt();
    
                totalDePessoas += pessoasAssistindo;
                switch (canal) {
                    case 4:
                        canal4 += pessoasAssistindo;
                        break;
                    case 5:
                        canal5 += pessoasAssistindo;
                        break;
                    case 7:
                        canal7 += pessoasAssistindo;
                        break;
                    case 12:
                        canal12 += pessoasAssistindo;
                        break;
                }
    
            }
            System.out.println("O PERCENTUAL DE PESSOAS ASSISTINDO CADA CANAL");
            if (totalDePessoas > 0) {
                System.out.println("Canal 4: " + ((double)canal4 / totalDePessoas * 100) + "%");
                System.out.println("Canal 5: " + ((double)canal5 / totalDePessoas * 100) + "%");
                System.out.println("Canal 7: " + ((double)canal7 / totalDePessoas * 100) + "%");
                System.out.println("Canal 12: " + ((double)canal12 / totalDePessoas * 100) + "%");
            } else {
                System.out.println("Nenhuma pessoa está assistindo");
            scan.close();
            }
        }
    }
