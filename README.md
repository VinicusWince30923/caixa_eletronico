<!DOCTYPE html>
<html>
<body>

<h1>Gerenciador de Conta Bancária</h1>

<h2>Código ainda em desenvolvimento</h2>

<p>Este repositório contém um script Python para gerenciar uma conta bancária. O script permite realizar operações de saque e depósito, e exibe o saldo da conta e da carteira após cada operação.</p>

<h2>Código do Projeto</h2>
<pre>
<code>

print("Bem-vindo ao seu banco! Aqui você pode sacar ou depositar seu dinheiro.")


def dados():
    return float(500) , float(500)

def sacar():
    print("Insira o valor que deseja sacar")
    saque = float(input("Insir o valor a ser sacado."))
    return saque

def depositar():
    print("Insira o valor que deseja depositar.")
    deposito = float(input("Insira o valor a ser depositado."))
    return deposito
    
def verificar_saque(saque , carteira , conta):

    if saque <= conta:
        carteira += saque
        conta -= saque
        print(f"Você sacou R${saque:.2f} e agora tem R${conta:.2f} na sua conta. Você tem $R{carteira:.2f} em sua carteira.")

    else:
        print("Você não tem essa quantia na conta. Insira outro valor.")
        
    return carteira , conta
        
        
def verifcar_deposito(deposito , carteira , conta):
    
    print(f"Você tem R${carteira} em sua carteira e R${conta} em sua conta.")
    
    if deposito <= carteira:
        conta += deposito
        carteira -= deposito
        print(f"Você depositou R${deposito:.2f}, agora você tem R${conta:.2f} em sua conta. Você tem R${carteira:.2f} em sua carteira")
    
    else:
        print(f"Você não tem essa quantidade em sua carteira. Você tem R${carteira:.2f} em sua carteira.")
        
    return carteira , conta
    
    
carteira , conta = dados()
        
        
while True:
        
    print("Escolha qual operação deseja fazer.")  
    print("1. Sacar.")
    print("2. Depositar.")
    print("3. Sair.")
    
    escolha = str(input("Insira a operação desejada."))
    
    if escolha == "1":
            
        saque = sacar()
        carteira, conta = verificar_saque(saque , carteira , conta)
        
    elif escolha == "2":
        
        deposito = depositar()
        carteira , conta = verifcar_deposito(deposito , carteira , conta) 

    elif escolha == "3":
    print("Obrigado por utilizar nosso banco.")
        break
    
    else:
        print("Insira um valor válido.")
        
    

</code>
</pre>

<h2>Estrutura do Código</h2>

<p>O código está organizado para gerenciar uma conta bancária, permitindo operações de saque e depósito, e exibindo o saldo atualizado após cada operação.</p>

<h3>Lista de Funções</h3>
<ul>
    <li><strong>dados()</strong>
        <ul>
            <li>Inicializa e retorna os valores de carteira e conta.</li>
        </ul>
    </li>
    <li><strong>sacar()</strong>
        <ul>
            <li>Solicita ao usuário o valor a ser sacado e o retorna.</li>
        </ul>
    </li>
    <li><strong>depositar()</strong>
        <ul>
            <li>Solicita ao usuário o valor a ser depositado e o retorna.</li>
        </ul>
    </li>
    <li><strong>verificar_saque(saque, carteira, conta)</strong>
        <ul>
            <li>Verifica se o valor do saque é menor ou igual ao saldo da conta.</li>
            <li>Atualiza e retorna os valores da carteira e conta após o saque.</li>
        </ul>
    </li>
    <li><strong>verificar_deposito(deposito, carteira, conta)</strong>
        <ul>
            <li>Verifica se o valor do depósito é menor ou igual ao saldo da carteira.</li>
            <li>Atualiza e retorna os valores da carteira e conta após o depósito.</li>
        </ul>
    </li>
</ul>

<h2>Requisitos do Sistema</h2>
<p>Para rodar a aplicação, são necessários os seguintes requisitos do sistema:</p>
<ul>
    <li><strong>Sistema Operacional:</strong> Windows 7 ou superior, macOS 10.13 ou superior, ou distribuições Linux modernas.</li>
    <li><strong>Python:</strong> Python 3.6 ou superior.</li>
</ul>

<h2>Execução</h2>
<p>Para executar o script de gerenciamento de conta bancária utilizando o Visual Studio Code (VSCode), siga os passos abaixo:</p>
<ol>
    <li>Abra o Visual Studio Code.</li>
    <li>Certifique-se de que a extensão do Python está instalada no VSCode. Caso não esteja, você pode instalá-la a partir da aba de extensões.</li>
    <li>Baixe o script Python do repositório e salve-o em um diretório de sua escolha.</li>
    <li>No VSCode, clique em <strong>File</strong> > <strong>Open Folder</strong> e navegue até o diretório onde o script foi salvo. Abra esse diretório.</li> 
    <li>Clique duas vezes no arquivo do script para abri-lo no editor.</li>
    <li>Com o arquivo aberto, clique no botão "Run" no canto superior direito (Símbolo de "Play") ou pressione <code>F5</code> para executar o script.</li>
</ol>

<h2>Exemplo de Uso</h2>
<ol>
    <li>O usuário será saudado com uma mensagem de boas-vindas ao gerenciador de conta bancária.</li>
    <li>O usuário será solicitado a inserir o valor para saque ou depósito.</li>
    <li>Após cada operação, o saldo da conta e da carteira será exibido.</li>
    <li>O usuário pode continuar realizando operações até decidir sair, digitando '3'.</li>
    <li>Ao finalizar, o programa exibirá uma mensagem de agradecimento e encerrará.</li>
</ol>

<h2>Contribuição</h2>
<p>Se você quiser contribuir para este projeto, sinta-se à vontade para abrir um pull request ou relatar problemas no repositório.</p>

</body>
</html>
