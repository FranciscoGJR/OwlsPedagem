# OwlsPedagem
Exercício Prático (EP) apresentada pela disciplina Banco de Dados (ACH2004), ministrada pela Prof. Dr. Sarajane Peres, na Universidade de São Paulo.


## Notas
Esse é um exemplo de CRUD para um sistema de hotelaria. Portanto, apresenta uma tabela para as entidades e seus respectivos atributos, contendo a possibilidade de criar, modificiar, remover e pesquisar entre os dados.

## Requisitos do sistema: Gestão de Hotelaria
O banco de dados que você modelará deverá estar preparado para dar suporte ao desenvolvimento de
um grande sistema de gestão de hotelaria. Abaixo seguem algumas especificações básicas sobre o
contexto que o seu banco de dados deve considerar. Você deve atender a todos esses requisitos e trazer
novos requisitos que agreguem valor ao seu banco de dados.

O sistema de gestão de hotelaria (SGH) pressupõe uma rede hoteleira que possui um escritório central e
uma série de hotéis distribuídos geograficamente pelo Brasil. As unidades do hotel dispersas pelo país
assumem diferentes categorias (p.ex. hotel tradicional, pousadas, apart-hotéis, condomínio de hotéis e
resorts). Além disso, os hotéis também são setorizados (dentro de uma mesma unidade ou entre unidades
diferentes) entre hotéis voltados para pessoas que estão a trabalho, hotéis para família, hotéis para
adultos, hotéis que permitem pets etc.

No escritório central deve estar instalado um módulo do SGH que gerencia as operações tradicionais de
uma empresa. Entre essas operações está o subsistema de gerenciamento do patrimônio, o subsistema
de contabilidade geral e o subsistema de recursos humanos. O gerenciamento do patrimônio diz respeito
ao cadastro de cada hotel pertencente à rede. Sobre cada hotel, o sistema guarda informações de registro
imobiliário (com dados de georreferenciamento), nome fantasia, tamanho e categoria da unidade. O
sistema de contabilidade geral é responsável por gerenciar o caixa de entrada e de saída de toda a rede
hoteleira. É desse sistema que são emitidas as notais fiscais para clientes e no qual são cadastrados os
documentos referentes a pagamentos realizados para governo, associações, serviços de terceiros e
fornecedores. O sistema de recursos humanos é onde todos os dados dos funcionários do hotel estão
cadastrados e são gerenciados. Além dos dados tradicionalmente necessários para identificar as pessoas,
o sistema também armazena informação sobre o tipo de contrato, o salário, os benefícios (planos de
saúde, vale transporte, alimentação, refeição, por exemplo).

Algumas unidades da rede possuir um lobby no qual é estabelecido um condomínio. Nesse condomínio
podem se instalar lojas de varejo, empresas de turismo, restaurantes e bares e teatros. O gerenciamento
dos aluguéis e controle dos tipos de condôminos são centralizados no escritório geral da rede.
O SGH disponibiliza um módulo de gerenciamento de reservas. Esse módulo pode ser gerenciado de forma
centralizada, porém, cada unidade da rede precisa ter autonomia sobre as reservas que lhe cabem e uma
unidade não deve ter permissão para realizar ingerência de reservas em outras unidades. O sistema
precisa ter acesso a informações que possibilitem admitir um novo hóspede, então algumas coisas são
necessárias: dados sobre acomodações (tipo e amenidades), preços praticados, políticas de uso,
capacidade máxima etc. Além disso, o status das unidades precisam estar armazenados (ocupado, livre,
reservado, fora de operação – dentro de um calendário de no máximo um ano à frente da data atual).
Esse sistema será usado para montagem de mapa de ocupação e para integração com sistemas de
terceiros de reservas online (no estilo Booking.com). A informatização nessa rede hoteleira é de última
geração. Então, as acomodações contam com sensores para identificação de itens faltantes, por exemplo,
a retirada de um item do frigobar automaticamente alimenta o módulo de geração de consumo da
acomodação para fins de contabilização final da conta para pagamento no check-out. Há ainda um
gerenciamento de manutenção de rotina associado a todas as dependências da unidade: acomodações,
piscina, academia, sala de eventos, restaurante. Esse controle mantém um status de limpeza realizada
principalmente para as acomodações, já que isso implica em uma acomodação estar disponível para
check-in ou não. 

O hotel mantém um sistema para permitir o autosserviço de estacionamento. Esse sistema faz reservas
de garagens (ao ar livre ou coberta), controla a saída e a entrada de carros e está disponível apenas para
hóspedes. Por ser um estacionamento restrito, a cobrança de uso é diária e relacionada à reserva do
cliente. O cliente pode usar o estacionamento por menos dias do que o reservado para sua acomodação,
mas não pode usar para um número maior de dias. 
O relacionamento com clientes (CRM) da rede de hotéis é baseado em um programa de fidelidade e um
chatbot. O programa de fidelidade precisa armazenar informações sobre todas as passagens do cliente
por qualquer unidade da rede de forma que ele possa ser bonificado periodicamente. A bonificação é
concedida na forma de pontos que ele pode usar em reservas futuras ou no serviço de quarto. O chatbot
é um sistema terceirizado, porém, ele gera requisições para a staff do hotel e essas requisições ficam
atreladas ao cliente (se ele é um hóspede) ou a um pool de requisições geral. O armazenamento das
requisições pressupõe um identificador da requisição, um atendedor (quais funcionários foi designado
para resolver a requisição), um status (aberta, atendida, cancelada), a data de abertura e de
fechamento/cancelamento, uma classificação do tipo da requisição e um campo texto de livre
preenchimento.

Todas as unidades contam com um espaço para eventos. Em cada unidade, esse espaço possui uma
capacidade em particular, uma infraestrutura e uma lista de tipos de uso. Por exemplo, uma unidade
maior possui um espaço para eventos que tem várias salas e pode receber um grande público; outra
unidade possui um espaço ao ar livre com capacidade para um público menor. Diferentes usos podem ser
feitos em cada unidade e o sistema de gestão do hotel delega a gestão desses espaços a módulos do
sistema instalados nas unidades.

Por fim, cada unidade também precisa gerenciar o café da manhã e o serviço de quarto. Isso significa que
ela possui uma cozinha que mante um controle de estoque de produtos alimentícios. Esse sistema está
interligado ao modulo de checkout para que as compras realizadas no serviço de quarto sigam
diretamente para a conta do cliente. O café da manhã pode ser considerado uma compra, visto que nem
todas as reservas têm o café da manhã como item incluso. 
