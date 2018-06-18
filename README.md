# Demo floating action button widget

This is a demo app show at FlutterDevs (06/13/2018)

## Steps

- Create a new Flutter project

`$ flutter create demo_flutter_button_widget`

- Open project on IDE (VS Code)

`$ cd demo_flutter_button_widget`
`$ code .`

- Comment out flutteractionbutton from initial app

```java
      // floatingActionButton: new FloatingActionButton(
      //   onPressed: _incrementCounter,
      //   tooltip: 'Increment',
      //   child: new Icon(Icons.add),
      // ), // This trailing comma makes auto-formatting nicer for build methods.
```

- Add new widget

```java
// Creating a Floating Action Button widget here
class MyButton extends StatelessWidget {
  final VoidCallback onPressed;
  final Widget child;
  MyButton(this.onPressed, this.child);

  @override
  Widget build(BuildContext context) {
    return Material(
      type: MaterialType.circle,
      elevation: 12.0,
      color: Colors.green,
      child: InkWell(
        onTap: onPressed,
        child: Container( width: 50.0, height: 50.0, child:child),
      ),
    );
  }
}
```

- Add new floating action button

```java
      floatingActionButton: MyButton(_incrementCounter, new Icon(Icons.add)),
```