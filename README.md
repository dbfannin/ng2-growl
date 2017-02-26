# NG2 Growl

NG2 Growl is a module that displays growl like messages

## Dependencies
 * @angular/common
 * @angular/core
 * ng2.logger
 
## Installation
```shell
npm install --save ng2-growl
```

Once installed you need to import our main module:
```js
import {GrowlModule} from 'ng2-growl';
```

The only remaining part is to list the imported module in your application module, passing in a config to intialize the logger.

```js
@NgModule({
  declarations: [AppComponent, ...],
  imports: [GrowlModule.forRoot({...}), ...],
  bootstrap: [AppComponent]
})
export class AppModule {
}
```

## Usage

To use NG2 Growl, you will need to add it to your an application html file

```angular2html
<ng2-growl></ng2-growl>

```
  
 
Import the service
 
 ```typescript
import {GrowlService} from 'ng2-growl';

```

Intect the service
```typescript
  constructor(private growlService: GrowlService) {  }

```

 
Then call one of the methods
 
 ```typescript
this.growlService.addError(`You're Error message goes here`);
this.growlService.addError({heading: 'Oops', message: 'an error has occured'});


```
