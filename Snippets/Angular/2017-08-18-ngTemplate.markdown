## NgForOf 指令语法
* 语法糖
```html
<li *ngFor="let item of items; index as i; trackBy: trackByFn">...</li>
```
### template语法
```html
<li template="ngFor let item of items; index as i; trackBy: trackByFn">...</li>
```
### ```<ng-template>``` 元素
```html
<ng-template ngFor let-item [ngForOf]="items" let-i="index" [ngForTrackBy]="trackByFn">
  <li>...</li>
</ng-template>
<!--等价于-->
<ng-template ngFor let-item="$implicit" [ngForOf]="items" let-i="index" 
   [ngForTrackBy]="trackByFn">
  <li>...</li>
</ng-template>
```