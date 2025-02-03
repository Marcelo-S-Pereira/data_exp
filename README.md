**Portal da Transparência - Análise de Viagens de Servidores**

Este repositório tem como objetivo explorar os dados disponibilizados pelo Portal da Transparência sobre viagens realizadas por servidores públicos, buscando identificar padrões, despesas e possíveis anomalias.

Baixar Dados

Os dados utilizados podem ser baixados diretamente do Portal da Transparência:

Portal da Transparência - Download de Dados de Viagens

Configuração Inicial

Defina o ano desejado para análise:

```python
Ano = 2023
caminho_dados = f'/caminho/para/dados/{Ano}_Viagem.csv'
caminho_output = f'/caminho/para/output/Viagens-Passagens-trechos_{Ano}.xlsx'
```


Certifique-se de que os arquivos de dados estejam salvos no caminho configurado.

Bibliotecas Utilizadas

pandas

matplotlib

plotly.express

Instale as bibliotecas com:

pip install pandas matplotlib plotly

Análise Explorátoria

A análise inclui as seguintes etapas:

1. Conversão e Limpeza de Dados

Configuração de opções do pandas para melhor visualização.

Conversão de colunas de datas.

Criação de colunas para despesas totais e duração da viagem.

2. Normalização de Cargos

Preenchimento de valores nulos para cargos.

Criação de dataframe consolidado com colunas agregadas (despesas médias, totais, duração média, destinos mais frequentes e número de viagens).

3. Visualização de Dados

Gráficos gerados para melhor compreensão dos dados:

Número de Viagens por Cargo

Despesas Médias por Cargo

Dispersão de Dias de Viagem por Despesas

Salvamento dos gráficos:

plt.savefig(caminho_graf1, bbox_inches='tight')
plt.savefig(caminho_graf2, bbox_inches='tight')

Casos de Destaque

Viagem de Destaque

Uma viagem de 9 dias realizada por Ministério, com gasto superior a R$ 190 mil, incluiu visitas oficiais a Jacarta/Indonésia e Phnom Penh/Camboja. Houve alterações de itinerário devido a ações na Faixa de Gaza.

Dados Relacionados

Identificador do processo de viagem: 19194886

Possíveis dados adicionais podem ser encontrados no arquivo de passagens.

Outras Viagens Relevantes

2 Viagens com +130 Dias:

Cargo: CCX-207 (Cargo Comissionado Executivo)

Acompanhamento da ex-Presidente Dilma Rousseff

Destino: Xangai/China

Gasto superior a R$ 190 mil.

Viagem de 216 Dias:

Solicitante: Polícia Federal

Despesa: +R$ 184 mil

Destino sigiloso.

Conclusão

A análise evidencia padrões relevantes e aponta para outliers que necessitam de atenção, como viagens com despesas elevadas em curtos períodos e gastos não identificáveis. Os dados fornecem subsídios para um melhor entendimento das despesas públicas com viagens de servidores.

Recomendações Finais

Consultar os arquivos de Passagens e Trechos para investigação detalhada.

Identificar padrões de viagens com alto custo e baixa duração.

Avaliar o impacto de cargos protegidos por sigilo nas despesas totais.

Contato

Caso tenha dúvidas ou sugestões, entre em contato via GitHub Issues.
