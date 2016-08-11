#### laprogiosrxswift
######Observable sequences
```
let observable = Observable.of(1,2,3)
observable.subscribe{
  print($0)
}
```
or
```
[1,2,3].toObservable().subscribe{print($0)}
```

let disposeBag = DisposeBag()

[1,2,3].toObservable().subscribeNext{print($0)}.addDisposableTo(disposeBag) //only print 123
[1,2,3].toObservable().subscribeCompleted{print($0)}.addDisposableTo(disposeBag) //only print completed
