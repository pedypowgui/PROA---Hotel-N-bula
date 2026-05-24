# Hotel nébula

## Entidades
### Hospede
Representação do usuário do sistema que seleciona e realiza as reservas. Possui nome, cpf, telefone, e-mail e data de nascimento.

### Reservas
Representação do pedido de uma hospedagem. Contém a data de realização da reserva, data de entrada, data de saída e o status da reserva(pendente, confirmada, cancelada).

### Avaliacoes
Representação das avaliações que os usuários fazem após se hospedarem. Contém a data da avaliação, a nota(de 0 a 5 estrelas) que o usuário deu e o comentário do usuário.

### Hospedagens
Representa a estadia em si do usuário. Possui a quantidade de hospedes que estarão nessa hospedagem, o check-in e o check-out.

### Funcionarios
Representa os trabalhadores do Hotel Nébula, tanto os de atendimento quanto os de serviço de quarto para limpeza. Possui e-mail, telefone, salario, cargo e nome.

### Quartos
Representa o quarto em que o hóspede ficará hospedado. Contém o número do quarto, andar que ele se localiza, o status(pronto e em limpeza), tipo(executivo, luxo e suíte) e o valor da diária.

### Pagamentos
Representa os pagamentos realizados durante pelo hóspede na hospedagem. Contém data de pagamento, forma de pagamento, valor e a hora do pagamento.

### HospedagemQuarto
Representa a ligação entre a hospedagem e o quarto, relacionando-os.

### FuncionarioLimpeza
Representa a ligação entre os funcinários da limpeza e o quarto, relacionando-os.

## Relacionamentos
### Hospede: 
- Pode realizar várias reservas
- Pode fazer avaliações depois de uma hospedagem
- Pode se hospedar uma ou várias vezes

### Reservas: 
- Pertence a um hóspede
- É gerenciada por um funcionário
- Gera uma hospedagem

### Avaliacoes: 
- Pertence a um hóspede e a uma hospedagem

### Hospedagens: 
- Gerenciada por um funcionário
- Gerada a partir de uma reserva
- Realizada por um hospede
- Recebe nenhuma ou várias avaliações
- Possui um quarto ou mais
- Possui um ou mais pagamentos

### Quartos: 
- É limpo por um ou mais funcionários
- Pertence a apenas uma hospedagem

### Pagamentos: 
- Pertence a uma hospedagem
- Aceita mastercard, visa, elo e pix

### Funcionarios: 
- Pode gerenciar reservas muitas
- Pode gerenciar muitas hospedagens
- Pode limpar muitos quartos

### HospedagemQuarto:
- Relaciona uma hospedagem com um quarto

### FuncionarioLimpeza
- Relaciona um funcionário da limpeza com um quarto
