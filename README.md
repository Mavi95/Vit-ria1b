Pular para reproduzir esboço

Biscoitos

O Editor p5.js usa cookies. Alguns são essenciais para a funcionalidade do site e permitem que você gerencie uma conta e preferências. Outros não são essenciais — eles são usados ​​para análises e nos permitem aprender mais sobre nossa comunidade. Nunca vendemos esses dados ou os usamos para publicidade. Você pode decidir quais cookies deseja permitir e saber mais em nossa Política de Privacidade .

Permitir todosPermitir Essencial

Aula 08 - Jogo Pongpor EstudanteAlura

ArquivoNovoSalvarExemplosEditarCódigo arrumadoEncontrarEsboçoAdicionar ficheiroAdicionar pastaConfiguraçõesPreferênciasLinguagemAjudaAtalhos do tecladoReferênciaSobre

esboço.js

1

//variáveis ​​da bolinha

2

deixe xBolinh a = 100 ; 

3

deixe yBolinha = 200 ;

4

deixe diametro = 22 ;

5

deixe raio = diametro / 2 ;

6

​

7

//variáveis ​​do oponente

8

deixe xRaqueteOponente = 585 ;

9

deixe yRaqueteOponente = 150 ;

10

​

11

//velocidade da bolinha

12

deixe velocidadeXBolinha = 6 ;

13

deixe velocidadeYBolinha = 6 ;

14

​

15

//variáveis ​​da raquete

16

deixe xRaquete = 5 ;

17

deixe yRaquete = 150 ;

18

deixe raqueteComprimento = 10 ;

19

deixe raqueteAltura = 90 ;

20

​

21

//placar do jogo

22

deixe meusPontos = 0 ;

23

deixe pontosDoOponente = 0 ;

24

​

25

​

26

deixe colidiu = falso ;

27

​

28

configuração de função () {

29

 criarCanvas ( 600 , 400 );

30

}

31

​

32

função draw () {

33

   fundo ( 0 );

34

   mostraBolinha ();

35

   movimentaBolinha ();

36

   verificaColisaoBorda ();

37

   mostraRaquete ( xRaquete , yRaquete );

38

   movimentaMinhaRaquete ();

39

   verificaColisaoRaquete ( xRaquete , yRaquete );

40

   verificaColisaoRaquete ( xRaqueteOponente , yRaqueteOponente );

41

   mostraRaquete ( xRaqueteOponente , yRaqueteOponente );

42

   movimentaRaqueteOponente ();

43

   incluirPlacar ()

44

   marcaPonto ();

45

}

46

função mostraBolinha () {

47

 círculo ( xBolinh a , yBolinha , diametro );


48

}

49

​

50

função movimentaBolinha () {

