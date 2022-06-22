# pr-tica-3
prática 3


# Main.dart

```jsx
import 'package:flutter/material.dart';
import 'package:listanamoradas/screens/login.dart';
import './screens/login.dart';
import './screens/lista.dart';

void main() {
  runApp(MeuApp());
}

class MeuApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: '@Namoradas',
      home: Lista(

      ),
    );
  }
}
```

## Cadastro

```jsx
import 'package:flutter/material.dart';

class Cadastro extends StatelessWidget{
  Widget build(BuildContext context) {
    return Scaffold();
  }
}
```

## Login

```jsx
import 'package:flutter/material.dart';

class Login extends StatelessWidget{
  Widget build(BuildContext context) {
    return Scaffold(
      body: Column(
        children: [
          Icon(Icons.contact_phone, size: 72, color: Colors.black,),
          Text('Namoradas', style: TextStyle(
            fontSize: 24,
            fontWeight: FontWeight.bold,
            color: Colors.black
          ),
          ),
          TextField(
            keyboardType: TextInputType.emailAddress,
            decoration: InputDecoration(
              border: UnderlineInputBorder(),
              label: Text("Email"),
            ),
          ),
          TextField(
            keyboardType: TextInputType.text,
            obscureText: true,
              decoration: InputDecoration(
                border: UnderlineInputBorder(),
                label: Text("Senha"),
              )
          ),
          TextButton(child: Text('Entrar'),
            onPressed: () => {}
          ),
        ],
      ),
    );
  }
}
```

## lista

```jsx
import 'package:flutter/material.dart';

class Lista extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        backgroundColor: Colors.amber ,
        title: Text('@Namoradas'),
        actions: [
          IconButton(icon: Icon(Icons.exit_to_app),
            onPressed: () => {},)
        ],
      ),
      body: ListView.builder(itemCount: 5,
      itemBuilder: (BuildContext context, int index) {
        return ListTile(
          title: Text('Namorada ${index + 1}'),
          trailing: Text('(61)9 4002-8922'),
        );
      }
    ),
      floatingActionButton: FloatingActionButton(
        child: Icon(Icons.add),
        onPressed: () => {},
      ),
    );
  }
}
```

## cadastro

```jsx
import 'dart:ui';

import 'package:flutter/material.dart';

class Cadastro extends StatelessWidget {
  @override
  Widget build(BuildContext){
    return Scaffold(
      appBar: AppBar(
        title: const Text('OnlyFans'),
        backgroundColor: Colors.deepPurple,
        actions: [
          TextButton(child:const Text('Salvar',
            style: TextStyle(color: Colors.white),
            ),
            onPressed: () => {},)

            ],
            ),
      body: Column(
        children: const[
          TextField(
            keyboardType: TextInputType.phone,
            decoration: InputDecoration(
              border: UnderlineInputBorder(),
              label: Text("Fone"),
            ),
          ),
          TextField(),
        ],
      )
    );
  }
}
```
