Step 1:
You need to install @angualr/cli at global level;
npm install @angular/cli -g

Step 2:
Using angualr CLI we will be doing initalising project directory
ng new <PROJECT-NAME> --style=scss --routing;
ng new ng4-training-project --style=scss --routing

--styles=scss, means we want CSS to use the Sass compile;
-routing, includes the default routing scaffolding.


STEP 3:
Configuring bootstrapModule
npm install --save @ng-bootstrap/ng-bootstrap

//Include Bootstart Root Module
import {NgbModule} from '@ng-bootstrap/ng-bootstrap';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    NgbModule.forRoot(), ...
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }

//For other modules
import {NgbModule} from '@ng-bootstrap/ng-bootstrap';

@NgModule({
  declarations: [OtherComponent, ...],
  imports: [NgbModule, ...]
})
export class OtherModule {
}
