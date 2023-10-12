# BUSCA INFORMADA - HEURÍSTICAS
## CONCEITO:
A busca informada, também conhecida como busca heurística, é uma técnica de busca que utiliza informações adicionais para orientar o processo de busca em direção a uma solução de forma mais eficiente. Isso é feito por meio do uso de heurísticas, que são funções que estimam quão próximo ou distante um estado está do estado objetivo. As heurísticas são usadas para priorizar os estados mais promissores durante a busca, com o objetivo de encontrar uma solução de maneira mais rápida do que a busca cega. Aqui estão os conceitos-chave relacionados à busca informada e heurísticas:

**1. Heurísticas:**
   - As heurísticas são funções que estimam o custo ou o valor de um estado em relação ao estado objetivo. Elas são projetadas para serem rápidas de calcular e fornecer estimativas razoavelmente precisas.

**2. Função de Avaliação:**
   - A busca informada utiliza uma função de avaliação que combina a heurística com o custo atual para determinar quais estados devem ser explorados a seguir.

**3. Exemplos de Heurísticas:**
   - **Distância Euclidiana**: Uma heurística comum em problemas de roteamento que estima a distância em linha reta entre o estado atual e o estado objetivo.
   - **Contagem de Peças Fora do Lugar**: Usada em quebra-cabeças, como o quebra-cabeça de 8 peças, conta quantas peças não estão na posição correta.
   - **Função de Heurística Admissível**: Uma heurística é admissível se nunca superestimar o custo para atingir o estado objetivo. Essa é uma propriedade importante para garantir a otimalidade da busca.

**4. Algoritmos de Busca Informada:**
   - **Busca A* (A-Star)**: É um dos algoritmos de busca informada mais populares. Ele usa a função de avaliação que combina o custo atual e a heurística. O A* é garantido para encontrar uma solução ótima se a heurística for admissível.
   - **Busca Greedy Best-First Search**: Usa apenas a heurística para escolher o próximo estado, ignorando o custo atual. Pode não ser ótimo, mas é mais eficiente em termos de tempo de execução.

**5. Vantagens da Busca Informada:**
   - Permite uma exploração mais eficiente da árvore de busca, especialmente em problemas complexos.
   - É útil em problemas com espaço de estados grande ou desconhecido.
   - Pode encontrar soluções ótimas se a heurística for admissível.

**6. Desvantagens da Busca Informada:**
   - Dependência de uma heurística precisa, e encontrar uma boa heurística pode ser desafiador em alguns casos.
   - Não garante soluções ótimas se a heurística não for admissível.

A busca informada é amplamente utilizada em problemas do mundo real, como roteamento de veículos, planejamento de trajetórias de robôs, jogos, sistemas de navegação, entre outros. A combinação de heurísticas eficazes com algoritmos de busca informada pode resultar em soluções mais rápidas e eficientes para uma ampla variedade de problemas.

## BUSCA GULOSA
A busca gulosa (também conhecida como busca de melhor escolha) é uma técnica de busca informada que se concentra em selecionar o estado que parece mais promissor com base em uma heurística, sem levar em consideração o custo real ou a profundidade do caminho até esse estado. A busca gulosa é uma forma de busca informada que prioriza a exploração de estados que estão mais próximos do estado objetivo, de acordo com a estimativa da heurística. Aqui estão os princípios-chave da busca gulosa:

**1. Heurística:**
- A busca gulosa utiliza uma heurística para estimar quão próximo ou distante um estado está do estado objetivo. Essa heurística deve ser rápida de calcular e, idealmente, deve ser admissível (ou seja, não superestimar o custo real para atingir o objetivo).

**2. Seleção do Estado:**
- Em cada etapa da busca, a busca gulosa seleciona o estado que tem a menor estimativa heurística em relação ao estado objetivo. Isso é feito com base na função de avaliação que combina a heurística e o custo atual.

**3. Vantagens da Busca Gulosa:**
- A busca gulosa é geralmente mais rápida do que algoritmos como A* (A-Star) porque não considera o custo total do caminho.
- Pode ser eficaz em problemas em que a heurística é altamente informativa e o espaço de estados não é muito grande.

**4. Desvantagens da Busca Gulosa:**
- A busca gulosa não garante encontrar uma solução ótima, mesmo se a heurística for admissível. Ela pode ficar presa em mínimos locais.
- Pode ignorar soluções potencialmente melhores se forem alcançadas por caminhos mais longos.

**5. Aplicações da Busca Gulosa:**
- A busca gulosa é comumente usada em sistemas de navegação e GPS para encontrar rotas rápidas para destinos, onde a distância euclidiana é uma heurística útil.
- É usada em problemas de otimização e roteamento, onde encontrar uma solução satisfatória é mais importante do que encontrar a solução ótima.

