import 'package:flutter/material.dart';

void main() {
  runApp(MaterialApp(
    home: Conteudo(),
  ));
}

class Conteudo extends StatefulWidget {
  const Conteudo({Key? key}) : super(key: key);

  @override
  _ConteudoState createState() => _ConteudoState();
}

class _ConteudoState extends State<Conteudo> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
        appBar: AppBar(
          title: Text("Pets"),
          centerTitle: true,
          backgroundColor: Colors.indigo[100],
        ),
        body: Container(
          width: double.infinity, //largura equivalente ao 100% do css e html
          padding:EdgeInsets.all(50), //espaçamentos dos elementcs em px e/ou dp
          decoration: BoxDecoration(
              border: Border.all(width:5, color: Colors.indigo.shade100)
          ),
          child: Center(
            child: Column( //Esta é uma coluna
              mainAxisAlignment: MainAxisAlignment.spaceEvenly, //alinhamento do main com espaços iguais
              crossAxisAlignment: CrossAxisAlignment.center, //alinhamento do main centralizado
              children: <Widget>
              [
                Padding(
                child:Image.asset("imagens/cat1.jpg"),
                padding:EdgeInsets.all(5)),
                RaisedButton(
                  child: Text(
                    "Entrar",
                    style: TextStyle(
                      color: Colors.white,
                      fontSize: 15,
                      fontWeight: FontWeight.w900,
                    ),
                  ),

                  color: Colors.indigo.shade100,
                  onPressed: (){},
                ),

                Padding(
                    child:Image.asset("imagens/dog1.jpg"),
                    padding:EdgeInsets.all(5)),
                RaisedButton(
                  child: Text(
                    "Entrar",
                    style: TextStyle(
                      color: Colors.white,
                      fontSize: 15,
                      fontWeight: FontWeight.w900,
                    ),
                  ),
                  color: Colors.indigo.shade100,
                  onPressed: (){},
                ),

                Padding(
                    child:Image.asset("imagens/cat2.jpg"),
                    padding:EdgeInsets.all(5)),
                RaisedButton(
                  child: Text(
                    "Entrar",
                    style: TextStyle(
                      color: Colors.white,
                      fontSize: 15,
                      fontWeight: FontWeight.w900,
                    ),
                  ),
                  color: Colors.indigo.shade100,
                  onPressed: (){},
                ),


                Padding(
                    child:Image.asset("imagens/dog2.jpg"),
                    padding:EdgeInsets.all(5)),
                RaisedButton(
                  child: Text(
                    "Entrar",
                    style: TextStyle(
                      color: Colors.white,
                      fontSize: 15,
                      fontWeight: FontWeight.w900,
                    ),
                  ),
                  color: Colors.indigo.shade100,
                  onPressed: (){},
                )
              ]

          )
          ),
        )
    );
  }
}
