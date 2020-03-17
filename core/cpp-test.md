# Teste de admissão para Retail Intelligence Core

## Descrição do teste

O teste de admissão será implementar [filtro de sobel](https://en.wikipedia.org/wiki/Sobel_operator) para a detecção de contornos em imagens arbitrárias.

## Requisitos de funcionamento

O programa deverá funcionar a partir da linha de comando, com a seguinte interface: `./< nome do programa > [ --exportar-grayscale ] < caminho para a imagem >`. Todas as imagens de entrada deverão ser no formato PNG e será necessária uma mensagem de erro para formatos inválidos. As imagens de saída serão a imagem resultante do filtro de sobel, nomeada `< nome da imagem original >_sobel.png`, e a imagem original em grayscale, nomeada `< nome da imagem original >_grayscale.png`, caso a flag `--exportar-grayscale` esteja presente; ambas as imagens deverão ser salvas na mesma pasta da imagem original, com as mesmas dimensões da imagem original.

## Requisitos técnicos

O projeto deverá ser escrito em C++14. A leitura da imagem deverá ser feita através da STL, sendo o uso da mesma aprovado e incentivado para o restante do projeto, não será aceita a leitura através de bibliotecas de terceiros ou stdio. Poderão ser usadas bibliotecas de terceiros para operações matriciais ([armadillo](http://arma.sourceforge.net/), [eigen](http://eigen.tuxfamily.org/index.php?title=Main_Page) ou outras), aplicação de testes unitários ([gtest](https://github.com/google/googletest), [catch2](https://github.com/catchorg/Catch2) ou outra) e leitura dos parâmetros da linha de comando.

O projeto deverá ser gerenciado através de [cmake](https://cmake.org/) (versões 1.13 ou superior) e deverá ter testes unitários integrados com a ferramenta [CTest](https://gitlab.kitware.com/cmake/community/-/wikis/doc/ctest/Testing-With-CTest). O programa deverá contar com testes unitários o filtro de sobel, os testes deverão executar o filro sobre segmentos de imagem de pelo menos duas vezes o tamanho do kermel do filtro e comparar as saídas do mesmo com resultados pré calculados. Os segmentos de imagem dos testes unitários não precisam representar imagens reais.

## Modo de entrega

O projeto deverá ser entregue através de um público repositório no github e deverá possuir com um arquivo `README.md` possuindo instruções detalhadas para a instalação das dependências, compilação do programa e execução dos testes unitários. O projeto deverá se licenciado através da licensa [MIT](https://opensource.org/licenses/MIT).