Embora a busca gulosa seja uma abordagem eficiente em termos de tempo de execução, é importante notar que ela não é adequada para todos os tipos de problemas. Ela é particularmente útil em problemas em que a heurística é altamente informativa e pode levar a soluções satisfatórias rapidamente, mesmo que não sejam ótimas. Em problemas onde a otimalidade é crucial, a busca gulosa pode não ser a escolha adequada, e algoritmos como A* são mais apropriados.

## EXEMPLOS DE BUSCA GULOSA:
A busca gulosa é frequentemente usada em problemas de otimização e roteamento, onde o objetivo principal é encontrar uma solução satisfatória, embora não necessariamente ótima, de forma eficiente. Aqui estão alguns exemplos de problemas em que a busca gulosa pode ser aplicada:

1. **Roteamento em Sistemas de Navegação GPS**:
   - O objetivo é encontrar a rota mais rápida de um ponto de partida a um destino, priorizando a minimização do tempo de viagem. A distância euclidiana entre os pontos pode ser usada como heurística.

2. **Problema do Caixeiro Viajante (Traveling Salesman Problem - TSP)**:
   - Neste problema de otimização, um vendedor precisa encontrar a rota mais curta que passa por um conjunto de cidades e retorna à cidade de origem. A busca gulosa pode ser usada para selecionar a cidade mais próxima como a próxima a ser visitada.

3. **Problema de Mochila (Knapsack Problem)**:
   - O objetivo é selecionar um conjunto de itens de uma lista, cada um com um valor e um peso, de modo que o valor total seja maximizado e o peso total não exceda a capacidade da mochila. A busca gulosa pode selecionar os itens com a melhor taxa valor/peso.

4. **Problema do Roteamento de Veículos (Vehicle Routing Problem - VRP)**:
   - Empresas de entrega e logística usam a busca gulosa para otimizar rotas de veículos, minimizando a distância percorrida ou o tempo de entrega.

5. **Problema de Empacotamento (Packing Problem)**:
   - Empresas de transporte de carga utilizam a busca gulosa para otimizar o carregamento de contêineres ou veículos de forma eficiente.

6. **Planejamento de Trajetória para Robôs Móveis**:
   - Robôs móveis usam a busca gulosa para planejar trajetórias que minimizam a distância ou o tempo de deslocamento, evitando obstáculos.

7. **Design de Circuitos Eletrônicos**:
   - No design de circuitos eletrônicos, a busca gulosa pode ser usada para otimizar a rota dos fios e conexões de forma a minimizar a área ocupada e atrasos de sinal.

8. **Algoritmos de Compressão de Dados**:
   - Algoritmos de compressão, como Huffman, usam uma busca gulosa para criar árvores de codificação que minimizam o tamanho do arquivo comprimido.

9. **Design de Layout de Páginas (Page Layout)**:
   - A busca gulosa pode ser usada para otimizar o layout de texto, imagens e outros elementos em páginas de revistas, livros e sites, com o objetivo de minimizar o espaço em branco e melhorar a estética.

Embora a busca gulosa seja eficaz em muitos desses problemas, é importante notar que ela pode não garantir a solução ótima em todos os casos. A escolha da heurística e a compreensão do trade-off entre eficiência e otimalidade são cruciais ao aplicar a busca gulosa em problemas do mundo real.

## BUSCA A ESTRELA:
A busca A* (A-Star) é um algoritmo de busca informada que combina as vantagens da busca gulosa e da busca em custo uniforme para encontrar a solução de um problema. Ela é amplamente usada em inteligência artificial, robótica, jogos e em problemas de otimização em que é necessário encontrar um caminho ou uma solução de custo mínimo em um espaço de estados. A busca A* é conhecida por ser um dos algoritmos mais eficientes e versáteis para busca em grafos. Aqui estão os princípios-chave da busca A*:

**1. Heurística:**
- A busca A* utiliza uma função de heurística que estima o custo do caminho do estado atual até o estado objetivo. Essa heurística deve ser admissível (não superestimar o custo) para garantir que a busca A* encontre a solução ótima.

**2. Função de Avaliação:**
- A busca A* utiliza uma função de avaliação que combina o custo real acumulado do início ao estado atual e a estimativa heurística do custo do estado até o estado objetivo.

**3. Seleção de Estados:**
- A busca A* seleciona estados a serem explorados com base na função de avaliação. Ela prioriza estados que têm baixo custo total, incluindo o custo real e a estimativa heurística.

**4. Vantagens da Busca A*:**
- Garante a otimalidade: Se a heurística é admissível, a busca A* encontrará a solução ótima.
- Eficiente: A busca A* é mais eficiente do que a busca cega (sem heurística) e é adequada para espaços de estados grandes.

