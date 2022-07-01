# SIlvestre
Compra e venda de passagens
print("-----------------------------------------")
print('Silvestre Turismo!\n')
print('Conectamos voçê ao seu proximo destino!\n')
print("-----------------------------------------")
print('Numero para contato: 83 8127-0228')
print('-----------------------------------')
print('''Escolha uma linha para seu destino:
[ 1 ] João Pessoa - PB
[ 2 ] Natal - RN
[ 3 ] Fortaleza - CE
[ 4 ] Recife - PE
[ 5 ] Salvador - BA ''')
print('-------------------')

poltronasVagas =[45,45,45,45,45]
quantidadelinhas = len (poltronasVagas)
for linha,poltronasDisponiveis in enumerate (poltronasVagas):
    print("Linha %d possui %d poltronas vagas: onibus (g7 1200)\n"% (linha+1,poltronasDisponiveis))


while True:
    linhaEscolhida = int(input("Escolha uma linha de 1 %d (para sair digite 0)" % quantidadelinhas))
    if linhaEscolhida == 0:
        print("Sistema Finalizado:\n")
        break
    if linhaEscolhida > quantidadelinhas or linhaEscolhida < 1:
        print("Linha invalida:\n")

    elif poltronasVagas[linhaEscolhida -1] == 0:
        print("Linha com vagas indisponiveis\n")

    else:
        quantidadePassagens=int(input("Reserve suas poltonas:(%d poltronas disponiveis\n)"% poltronasVagas[linhaEscolhida -1]))
        if quantidadePassagens > poltronasVagas[linhaEscolhida -1]:
            print("Voce escolheu um quantidade maior do que poltonas disponiveis\n")
        elif quantidadePassagens < 1:
            print("Escolhar a quantidade correta de poltronas no maximo 3\n")
        else:
            poltronasVagas[linhaEscolhida -1] -= quantidadePassagens
            print('-----------------------------------------------')


            for linha,poltronasDisponiveis in enumerate(poltronasVagas):
                print("Linha %d possui %d poltronas vagas\n" % (linha+1,poltronasDisponiveis))
                print('-----------------------------------')
                linhaEscolhida = int(input("Escolha uma linha de 1 %d (para sair digite 0)" % quantidadelinhas))
                if linhaEscolhida == 0:
                    print("Sistema Finalizado:\n")
                    break
                if linhaEscolhida > quantidadelinhas or linhaEscolhida < 1:
                    print("Linha invalida:\n")

                elif poltronasVagas[linhaEscolhida -1] == 0:
                    print("Linha com vagas indisponiveis\n")

                else:
                    quantidadePassagens=int(input("Reserve suas poltonas:(%d poltronas disponiveis\n)"% poltronasVagas[linhaEscolhida -1]))
                    if quantidadePassagens > poltronasVagas[linhaEscolhida -1]:
                        print("Voce escolheu um quantidade maior do que poltonas disponiveis\n")
                    elif quantidadePassagens < 1:
                        print("Escolhar a quantidade correta de poltronas no maximo 3\n")
                    else:
                        poltronasVagas[linhaEscolhida -1] -= quantidadePassagens
                        print('-----------------------------------------------')
                import calendar
                c = calendar.TextCalendar(calendar.SUNDAY)
                str = c.formatmonth(2021,10)
                print(str)

                print('----------------------------------')
                print('Datas disponíveis para sua viagem:')


                from datetime import datetime
                data_da_viagem = 'dd/mm/aaaa'
                data = input('Digite a data de embarque na forma dd/mm/aaaa:\n')

                print("---------------------")
                print("Destinos disponiveis:")
                print("---------------------")
                print('--------------------------------------------')
                print("Joao pessoa (PB)")
                print("\linha 1 via BR-101\ onibus (g7 1200)")
                print('Horarios de saida(06.00)horas & (13.00)horas')
                print('--------------------------------------------')
                print('Natal (RN)')
                print('\linha 2\ via BR-101 onibus (g7 1200)')
                print('Horarios de saida(09.00)horas & (14.00)horas')
                print('--------------------------------------------')
                print('Fortaleza (CE)')
                print('\linha 3 via BR-101\ onibus (g7 1200) leito')
                print('Horarios de saida(10.00)horas & (15.00)horas')
                print('--------------------------------------------')
                print('Recife (PE)')
                print(' \linha 4 via BR-101\ onibus (g7 1200)')
                print('Horarios de saida(11.00)horas & (16.00)horas')
                print('--------------------------------------------')
                print('Salvador (BA)')
                print('\linha 5 via BR-101\ onibus (g7 1200) leito')
                print('Horarios de saida(12.00)horas & (17.00)horas')
                print('-----------------------------------------------')
                print('De segunda a sabado dois horarios por linha, já nos domingos so um horario extra por linha na parte da manha; ')
                print('-------------------------------------------------------------------------------------------------------------')
                print('Atenção será cobrada um tarifa extra de 10% em cima das passagens nos finais de semana;')
                print('------------------------------------------------------------------------------------')
                opcao = (input('Selecione um destino:'))
                horario =(input('Digite o horario que escolheu\n :'))
                passagem = int(input('Digite a quantidade de passagem desejada:\n'))
                while passagem > 3:
                 passagem = int(input('Número invalido. Digite quantidade menor ou igual a três:\n'))







                print('-----------------')
                print('Joao pessoa (PB):')
                print('Valor da tarifa R$33.60:')
                print('------------------------')
                print('----------')
                print('Natal (RN)')
                print(' Valor da tarifa R$60.70:')
                print('-------------------------')
                print('---------------')
                print(' Fortaleza (CE):')
                print('Valor da tarifa R$176.70:')
                print('-------------------------')
                print('------------')
                print('Recife (PE):')
                print('Valor da tarifa R$70.70:')
                print('------------------------')
                print('--------------')
                print('Salvador (BA):')
                print('Valor da tarifa R$ 291.30')
                print('-------------------------')

                Valor =float(input('Digite o valor referente  a seu destino'))
                print(Valor)
                valor_total = Valor * passagem
                print("valor total das passagens é de R$\n{:.2f}".format(valor_total))
                nome =input('Digite seu nome completo: ')
                CPF = int(input('Digite seu CPF:\n'))

                codigo = CPF * 5



                print("---------------------------------------------")
                print("--Nome completo:\n","_",nome,":")
                print("---------------------------------------------")
                print("--Numero do CPF:\n","_",CPF,":")
                print("----------------------------------------------")
                print("--Codigo da passagem:\n","_",codigo,":" )
                print("----------------------------------------------")
                print("--Horario da viagem:\n" "_",horario,'Horas')
                print("----------------------------------------------")
                print("--Destino:\n""___Cidade:",opcao)
                print("------------------------------")
                print("--Dia da sua viagem:",data)
                print("--------------------------")
                print("------------------------------------------------------")
                print("--valor total das passagens:\n","___R$",valor_total,":")
                print("----------------------------------------------")
                print("Compra das passagens finalizada com sucesso:\n")
                print("----------------------------------------------")
                print("Olá, voce que imprimir a segunda via da sua passagem ?")
                print('------------------------------------------------------')

                while True :
                    resp = input("Digite sim para imprimir e nao para nao imprimir ! ")
                    if resp == 'sim' or resp == 's' or resp == 'yes':
                        print('Certo, vou imprimir sua segunda via.')
                        print("---------------------------------------------")
                        print("--Nome completo:\n","_",nome,":")
                        print("---------------------------------------------")
                        print("--Numero do CPF:\n","_",CPF,":")
                        print("----------------------------------------------")
                        print("--Codigo da passagem:\n","_",codigo,":" )
                        print("----------------------------------------------")
                        print("--Horario da viagem:\n" "_",horario,'Horas')
                        print("----------------------------------------------")
                        print("--Destino:\n""___Cidade:",opcao)
                        print("------------------------------")
                        print("--Dia da sua viagem:",data)
                        print("--------------------------")
                        print("------------------------------------------------------")
                        print("--valor total das passagens:\n","___R$",valor_total,":")
                        print("----------------------------------------------")
                        print("Segunda via imprimida com sucesso:\n")
                        print("------------------------------------")
                        break


                    elif resp == 'não' or resp == 'n' or resp == 'no':
                        print('------------')
                        print('ok entendemos')
                        print('------------')
                        break


                    else:
                        print('---------------------')
                        print("Use sim ou não apenas")
                        pass
