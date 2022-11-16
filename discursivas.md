# Questões discursivas ✍

## Não corrija

---

## Git e Github:

### **Questão 1:** O que são sistemas de controles de versões? Por que são importantes?

Os sistemas de controle de versão ajudam a rastrear e gerenciar alterações feitas no código fonte de um software.\
Após algum tempo de desenvolvimento de um software podemos ter problemas como:

- Diversas pessoas tentando alterar um ou mais arquivos ao mesmo tempo;
- Uma alteração feita em parte do sistema que quebra outra;
- Modificação não intencional de algum arquivo;

Os sistemas de controlede verssão podem prevenir esses tipos de problemas e muitos outros.

### **Questão 2:** Qual a diferença entre o Git e o GitHub? Como eles estão relacionados? É possível usar um sem o outro?

Git é o Sistema de gerenciamento de versões e Github é um serviço baseado em nuvem que hospeda o git.
O git pode funcionar sem o github, o contrário não acontece.

### **Questão 3:** O Git é um sistema distribuído de controle de versões. O que significa isso?

# ?

---

## Modelo lógico:

### **Questão 4:** Existem alguns errinhos no projeto HR ilustrado acima (principalmente em relação às cardinalidades dos relacionamentos e em relação à obrigatoriedade das chaves estrangeiras). Identifique quais são esses erros, explique o que está errado e conserte os erros se for necessário.

Algumas chaves estão configuradas como "NOT NULL" no PK mas estão como "NULLABLE" no FK da outra tabela.

### **Questão 5:** Alguma tabela do projeto representa um relacionamento do tipo N:N? Se sim, identifique a tabela e explique porque é um relacionamento N:N; Se não, explique porque não há relacionamentos N:N neste projeto.

# ?

### **Questão 6:** Pelo projeto apresentado é possível que um determinado empregado seja o gerente de zero, um ou mais departamentos. Se eu quisesse impor uma regra que diz que um empregado só pode ser gerente de, no máximo, um departamento, o que eu teria que fazer no projeto? O que eu teria que criar no banco de dados para impor essa restrição? Por quê?

# ?

### **Questão 7:** Por que os relacionamentos entre as tabelas estão representados com linhas pontilhadas? O que isso representa? Por que foi representado assim?

Representa uma relação não identificada, é quando a chave primária da table pai não se torna uma chave primária na tabela filha. Foi representado dessa forma para que não haja uma dependência entre as duas tabelas fazendo com que a tabela filha não seja identificada pela chave primária da tabela pai.

### **Questão 8:** Qual é o único tipo de relacionamento que pode guardar dados? Por quê? Existe algum relacionamento assim nesse projeto? Se não existir, você suge-riria trocar alguns dos relacionamentos existentes para melhorar o projeto?

N:N. Esse tipo de relacionamento cria uma tabela intermediária. Suge-riria trocar o relacionamento departamentos_empregados para um do tipo N:N.

### **Questão 9:** Explique o relacionamento da tabela empregados com ela mesma? É um erro? É correto? Por quê?

É correto. Um surpervidor é um funcionário que é responsável por outros empregados. Se o funcionário não for um supervisor, ele não será o FK_id_supervisor de nenhum empregado.

---

## Questões sobre a implementação no PostgreSQL:

### **Questão 10:** Qual a diferença entre banco de dados, usuário e esquema no Post-greSQL?

O bando de dados do postgres é uma coleção de esquemas. Os esquemas por sua vez armazenam as coleções de dados (tabelas, funções, views, indexes etc).

### **Questão 11:** Por que um esquema é importante?

Ele agrupa dados em um namespace comum criando assim uma representação lógica amigável do conjunto de dados.

### **Questão 12:** Se você não definir um esquema específico, onde os objetos do banco de dados (tabelas, relacionamentos, dados, etc.) serão gravados? Isso é bom ou ruim? Por que?

No schema "public". Ruim, pode ocasionar colisão de nomes.

### **Questão 13:** Agora que você já implementou o projeto no PostgreSQL, tem alguma sugestão de melhoria a fazer para o projeto? Como ele poderia ser melhorado?

Adicionando uma relação N:N entre as tabelas empregados e departamentos.

### Questão 14: Faça uma comparação dos SGBD que você utilizou. Quais as vantag-nes e desvantagens de cada um? Quem tem a melhor documentação?

O Mysql tem uma melhor documentação tanto no suporte oficial quanto online em fórums.

### Questão 15: Como você acha que foi seu desempenho neste PSet? Como você foi buscando as informações necessárias e lendo as documentações dos SGBD? Você aproveitou a oportunidade e buscou ajuda dos monitores? Até o próximo PSet pessoal!

Ruim. Mal tive tempo de realizar o trabalho.