**5. Desvantagens da Busca A*:**
- A eficiência depende da qualidade da heurística. Uma heurística ruim pode resultar em um desempenho pior.
- Pode exigir mais memória do que a busca em profundidade ou busca em largura, devido à manutenção de uma lista de estados a serem explorados.

**6. Aplicações da Busca A*:**
- Roteamento em sistemas de navegação GPS.
- Planejamento de trajetória para robôs móveis.
- Resolução de quebra-cabeças, como o quebra-cabeça de 8 peças.
- Jogos de tabuleiro, como xadrez, para encontrar as melhores jogadas.

A busca A* é uma ferramenta poderosa para encontrar soluções de custo mínimo em problemas de busca. Se a heurística é escolhida cuidadosamente, a busca A* pode ser altamente eficiente e garantir a otimalidade da solução. No entanto, a qualidade da heurística é fundamental para o desempenho do algoritmo.

## EXEMPLOS DE BUSCA A ESTRELA:
A busca A* (A-Star) é uma técnica de busca informada que pode ser aplicada a uma variedade de problemas em que se deseja encontrar um caminho de custo mínimo ou solução ótima. Aqui estão alguns exemplos de problemas que podem ser resolvidos usando a busca A*:

1. **Sistemas de Navegação e GPS**:
   - Encontrar a rota mais rápida de um ponto de partida a um destino, considerando o tráfego, ruas e rodovias. A busca A* é comumente usada para essa finalidade, com a distância euclidiana como heurística.

2. **Robótica e Planejamento de Trajetória**:
   - Planejar a trajetória de um robô móvel para evitar obstáculos e alcançar um local de destino de maneira eficiente. A busca A* é aplicada para encontrar o caminho mais curto.

3. **Jogos de Labirinto**:
   - Em jogos de labirinto, a busca A* pode ser usada para encontrar o caminho mais curto entre um personagem e um objetivo, levando em consideração obstáculos.

4. **Quebra-Cabeça de Oito Peças (8-Puzzle)**:
   - O objetivo é reorganizar peças deslizantes para chegar a uma configuração específica. A busca A* é usada para encontrar a sequência mais curta de movimentos.

5. **Resolução de Labirintos e Enigmas em Jogos de Video Game**:
   - Muitos jogos de vídeo game usam a busca A* para encontrar caminhos para personagens, inimigos ou objetos em ambientes complexos.

6. **Sistemas de Logística e Roteamento de Veículos**:
   - Otimizar rotas de entrega, escolhendo a ordem das entregas e minimizando o tempo ou a distância percorrida por veículos de entrega.

7. **Design de Redes de Comunicação**:
   - Projetar redes de comunicação eficientes, como redes de fibra óptica, para minimizar a distância total de cabos necessários.

8. **Aplicações de Inteligência Artificial e Busca**:
   - Em jogos de estratégia, como xadrez e damas, a busca A* é usada para encontrar as melhores jogadas.
   
9. **Design de Circuitos Integrados (CI)**:
   - A busca A* pode ser usada para otimizar a rota de conexões entre componentes em um circuito integrado para minimizar a área ocupada e os atrasos de sinal.

10. **Jogos de Palavras Cruzadas e Quebra-Cabeças de Palavras**:
    - Encontrar as melhores palavras ou soluções em quebra-cabeças de palavras cruzadas, levando em consideração restrições e dicas.

A busca A* é uma técnica poderosa e versátil que pode ser aplicada a uma ampla variedade de problemas em que é necessário encontrar um caminho ou uma solução de custo mínimo. Ela é amplamente usada em sistemas de navegação, robótica, jogos, otimização e muitas outras aplicações. A escolha da heurística apropriada é fundamental para o desempenho da busca A*.

## HEURÍSTICA ADMISSÍVEL:
Uma heurística admissível é uma função de estimativa que nunca superestima o custo real para atingir o estado objetivo a partir do estado atual. Em outras palavras, uma heurística é admissível se fornecer uma estimativa inferior ou igual ao custo real da solução, mas nunca uma estimativa superior. Essa propriedade é importante em algoritmos de busca informada, como a busca A*, porque garante que o algoritmo encontre uma solução ótima. Aqui estão alguns exemplos de heurísticas admissíveis e as situações em que são aplicadas:

1. **Distância Euclidiana (Euclidean Distance)**:
   - Essa heurística é frequentemente usada em problemas de roteamento e navegação, como sistemas de GPS. Ela calcula a distância em linha reta (a "distância do pássaro") entre o estado atual e o estado objetivo. A distância euclidiana é admissível porque é impossível chegar ao objetivo em um caminho mais curto do que a linha reta.

2. **Contagem de Peças Fora do Lugar (Misplaced Tiles)**:
   - Usada em quebra-cabeças, como o quebra-cabeça de 8 peças, essa heurística conta quantas peças estão fora de suas posições corretas em relação ao estado objetivo. Como cada movimento só pode trocar uma peça, a contagem de peças fora do lugar fornece uma estimativa inferior para o número de movimentos necessários para resolver o quebra-cabeça.

