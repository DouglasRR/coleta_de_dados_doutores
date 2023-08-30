# Coleta de Dados de Ginecologistas em MG (Doctoralia)

## Objetivo

Este código é uma solução para a coleta de dados de todos os ginecologistas em Belo Horizonte, MG, a partir do site da Doctoralia. Ele extrai informações como a cidade, nome, telefone e link de cada perfil de ginecologista.

## Funcionalidade

O código utiliza a biblioteca BeautifulSoup para realizar o web scraping e coletar os dados dos perfis de ginecologistas. Ele começa visitando cada página de resultados de busca no site da Doctoralia e coletando os links dos perfis de doutores e clínicas. Em seguida, ele filtra esses links para garantir que apenas os perfis de ginecologistas sejam considerados.

Para cada perfil, o código coleta o nome, cidade e telefone. Caso algum desses campos não seja encontrado, ele retorna um ponto de interrogação. Os dados coletados são armazenados em um DataFrame do pandas.

## Módulos Utilizados

- `BeautifulSoup`: Biblioteca para análise e extração de dados de HTML e XML.
- `requests`: Biblioteca para realizar requisições HTTP.
- `pandas`: Biblioteca para manipulação de dados em formato tabular.
- `re`: Módulo para manipulação de expressões regulares.
- `os`: Módulo para interagir com o sistema operacional, usado para exclusão de arquivos auxiliares.

## Uso

1. **Iniciar a Coleta**: O código instância a classe `Coleta` e chama o método `iniciar()` para começar a coleta dos dados.
2. **Coleta dos Dados**: O código navega por todas as páginas de resultados da busca e extrai os links dos perfis de ginecologistas.
3. **Filtragem dos Links**: Ele filtra os links para incluir apenas os perfis relevantes.
4. **Coleta das Informações**: Para cada perfil, ele extrai o nome, cidade e telefone, armazenando-os no DataFrame.
5. **Exclusão de Arquivos Auxiliares**: Os arquivos temporários criados durante a coleta são excluídos.
6. **Exportação dos Dados**: Os dados são exportados para um arquivo Excel chamado `dados.xlsx`.

## Observações

- O código é projetado para coletar informações dos 82 perfis de ginecologistas em Belo Horizonte. Se a quantidade de perfis mudar, isso deve ser ajustado.
- O código pode ser adaptado para outros casos de uso semelhantes, mas lembre-se de verificar as políticas de uso do site antes de fazer web scraping.

## Disclaimer

Este código é apresentado apenas para fins educativos e informativos. Certifique-se de que o uso do web scraping esteja em conformidade com os termos de uso do site alvo.
