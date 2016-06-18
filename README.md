# Contatos
Agenda de contatos.;

agenda = {}
contato = {}
cadastro = True

while cadastro == True: # Enquanto cadastro for verdadeiro progrmama pede novo contato. 
      novo = input("Informe o novo contato: ")

      contato["Nome"] = input("Informe o nome: ")
      contato["Telefone"] = input("Informe o telefone: ")
      contato["Endereço"] = input("Informe o end: ")
      contato["Email"] = input("Informe o email: ")
            
      parar = input("Digite (sair) para fechar o programa : ")
      agenda[novo] = {"Nome":contato["Nome"],"Telefone":contato["Telefone"],"Endereço":contato["Endereço"],"Email":contato["Email"]}

      if parar == "sair":
            cadastro = False # cadastro falso finaliza o programa
            break

c = input("Informe qual contato voce deseja obter as informacoes: ")
while c not in agenda: #Se o contato for informado errado , o prog pedira que digite novamente.
      print("Contato invalido")
      c = input("Informe qual contato voce deseja obter as informacoes: ")
            
print("Os dados de %s:%s"%(c,agenda[c]))

