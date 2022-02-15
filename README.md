# AngularCalculation

# Web Page for Mathematical Calculations using Angular

## AIM:
To design a dynamic website to perform mathematical calculations using Angular Framwork

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS in component.html file

### Step 3:

Write typescript to perform the calculations.

### Step 4:

Validate the layout in various browsers.

### Step 5:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
# Rectangle
## rectangle.component.ts
```
import { Component } from "@angular/core";

@Component({
    selector:'Rectangle-Area',
    templateUrl:'./rectangle.component.html'
})
export class RectangleComponent{
    length:number;
    breadth:number;
    area:number;
    constructor(){
        this.length=0;
        this.breadth=0;
        this.area=0;


    }
    onCalculate()
    {
            this.area = this.length*this.breadth
    }
}
```
## rectangle.component.html
```
<style>
    h2{
background-color: rgb(11, 245, 245);
color: rgb(53, 138, 207);
}
.container {
  display: block;
  background-color: #8bdf97;
  min-height: 200px;
  margin-top: 100px;
}
.al{
    text-align: center;
    font-size: 25px;
}

</style>

<div class="container">
    <div class="al">
    <h2>AREA OF RECTANGLE</h2>
    Length=<input type="text"[(ngModel)]='length'>Meters<br/>
    Breadth=<input type="text"[(ngModel)]='breadth'>Meters<br/>
    <input type="button" (click)="onCalculate()" value="CalculateArea"><br/>
    Area=<input type="text" [value]="area"> Meters<sup>2</sup><br/>
</div>

</div>
```
# Cylinder
## cylinder.component.ts
```
import { Component } from "@angular/core";

@Component({
    selector:'Cylinder-Vol',
    templateUrl:'./cylinder.component.html'
})
export class CylinderComponent{
    radius:number;
    height:number;
    volume:number;
    constructor(){
        this.radius=0;
        this.height=0;
        this.volume=0;
    }
    onCalculate(){
        this.volume = 22/7*this.radius**2*this.height
    }
}
```
## cylinder.component.html
```
<style>
    h2{
background-color: rgb(11, 245, 245);
color: rgb(241, 77, 211);
}
.container {
  display: block;
  background-color: #8bdf97;
  min-height: 200px;
  margin-top: 100px;
}
.al{
    text-align: center;
    font-size: 25px;
}

</style>
<div class="container">
<div class="al">
    <h2>VOLUME OF CYLINDER</h2>
    Radius=<input type="text"[(ngModel)]='radius'>Meters<br/>
    Height=<input type="text"[(ngModel)]='height'>Meters<br/>
    <input type="button" (click)="onCalculate()" value="CalculateArea"><br/>
    Volume=<input type="text" [value]="volume"> Meters<sup>3</sup><br/>
    volume=π*r^2*h

</div>
</div>
```
# Cone
## cone.component.html
```
<style>
    h2{
background-color: rgb(11, 245, 245);
color: rgb(241, 77, 211);
}
.container {
  display: block;
  background-color: #8bdf97;
  min-height: 200px;
  margin-top: 100px;
}
.al{
    text-align: center;
    font-size: 25px;
}

</style>
<div class="container">
    <div class="al">
    <h2>VOLUME OF CONE</h2>
    Radius=<input type="text"[(ngModel)]='radius'>Meters<br/>
    Height=<input type="text"[(ngModel)]='height'>Meters<br/>
    <input type="button" (click)="onCalculate()" value="CalculateArea"><br/>
    Volume=<input type="text" [value]="volume"> Meters<sup>3</sup><br/>
    V=πr2h/3
</div>
</div>
```
## cone.component.ts
```
import { Component } from "@angular/core";

@Component({
    selector:'Cone-Vol',
    templateUrl:'./cone.component.html'
})
export class ConeComponent{
    radius:number;
    height:number;
    volume:number;
    constructor(){
        this.radius=0;
        this.height=0;
        this.volume=0;
    }
    onCalculate(){
        this.volume = 22/7*this.radius**2*this.height/3
    }
}
```
## app.component.html
```
<div class="backgd">
  <h2>MATH CALCULATION</h2>
  <div class="container">
      
<Rectangle-Area>

</Rectangle-Area>

<Cylinder-Vol>

</Cylinder-Vol>

<Cone-Vol>

</Cone-Vol>
<div class="footer">DEVELOPED BY: RAJESHKANNAN.M</div>

  </div>

</div>

```
## app.component.css
```
h2{
    text-align: center;
    color: rgb(17, 14, 39);
    margin-top: 10px;


}
.container {
    width: 800px;
    margin-left: auto;
    margin-right: auto;
  }
  .backgd{
    background-color: rgb(226, 15, 209) ;
}
  .footer{
      text-align: center;
      font-size: 30px;
      color: rgb(15, 15, 46);
      background-color: rgb(55, 152, 105);
      margin-top: 10px;
  }
```
## app.module.ts
```
import { NgModule } from '@angular/core';
import { FormsModule } from '@angular/forms';
import { BrowserModule } from '@angular/platform-browser';

import { AppComponent } from './app.component';
import { ConeComponent } from './cone/cone.cpomponent';
import { CylinderComponent } from './cylinder/cylinder.component';
import { RectangleComponent } from './rectangle/rectangle.component';

@NgModule({
  declarations: [
    AppComponent,RectangleComponent,CylinderComponent,ConeComponent
  ],
  imports: [
    BrowserModule,FormsModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }

```

## OUTPUT:
# without output

![OP1](https://user-images.githubusercontent.com/93901857/153917498-0be0651c-8d00-49ab-84be-25d62bd40222.jpg)

# with output 

![OP2](https://user-images.githubusercontent.com/93901857/153917321-e691d2ea-98bc-4084-a266-84bf7f90eb99.jpg)


## Result:
Thus a Mathmetical Calculation website is created using Angular.


