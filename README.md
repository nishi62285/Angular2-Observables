# Angular2-Observables
basic observables in angular2
source = Rx.Observable.create(observer => {
setTimeout(function(){ observer.next('Tom')}, 10000);
setTimeout(function(){observer.next('Tom')}, 8000);
setTimeout(function(){ observer.next('Hary') }, 20000);
  });

source.subscribe(value=>{ console.log(value)},error=>{console.log('error') },()=>{console.log('completed')})


const secondsObservable = new Observable((observer) => {       
    let i = 0;
    setInterval(() => {
        observer.next(i++);
    }, 1000);
});

secondsObservable.subscribe(value => console.log(value));
