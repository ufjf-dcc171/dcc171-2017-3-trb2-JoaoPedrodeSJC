    Este trabalho visa exemplificar como seria a interface deste programa em uma
mesa específica. Os dados utilizados como exemplo e o número da mesa são passa-
dos pelo contrutor da classe "janelaTrabalho" e tal número pode ser visulizado 
no título da janela. 
    Para realizar este trabalho, fora utilizado listas, Labels, tabela, Jscroll-
Pane, ImageIcons e botões. A janela é dividida por 3 gridLayouts, um no norte, 
um no centro e outro no sul da janela. O grid situado no norte da janela contem 
dois labels, um com o valor fixo "Inicio do atendimento:" e outro que guarda e 
demonstra o horário do inicio do atendimento. O grid do centro é dividido em 
três partes, a do canto esquerdo demonstra duas possíveis listas(lstTipos e 
lstComidas), a do meio demonstra as imagens vinculadas ao produto selecionado e 
a do canto direito demonstra uma tabela(comprados), ambas as listas e a tabela 
também estão contidas em JscrollPanes. O gridlayout da parte inferior guarda os 
botões( selecionar, voltar,adicionar e finalizar) que serão utilizados para 
interagir com a interface. lstTipos e lstComidas possuem um listener cada um, 
estes fazem a a mudança da imagem que é apresentada no centro de acordo com o 
objeto que for selecionado, no momento que o objeto é selecionado, ele obtem o 
mesmo, copia o caminho para a imagem do objeto e cola no label do centro. 
lstTipos guardaos tipos de comidas (ex. bebida, salgado, pizza, etc) quando um 
deles é selecionado e logo o botão "selecionar" é apertado, o listener do botão 
"pressionar" troca a Jscrollpane "westPane", que contém a lista lstTipos, pelo 
JScroolPane westPane2 que possui a lista lstComidas que está vinculada ao objeto
 que foi selecionado no lstTipos e troca o gridlayout pane "botoes", que possui 
os botões "selecionar" e "finalizar" pelo gridlayout pane "botoes2", que possui 
os botões "adicionar" e "voltar". "voltar" realiza o mesmo processo que selecio-
nar, no entanto faz a troca inversa. "adicionar" adiciona o objeto selecionado 
na "lstComidas" à tabela do lado direito do painel e o seu preço à variável 
"valor", que é a variável que guarda o total da transação demonstrado na tabela 
e, caso seja o primeiro objeto da transação, ele também seta o valor da variável
 "inicio" para o horário atual do sistema. finalizar reseta o valor das variá-
veis "inicio" e "valor", limpa a tabela de objetos comprados  e, como também, 
demonstra o horário em que o atendimento foi finalizado.
    Uma interface para o atendente foi adicionada, nela o atendente pode fechar
os pedidos e remover items dos pedidos que ainda estão abertos, uma interface 
para fazer a seleção entre interface atendente e interface cliente também foi 
adicionada.
    A persistência dos dados está em todas as interfaces, na janelaTrabalho o 
actionlistener do botão finalizar salva os pedidos da mesa no arquivo de mesmo
número, na selecionaInterface, o actionlistener do botão "adicionar mesa" aumen-
ta a quantidade de mesas no arquivo mesas e o botão "remover mesa" diminui. Na 
"interfaceAtendente", o actionlistener do combobox das mesas faz o upload dos
pedidos da mesa de acordo com qual mesa está selecionada, ele pega o valor sele-
cionado do combobox e abri o arquivo com nome igual ao valor, os outros botões
(fechar e remover) realizam a mesma operação de persistência, que é sobrescrever
 os dados do arquivo, com nome igual ao valor selecionado no combobox e, com os
dados da tabela. 

Aluno:João Pedro de Souza Jardim da Costa matrícula: 201576044
 Curso: Sistemas de Informação