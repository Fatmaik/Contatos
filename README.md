# Address Book
Agenda de contatos.;

agenda = {}
contato = {}
cadastro = True
c = ""

while cadastro == True: # Enquanto cadastro for verdadeiro progrmama pede novo contato. 
      novo = input("Informe o novo contato: ")

      contato["Nome"] = input("Informe o nome: ")
      contato["Telefone"] = input("Informe o telefone: ")
      contato["Endereço"] = input("Informe o end: ")
      contato["Email"] = input("Informe o email: ")
            
      parar = int(input("Digite (1) para add mais contatos,(2) para consultar contatos ou (0) para fechar o programa : "))
      agenda[novo] = {"Nome":contato["Nome"],"Telefone":contato["Telefone"],"Endereço":contato["Endereço"],"Email":contato["Email"]}

      while cadastro == True:
            if parar == 1:
                  cadastro = True # cadastro falso finaliza o programa
                  break
            elif parar == 2:
                  c = input("Informe qual contato voce deseja obter as informacoes: ")
                  print("Os dados de %s:%s"%(c,agenda[c]))
                  parar = int(input("Digite (1) para add mais contatos,(2) para consultar contatos ou (0) para fechar o programa : "))
            elif parar != 1 and parar != 2:
                  cadastro = False
                  break

while c not in agenda: #Se o contato for informado errado , o prog pedira que digite novamente.
      print("Contato invalido")
      c = input("Informe qual contato voce deseja obter as informacoes: ")
            
print("Os dados de %s:%s"%(c,agenda[c]))
