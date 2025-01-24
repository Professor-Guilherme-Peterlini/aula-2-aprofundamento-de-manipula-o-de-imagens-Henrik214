# Questionário Teórico: Processamento de Imagens com Python

## Instruções
* Responda todas as questões de forma clara e concisa
* Justifique suas respostas quando solicitado
* Tempo estimado: 45 minutos

## Questões

### Parte 1: Conceitos Básicos

1. (2,0 pontos) Explique a diferença entre os métodos de redimensionamento de imagem:
   * Nearest Neighbor
   * Bilinear
   * Bicubic

   R:Nearest Neighbor é rapido, mas com imagem pixel.
   Bilinear é mais suave, e com borões.
   Bicubic é muito suave e detalhado, mas é lento. 
   
2. (1,5 pontos) Por que é importante fazer backup das imagens originais antes de aplicar transformações? Cite dois cenários onde isso é crítico.
R:1 pode perde a qualidade da imagem.
2 pode erra na edição da imagem.
### Parte 2: Escala de Cinza

3. (2,0 pontos) Compare os dois métodos de conversão para escala de cinza vistos em aula:
   * Média simples dos canais RGB
   * Método por luminosidade (Y = 0.299R + 0.587G + 0.114B)
   
   Por que o segundo método é considerado mais preciso para a percepção humana?

R: Média simples trata todas as cores iguais, mas o verde é mais importante para o olho humano.
Luminosidade da mais atenção ao verde, que é o que vemos como mais brilhante.

4. (1,5 pontos) Em processamento de imagens, por que frequentemente convertemos uma imagem para escala de cinza antes de aplicar outros algoritmos?

R: É mais rápido e focado nas informações de brilho, que são mais importantes para muitas tarefas, como detecção de bordas e análise de formas.

### Parte 3: Detecção de Bordas

5. (2,0 pontos) Explique o funcionamento dos seguintes operadores de detecção de bordas:
   * Sobel
   * Prewitt
   * Laplaciano

6. (1,5 pontos) Na função `pipeline_processamento()` implementada, por que aplicamos equalização de histograma antes da detecção de bordas?
R:Equalização de histograma melhora o contraste e faz as áreas claras ficarem mais claras e as escuras mais escuras.
Detecção de bordas encontra as mudanças de brilho na imagem. Se a imagem tem baixo contraste, as bordas ficam difíceis de ver.
### Parte 4: Aplicação Prática

7. (2,0 pontos) Considere o seguinte trecho de código:
```python
img_bordas = img_equalizada.filter(ImageFilter.FIND_EDGES)
img_final = img_bordas.point(lambda x: 255 if x > limiar else 0)
```
   * Qual o propósito da segunda linha?
   * Como a escolha do valor de limiar afeta o resultado final?

8. (2,5 pontos) Descreva um pipeline completo para:
   * Detectar bordas em uma imagem com ruído
   * Justifique cada etapa do processo
   * Explique como você escolheria os parâmetros


## Bônus (1,0 ponto extra)
Proponha uma modificação no pipeline de processamento que poderia melhorar os resultados em imagens com baixo contraste.
---
**Autor**: [Guilherme Tavares]  
**Data**: [24/01/2025]  
**Versão**: 1.1
