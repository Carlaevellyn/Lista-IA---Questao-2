Lista de Inteligência Artificial - Questão 2

Integrantes:
Carla Evellyn
jhennifer kyria
Sthefany Barboza

Questão 2.1 – Sistema de Inferência (Akinator)

Descrição
Este projeto implementa um sistema inspirado no jogo Akinator, capaz de identificar personagens com base nas respostas fornecidas pelo usuário.
O sistema utiliza uma base de conhecimento composta por personagens e seus atributos armazenados em um arquivo JSON. A partir das respostas do usuário, hipóteses incompatíveis são eliminadas até que reste o personagem mais provável.

Técnica Utilizada:
Busca em Espaço de Hipóteses
Inicialmente, todos os personagens são considerados candidatos.

A cada resposta do usuário:
Os candidatos incompatíveis são removidos;
O conjunto de possibilidades é reduzido;
O processo continua até que reste apenas um personagem ou o candidato mais provável.

Base de Conhecimento:
Arquivo:
personagens.json

Cada personagem possui um conjunto de atributos, como:
humano
poder
estudante
protagonista
espada
vilao
professor
guerreiro
entre outros

Funcionalidades:
Inferência baseada em perguntas e respostas;
Eliminação automática de hipóteses;
Adição de novos personagens;
Persistência dos dados em JSON;
Interface gráfica desenvolvida com Streamlit.

Execução:
pip install streamlit
streamlit run app.py

Questão 2.4 – Sistema CBR (Case-Based Reasoning)

Descrição
Este projeto implementa um sistema de diagnóstico médico simplificado utilizando a técnica de Raciocínio Baseado em Casos (CBR).
O sistema compara os sintomas informados pelo usuário com casos armazenados previamente e sugere a solução mais semelhante encontrada.

Ciclo CBR Implementado:
Retrieve (Recuperar)
Busca os casos mais semelhantes ao problema informado.

Reuse (Reutilizar)
Utiliza o diagnóstico e tratamento do caso mais parecido.

Revise (Revisar)
Permite ao usuário informar se a solução encontrada foi adequada.

Retain (Reter)
Caso a solução não seja adequada, um novo caso pode ser adicionado à base de conhecimento.

Base de Conhecimento:
Arquivo:
casos.json

Cada caso contém:
sintomas
diagnóstico
tratamento

Método de Similaridade:
O sistema utiliza o Índice de Jaccard para comparar conjuntos de sintomas.

Fórmula:

J(A,B) = |A ∩ B| / |A ∪ B|

Onde:
A representa os sintomas informados pelo usuário;
B representa os sintomas de um caso armazenado.

O resultado é convertido para porcentagem de similaridade.

Funcionalidades:
Seleção de sintomas por checkboxes;
Busca dos casos mais semelhantes;
Exibição do Top 3 resultados;
Cálculo de similaridade;
Inclusão de novos casos;
Persistência em JSON;

Interface gráfica desenvolvida com Streamlit.

Execução:
pip install streamlit
streamlit run CBR.py

Tecnologias Utilizadas:
Python 3
Streamlit
JSON
Inteligência Artificial
Busca em Espaço de Hipóteses
Case-Based Reasoning (CBR)
