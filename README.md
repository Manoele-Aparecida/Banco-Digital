# Banco-Digital
# Banco-Digital
# Banco-Digital

private String nome;
private List<Conta> contas;

public String getNome() {
	return nome;
}

public void setNome(String nome) {
	this.nome = nome;
	
}
public class ContaPoupança extends Conta implements ImprimirInformacoesComuns {

public ContaPoupança(Cliente cliente) {
	super(cliente);
	}
@Override
public void imprimirExtrato() {
System.out.println("===Extrato Conta Poupança");
super.imprimirInfosComnuns();
}
}

public class Cliente {

public static Object Manoele;
private String nome;

public String getNome() {
	return nome;
}

public void setNome(String nome) {
	this.nome = nome;
}
}

public List<Conta> getContas() {
	return contas;
}
public class ContaCorrente extends imprimirInfosComnuns {

public ContaCorrente(Cliente string) {
super(string);
}

public ContaCorrente(String string) {
	
}

@Override
public void imprimirExtrato() {
System.out.println("===Extrato Conta Corrente");
super.imprimirInfosComnuns();
}
}

public void sacar(double valor) {
saldo -= valor;

}
@Override
public void depositar(double valor) {
	saldo += valor;
}
@Override
public void tranferir(double valor, Conta contaDestino) {
	this.sacar(valor);
	contaDestino.depositar( valor);
}
public int getAgencia() {
	return agencia;
}
public int getConta() {
	return conta;
}
public double getSaldo() {
	return saldo;
}
public double getPix() {
	return Pix(); 
	}

public void depositar() {
	
}
public void transferir() {
	
}


 protected void imprimirInfosComnuns() {
}
 System.out.println(String.format("Titular: %s", this.cliente.getNome()));
System.out.println(String.format("Agencia: %d", this.agencia));
System.out.println(String.format("Conta: %d",this.conta));
System.out.println(String.format("Saldo: %2f", this.saldo));
}
}

public interface IConta {
public void sacar(double valor);

	public void depositar(double valor) ;  
	
		public void tranferir(double valor, Conta contaDeposito) ;
	
		void imprimirExtrato();
}
