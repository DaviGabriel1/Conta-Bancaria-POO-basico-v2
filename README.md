# Conta Bancária
Este é um projeto de uma conta bancária criado com o objetivo de simular as principais funcionalidades de uma conta corrente ou poupança. Esta é a segunda versão do código, que apresenta correções em relação à primeira versão.

<h2>Funcionalidades</h2>
A classe Conta possui as seguintes funcionalidades:


- Abrir conta: é possível abrir uma conta corrente ou poupança, definindo um saldo inicial de 50 ou 150 reais, respectivamente.
Fechar conta: é possível fechar uma conta somente se não houver débitos ou créditos na conta.
- Depositar: é possível depositar um valor positivo na conta, aumentando o saldo.
- Sacar: é possível sacar um valor da conta, desde que o saldo seja suficiente e o valor não ultrapasse o limite de saque.
- Pagar mensalidade: é possível pagar a mensalidade da conta, que é de 12 reais para conta corrente e 20 reais para conta poupança.

<h2>Correções realizadas na segunda versão</h2>

- Corrigida a lógica de abertura de conta, que estava apresentando erro na definição do tipo de conta

- Corrigido o limite de saque, que estava sendo comparado com o saldo ao invés do atributo "saque".
- Melhorada a lógica de fechamento de conta, adicionando condições que verificam se há débitos ou créditos na conta.
- Adicionada validação para não permitir depósitos com valores nulos ou negativos.
- Melhorada a mensagem de saque sucedido para indicar quando todo o saldo da conta foi sacado e quando o saldo ficou negativo.
- Adicionada função para obter e definir o número da conta.
<h2>Exemplo de uso</h2>
Para utilizar a classe Conta, é possível instanciar um objeto da seguinte forma:

```Conta cliente = new Conta(635352,"cc","Davi",70,true,0);```
Neste exemplo, a conta criada possui número 635352, tipo corrente, nome do dono "Davi", saldo inicial de 70 reais, conta aberta e limite de saque de 0 reais.

É possível realizar operações na conta, como depositar e sacar, e obter informações sobre a conta, como número da conta, tipo, nome do dono, saldo e status.

```cliente.depositar(65.0);
System.out.println("Seu número da conta é: " + cliente.getnumConta());
System.out.println("Seu tipo de conta é: " + cliente.getTipo());
System.out.println("Seu nome na conta é: " + cliente.getDono());
System.out.println("Seu saldo é: " + cliente.getSaldo() + " reais");
System.out.println("Seu status da conta é: " + cliente.getStatus());
cliente.abrirConta("cc");
cliente.sacar(70.0);
```


Este código deposita 65 reais na conta, imprime informações sobre a conta e tenta abrir a conta novamente, mesmo ela já estando aberta. Em seguida, tenta sacar 70 reais da conta, o que não é possível pois o saldo atual da conta é de 135 reais e o limite de saque é de 0 reais.