3. **Soma das Distâncias ManhattaNo (Manhattan Distance)**:
   - Também aplicada em quebra-cabeças e jogos de tabuleiro, como o quebra-cabeça de 8 peças e o xadrez, a heurística da distância Manhattan calcula a soma das distâncias horizontais e verticais entre as peças e suas posições corretas. Essa heurística é admissível porque não considera movimentos na diagonal, subestimando o custo real.

4. **Heurística do Máximo (Max Heuristic)**:
   - Em algumas situações, você pode usar a heurística máxima que escolhe o valor máximo entre várias heurísticas admissíveis. Por exemplo, em um problema de planejamento, você pode usar a heurística máxima entre diferentes estimativas para priorizar o pior cenário.

5. **Árvore Geradora Mínima (Minimum Spanning Tree)**:
   - Usada em problemas de roteamento de rede, a heurística da árvore geradora mínima estima o custo mínimo necessário para conectar todos os pontos de interesse. Embora não seja tão precisa quanto a distância euclidiana, ela é admissível porque a conexão direta entre todos os pontos nunca será mais barata.

6. **Redes de Comunicação (Communication Networks)**:
   - Em problemas de otimização de redes de comunicação, a heurística admissível pode estimar a largura de banda ou o número mínimo de enlaces necessários para conectar todos os dispositivos.

Lembre-se de que a escolha da heurística adequada é crucial para o desempenho do algoritmo de busca informada. Heurísticas admissíveis garantem que o algoritmo, como a busca A*, encontre soluções ótimas, desde que a heurística não superestime o custo real. Essas heurísticas são especialmente úteis em problemas de busca, planejamento e otimização, onde encontrar soluções de custo mínimo é essencial.

## COMO CRIAR HEURÍSTICA?
Criar uma heurística eficaz é um desafio, pois envolve a definição de uma função que forneça uma estimativa precisa do custo real para atingir o estado objetivo a partir do estado atual. Aqui estão algumas diretrizes gerais sobre como criar uma heurística:

1. **Compreenda o Problema:**
   - Para criar uma heurística eficaz, você deve ter uma compreensão profunda do problema que está resolvendo. Isso inclui entender as regras, restrições e características do problema.

2. **Análise de Padrões:**
   - Identifique padrões ou características do problema que possam ser usados para criar a heurística. Pergunte-se quais características são relevantes para estimar o custo.

3. **Baseie-se na Intuição:**
   - A heurística é frequentemente baseada na intuição e no conhecimento do problema. Pergunte a si mesmo quais estados parecem estar mais próximos do estado objetivo e por quê.

4. **Desenvolva uma Função Simples:**
   - Inicialmente, crie uma heurística simples e direta que use apenas algumas características do problema. Às vezes, uma heurística simples é suficiente.

5. **Teste e Refine:**
   - Teste a heurística em diferentes estados e verifique se ela fornece estimativas razoáveis. Ajuste a heurística com base nos resultados dos testes.

6. **Compare com a Solução Ótima:**
   - Se possível, compare as estimativas da heurística com o custo real em um conjunto de casos de teste. Isso ajudará a avaliar a qualidade da heurística.

7. **Considere Cenários Extremos:**
   - Verifique como a heurística se comporta em cenários extremos. Pode ser útil criar heurísticas que priorizem o pior cenário.

8. **Explore Heurísticas Combinadas:**
   - Às vezes, a combinação de várias heurísticas pode ser mais eficaz do que uma única heurística. Você pode ponderar ou combinar heurísticas para obter uma estimativa melhor.

9. **Aprenda com a Literatura e Experiências Anteriores:**
   - Pesquise trabalhos anteriores relacionados ao problema. Você pode encontrar heurísticas já propostas ou abordagens que possam inspirar a criação de sua heurística.

10. **Evite a Superestimação:**
    - Lembre-se de que a heurística deve ser admissível, ou seja, não deve superestimar o custo real. Se sua heurística superestimar o custo, a busca informada pode não encontrar a solução ótima.

11. **Reavalie e Ajuste Conforme Necessário:**
    - A criação de uma heurística eficaz muitas vezes envolve iteração e ajustes. Esteja disposto a refinar a heurística com base no desempenho real em diferentes casos.

Lembre-se de que criar uma heurística é frequentemente um processo de tentativa e erro. Nem sempre é fácil criar uma heurística perfeita, e é comum experimentar várias abordagens antes de encontrar uma que funcione bem para o seu problema específico. Também é importante lembrar que a qualidade da heurística pode afetar significativamente o desempenho dos algoritmos de busca informada, como a busca A*. Portanto, o esforço investido na criação de uma heurística precisa é frequentemente recompensado com soluções mais eficientes e otimizadas.