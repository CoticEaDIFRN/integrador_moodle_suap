Estas instruções descrevem como fazer a instalação correta do Plugin "Suap-Edu-Webservice".
Esse plugin é desenvolvido e suportado pela equipe de desenvolvimento da COTIC IFRN EaD.
Plugin desenvolvido baseado no módulo Enrollment block, by Symetrix.

Pré-requisitos:
============
Você irá precisar no mínimo de:

1.  Um servidor rodando Moodle 2.0, ou superior;

2.  Um navegador com suporte ao Javascript;

Instalação:
============
Estas instruções assumem que o Moodle já esta instalado no seu servidor (/var/www/moodle).

1.  Descompacte o arquivo e copie para a pasta /var/www/moodle/blocks;


2.  Faça login no seu ambiente Moodle como usuário administrador;

	O próprio Moodle irá identificar a nova instalação e apresentará a tela para a continuação do processo.


4.  Clique no botão para fazer a instalação;


5.  Clieque no botão "Continuar";

	A partir deste ponto você já poderá adicionar o bloco do "Suap-Edu-Webservice".

Banco de dados:
============
O banco de dados deve ser um pouco modificado, com a adição das seguintes colunas:

1. Na tabela "mdl_course_categories" adicionar coluna "id_suap"
	Comando sql: ALTER TABLE  `mdl_course_categories` ADD `id_suap` VARCHAR(100) NULL ;

2. Na tabela "mdl_course" adicionar coluna "id_suap"
	Comando sql: ALTER TABLE  `mdl_course` ADD  `id_suap` VARCHAR(100) NULL ;

3. Na tabela "mdl_course_categories" adicionar coluna "custom_css"
	Comando sql: ALTER TABLE  `mdl_course_categories` ADD `custom_css` TEXT NULL ;

Fim
============

Categories

1. Campus (sigla) [EAD]
   1. Modalidade (????) [TSUB?]
     1. Curso (código) [15121]
        1. Oferta (ano.semestre) [2018.2]
           1. *Turma (código: anosemestre.periodo.curso.turma) [20182.4.15121.1E]

Courses

1. Diário (código: anosemestre.periodo.curso.turma.modalidade.componente) [20182.4.15121.1E.TSUB.0025]
   1. Enrollment [função no diário][Aluno, professor, tutor, etc..]
   2. Group (Nome do pólo) [Natal]
