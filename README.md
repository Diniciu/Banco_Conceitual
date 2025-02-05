# Banco_Conceitual

## Descrição do Esquema Conceitual

Este arquivo contém um diagrama de um esquema conceitual para um sistema de gerenciamento de serviços automotivos. O diagrama ilustra as entidades principais do sistema e os relacionamentos entre elas. As entidades incluem Cliente, Veículo, Ordem de Serviço, Equipe, Mecânico, Serviço e Peça. Cada entidade possui seus respectivos atributos e chaves primárias, e os relacionamentos entre as entidades são representados por linhas conectando-as, com indicações de cardinalidade.

## Entidades e Atributos

### Cliente
- **idCliente** (INT): Identificador único do cliente.
- **Nome** (VARCHAR(45)): Nome do cliente.
- **Endereço** (VARCHAR(45)): Endereço do cliente.
- **Telefone** (VARCHAR(45)): Telefone do cliente.
- **Email** (VARCHAR(45)): Email do cliente.
- **Veículo_idVeículo** (INT): Chave estrangeira referenciando a entidade Veículo.

### Veículo
- **idVeículo** (INT): Identificador único do veículo.
- **Placa** (VARCHAR(45)): Placa do veículo.
- **Modelo** (VARCHAR(45)): Modelo do veículo.
- **Ano** (INT): Ano de fabricação do veículo.
- **Marca** (VARCHAR(45)): Marca do veículo.
- **Ordem de Serviço_idOrdem de Serviço** (INT): Chave estrangeira referenciando a entidade Ordem de Serviço.

### Ordem de Serviço
- **idOrdem de Serviço** (INT): Identificador único da ordem de serviço.
- **Data de Emissão** (DATE): Data de emissão da ordem de serviço.
- **Data de Conclusão** (DATE): Data de conclusão da ordem de serviço.
- **Valor Total** (DECIMAL): Valor total da ordem de serviço.
- **Status** (VARCHAR(45)): Status da ordem de serviço.
- **Serviço_idServiço** (INT): Chave estrangeira referenciando a entidade Serviço.
- **Peça_idPeça** (INT): Chave estrangeira referenciando a entidade Peça.

### Equipe
- **idEquipe** (INT): Identificador único da equipe.
- **Nome da Equipe** (VARCHAR(45)): Nome da equipe.
- **Mecânico_idMecânico** (INT): Chave estrangeira referenciando a entidade Mecânico.
- **Ordem de Serviço_idOrdem de Serviço** (INT): Chave estrangeira referenciando a entidade Ordem de Serviço.

### Mecânico
- **idMecânico** (INT): Identificador único do mecânico.
- **Nome** (VARCHAR(45)): Nome do mecânico.
- **Endereço** (VARCHAR(45)): Endereço do mecânico.
- **Especialidade** (VARCHAR(45)): Especialidade do mecânico.

### Serviço
- **idServiço** (INT): Identificador único do serviço.
- **Descrição** (VARCHAR(45)): Descrição do serviço.
- **Valor da Mão-de-Obra** (DECIMAL): Valor da mão-de-obra do serviço
