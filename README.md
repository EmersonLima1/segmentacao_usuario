# Sistema de Segmentação e Perfil de Usuário

<div align="justify">

Este projeto consiste em um sistema de segmentação e perfil de usuário. O conjunto de dados compreende 1.000 perfis de usuários, cada um com 16 recursos distintos, incluindo dados demográficos, comportamento online, envolvimento com o conteúdo, interação com anúncios e interesses do usuário.

### Objetivo

O objetivo principal deste sistema é categorizar os usuários em segmentos distintos, identificando padrões e clusters significativos na base de usuários. Ao analisar dados de interação do usuário, informações demográficas e métricas de engajamento, o sistema permite que as empresas adaptem suas campanhas publicitárias aos segmentos identificados. Isso aumenta a relevância do anúncio, o envolvimento do usuário e as taxas de conversão, ao mesmo tempo que otimiza os gastos com publicidade.

### Fonte dos Dados

Os dados foram obtidos em: [user_profiles_for_ads.csv](https://statso.io/wp-content/uploads/2024/02/user_profiles_for_ads.csv)

### Recursos do Conjunto de Dados

O conjunto de dados inclui os seguintes recursos para cada usuário:

- ID do usuário: Identificador exclusivo de cada usuário.
- Idade: Faixa etária do usuário.
- Gênero: Gênero do usuário.
- Localização: Tipo de localização do usuário (Urbana, Suburbana, Rural).
- Idioma: Idioma principal do usuário.
- Nível de escolaridade: Nível de escolaridade mais alto alcançado.
- Curtidas e reações: Número de curtidas e reações que um usuário fez.
- Contas seguidas: Número de contas que um usuário segue.
- Uso do dispositivo: Dispositivo principal usado para acessar a plataforma (celular, desktop, tablet).
- Tempo gasto online (horas/dia da semana): Média de horas passadas online durante a semana.
- Tempo gasto online (horas/fim de semana): Média de horas passadas online nos finais de semana.
- Taxas de cliques (CTR): Porcentagem de impressões de anúncios que levam a cliques.
- Taxas de conversão: Porcentagem de cliques que levam a conversões/ações.
- Tempo de interação com anúncios (seg): Tempo médio gasto interagindo com anúncios em segundos.
- Nível de renda: Nível de renda do usuário.
- Principais interesses: Principais interesses do usuário.

### Ambiente de desenvolvimento

Este projeto foi desenvolvido no ambiente do Google Colab, uma plataforma gratuita baseada em nuvem que permite escrever e executar código Python diretamente no navegador, sem a necessidade de configuração de ambiente local. O uso do Google Colab proporcionou uma maneira conveniente de colaborar em tempo real, além de oferecer acesso fácil a recursos computacionais, como CPUs, que foram suficientes para as tarefas de análise de dados e modelagem realizadas neste projeto. O ambiente também facilitou o compartilhamento e a replicação do código, permitindo que qualquer pessoa interessada na análise dos dados e resultados pudesse acessar e executar o código sem configurações adicionais.

[Link para o arquivo notebook do projeto](https://github.com/EmersonLima1/segmentacao_usuario/blob/main/Segmenta%C3%A7%C3%A3o_e_perfil_de_usu%C3%A1rio.ipynb)

### Funcionalidades

- Segmentação de Usuários:
    - Utiliza o algoritmo K-means para agrupar os usuários em segmentos distintos com base em características demográficas, comportamentais e de engajamento.

- Análise de Segmentos:
    - Analisa os segmentos gerados e classifica-os com base em características importantes, como interesses, localização e gênero.
    - A relevância de cada segmento é determinada com base em métricas de engajamento, como taxas de cliques e conversão.

- Visualização de Dados:
    - Cria gráficos para visualizar a distribuição de variáveis demográficas, comportamentais e métricas de engajamento dos usuários.
    - Visualiza os interesses mais comuns dos usuários em um gráfico de barras.
    - Mostra relações lineares entre diferentes variáveis, como tempo online e taxas de cliques/conversão.

### Utilização do K-means

- O algoritmo K-means é uma técnica de agrupamento amplamente utilizada em análise de dados e aprendizado de máquina. Ele é empregado neste projeto como parte do processo de segmentação de usuários para campanhas publicitárias mais direcionadas e eficazes.

- Funcionalidades Principais:

  - Padronização de Dados:
    - Antes de aplicar o K-means, os dados são padronizados para garantir que todas as características tenham a mesma escala. Isso é importante para evitar que características com magnitudes maiores dominem o processo de agrupamento.

  - Determinação do Número de Clusters:
    - O usuário pode especificar o número desejado de clusters (segmentos) que deseja criar. Este número é um parâmetro essencial para o algoritmo K-means.

  - Agrupamento dos Usuários:
    - O K-means é então aplicado aos dados padronizados. Ele agrupa os usuários em 'k' grupos, onde 'k' é o número especificado de clusters. O algoritmo tenta minimizar a variância dentro de cada cluster e maximizar a variância entre os clusters.

  - Análise e Classificação dos Segmentos:
    - Após a aplicação do K-means, cada usuário é atribuído a um dos clusters com base em sua proximidade aos centróides dos clusters. Uma análise adicional é realizada para entender as características de cada segmento, como interesses, comportamento online e métricas de engajamento com anúncios. Os segmentos são então classificados com base em sua relevância, o que auxilia na identificação de segmentos valiosos para direcionar campanhas publicitárias.

- Benefícios:

  - Segmentação Eficiente: O K-means permite segmentar os usuários em grupos significativos com base em suas características, facilitando uma compreensão mais profunda do comportamento e das preferências dos usuários.

  - Otimização de Estratégias de Marketing: Ao identificar segmentos valiosos, as empresas podem adaptar suas campanhas publicitárias para atender às necessidades e interesses específicos desses segmentos, aumentando a relevância dos anúncios e as taxas de conversão.

  - Reutilização e Manutenção do Código: O uso do K-means como parte de uma classe de sistema de segmentação de usuários encapsula a funcionalidade relacionada à segmentação, facilitando a reutilização, organização e manutenção do código.
 
### Comentários sobre os segmentos (clusters) encontrados:

- Segmento 1:
    - Descrição: Este segmento é composto por usuários localizados em áreas rurais que acessam a plataforma exclusivamente por dispositivos móveis. Eles demonstram interesse em culinária gourmet e cuidados com animais de estimação.
    - Comentário: Este segmento pode ser alvo de campanhas publicitárias relacionadas a produtos ou serviços relacionados à culinária gourmet e cuidados com animais de estimação, adaptadas para dispositivos móveis.

- Segmento 3:
    - Descrição: Usuárias femininas que acessam a plataforma principalmente por desktops e têm interesse em modelagem de moda e ciência de dados.
    - Comentário: Estratégias de marketing direcionadas a produtos relacionados à moda e cursos de ciência de dados podem ser eficazes para este segmento, especialmente através de anúncios adaptados para desktops.

- Segmento 5:
    - Descrição: Mulheres com doutorado, que falam espanhol e residem em áreas suburbanas. Elas demonstram interesse em produção musical, ciência de dados, modelagem de moda e fotografia, e acessam a plataforma por meio de dispositivos móveis e desktops.
    - Comentário: Este segmento pode ser alvo de campanhas publicitárias relacionadas a cursos online avançados, equipamentos de fotografia e software de produção musical, otimizados para dispositivos móveis e desktops.

- Segmento 7:
    - Descrição: Homens com graduação em bacharelado, que falam espanhol e residem em áreas suburbanas. Eles acessam a plataforma exclusivamente por dispositivos móveis e demonstram interesse em cuidados com animais de estimação, modelagem de moda, marketing digital e estilo de vida ecológico.
    - Comentário: Estratégias de marketing que promovam produtos ou serviços relacionados ao estilo de vida ecológico, juntamente com campanhas publicitárias criativas sobre moda e cuidados com animais de estimação, podem ser eficazes para este segmento, especialmente em dispositivos móveis.

- Segmento 9:
    - Descrição: Mulheres com graduação em bacharelado.
    - Comentário: Embora este segmento tenha uma descrição mais genérica, ainda pode ser alvo de campanhas publicitárias que abordem uma variedade de interesses e necessidades relacionadas a produtos ou serviços relevantes para mulheres com educação universitária.

- Segmento 10:
    - Descrição: Usuários localizados em áreas suburbanas com interesse em ciência de dados, leitura e literatura.
    - Comentário: Este segmento pode ser direcionado com campanhas publicitárias que promovam livros, cursos online e eventos relacionados à ciência de dados e literatura, adaptados para dispositivos móveis e desktops.

- Segmento 13:
    - Descrição: Homens que acessam a plataforma por dispositivos móveis e desktops, com interesse em produção musical e estilo de vida ecológico.
    - Comentário: Campanhas publicitárias que destacam equipamentos de produção musical e produtos sustentáveis podem atrair a atenção deste segmento, especialmente quando apresentadas em dispositivos móveis e desktops.

- Segmento 14:
    - Descrição: Mulheres residentes em áreas suburbanas com interesse em fitness e bem-estar, além de modelagem de moda.
    - Comentário: Estratégias de marketing que promovam roupas esportivas, equipamentos de fitness e produtos de bem-estar podem ressoar com este segmento, especialmente quando apresentadas de forma visualmente atraente em dispositivos móveis e desktops.

- Segmento 16:
    - Descrição: Usuários localizados em áreas rurais com interesse em ciência de dados e investimentos financeiros.
    - Comentário: Este segmento pode ser direcionado com campanhas publicitárias relacionadas a cursos de análise de dados e investimentos financeiros, adaptadas para dispositivos móveis e desktops.

- Segmento 18:
    - Descrição: Homens que residem em áreas urbanas.
    - Comentário: Embora a descrição deste segmento seja bastante genérica, ainda pode ser alvo de campanhas publicitárias que abordem uma variedade de produtos e serviços relevantes para homens urbanos.
 
### Comentários sobre as Relações entre Tempo e Taxas de Conversão e Cliques em Anúncios

- Relação entre Tempo Online em Dias Úteis e Taxas de Conversão:

    ![Descrição da imagem](https://github.com/EmersonLima1/segmentacao_usuario/raw/main/Gr%C3%A1ficos%20de%20rela%C3%A7%C3%A3o/Tempo%20online%20dias%20ut%C3%A9is%20x%20taxas%20de%20convers%C3%A3o.png)

  - Com base na observação do gráfico, percebe-se uma variação nas taxas de conversão médias com o aumento do tempo online em dias úteis. Porém, essa variação não segue um padrão claro de aumento ou diminuição consistente, sugerindo uma influência moderada, porém não linear, do tempo online em dias úteis nas taxas de conversão.

- Relação entre Tempo Online em Dias Úteis e Taxas de Cliques:

    ![Descrição da imagem](https://github.com/EmersonLima1/segmentacao_usuario/raw/main/Gr%C3%A1ficos%20de%20rela%C3%A7%C3%A3o/Tempo%20online%20dias%20ut%C3%A9is%20x%20taxas%20de%20cliques.png)

  - Ao analisar o gráfico, nota-se uma variação nas taxas de cliques médias à medida que o tempo online em dias úteis aumenta. Os intervalos entre 2.0 e 3.0 horas e entre 3.0 e 4.0 horas apresentam taxas de cliques mais altas em comparação com os intervalos adjacentes, indicando uma propensão dos usuários a clicar mais em anúncios durante esses períodos.

- Relação entre Tempo Online nos Finais de Semana e Taxas de Conversão:

    ![Descrição da imagem](https://github.com/EmersonLima1/segmentacao_usuario/raw/main/Gr%C3%A1ficos%20de%20rela%C3%A7%C3%A3o/Tempo%20online%20finais%20de%20semana%20x%20taxas%20de%20convers%C3%A3o.png)
    
  - Observando o gráfico, é possível identificar uma tendência de aumento nas taxas de conversão médias à medida que o tempo online nos finais de semana aumenta. Os intervalos de tempo mais longos, especialmente acima de 7 horas, apresentam as taxas de conversão médias mais altas em comparação com os intervalos mais curtos, sugerindo uma maior propensão dos usuários a realizar ações de conversão durante esses períodos.

- Relação entre Tempo Online nos Finais de Semana e Taxas de Cliques:

    ![Descrição da imagem](https://github.com/EmersonLima1/segmentacao_usuario/raw/main/Gr%C3%A1ficos%20de%20rela%C3%A7%C3%A3o/Tempo%20online%20finais%20de%20semana%20x%20taxas%20de%20cliques.png)

  - Com base na análise do gráfico, observa-se uma relação inversa entre o tempo online nos finais de semana e as taxas de cliques médias. Embora os intervalos mais curtos de tempo apresentem taxas de cliques médias mais altas, os intervalos mais longos exibem taxas de cliques médias mais baixas, indicando que passar muito tempo online nos finais de semana pode diminuir a propensão dos usuários a clicar em anúncios.

- Relação entre Tempo de Interação com Anúncios e Taxas de Cliques:

    ![Descrição da imagem](https://github.com/EmersonLima1/segmentacao_usuario/raw/main/Gr%C3%A1ficos%20de%20rela%C3%A7%C3%A3o/Tempo%20intera%C3%A7%C3%A3o%20an%C3%BAncios%20x%20taxa%20de%20cliques.png)

  - Ao analisar o gráfico, verifica-se que intervalos mais curtos de tempo de interação com anúncios tendem a apresentar taxas de cliques médias mais altas. No entanto, à medida que o tempo de interação aumenta, a relação entre o tempo e as taxas de cliques não segue uma tendência linear, destacando a importância da qualidade e relevância do conteúdo do anúncio na determinação do engajamento dos usuários.
 
### Implicações para a Estratégia de Marketing

Com base nas visualizações detalhadas dos dados e nos segmentos identificados pelo sistema de segmentação de usuários, a empresa pode aprimorar suas estratégias de marketing de maneira significativa. As informações demográficas, comportamentais e de interesse fornecem insights valiosos para a personalização de campanhas publicitárias, permitindo à empresa direcionar mensagens mais relevantes para cada segmento específico. Isso não apenas aumenta a eficácia das campanhas, mas também ajuda a otimizar o uso dos recursos de marketing, concentrando-se nos segmentos com maior potencial de conversão. Em última análise, essa abordagem permite que a empresa atinja seus objetivos de negócios com maior eficiência e maximize o retorno sobre o investimento em publicidade.
