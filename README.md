# Sistema de Gestão de Operadora Logística | Domínio



Por que o DDD ajudará a empresa a organizar o ecossistema (conforme o projeto cresce): pois o DDD ajuda na separação de conceitos da organização, e facilita a comunicação. Isso deixa a estrutura mais modular, escalável, segura, simples e reduz o alto acoplamento entre as entidades.



### Subdomínios:



* Rota - Core;
* Rastreamento - Core;
* Frete - Core;
* Faturamento - Generic;
* ConciliacaoBancaria - Generic;
* Veiculo - Supporting.



### Glossário (linguagem ubíqua):



| Termo | Explicação | Código |


* Conciliação Bancária -> verificação de registros bancários : ConciliacaoBancaria
* Faturamento -> informação da receita gerada: Faturamento
* Finança -> contexto relacionado ao fluxo de caixa : Financa
* Frete -> taxa do envio : Frete
* Frota -> conjunto de veículos da organização : Frota
* Logística -> gerenciamento da movimentação de recursos realizados pela frota : Logistica
* Nota Fiscal -> registro de documento fiscal : NotaFiscal
* Rastreamento -> localização do envio : Rastreamento
* Rota -> caminho traçado pelo veículo do pedido : Rota
* Veículo -> transporte utilizado para entregas : Veiculo


### Domínio | Diagrama DDD (strategic design):
(com bounded contexts e shared kernels).



<img src="dominio.jpg" width="700px" height="900px" />



Explicação das conexões no shared kernel: frete e faturamento compartilham funcionalidades relacionadas com as taxas das entregas. Frota e rastreamento compartilham informações relacionadas ao percurso de veículos da frota.   



A estrutura do projeto (com a divisão de domínios) está disponível dentro da pasta *estrutura* neste repositório. Ela lembra uma arquitetura utilizando o padrão monólito. É possível implementar o projeto com uma arquitetura de micro-serviços.
