

![image](https://github.com/JasonDontw/ToDoList/blob/master/display.gif)



## DOM
## 1. 有State數據
## 2. 有JSX模板
## 3. 數據+模板結合，生程實體的DOM，來顯示
## 4. State發生改變
## 5. 數據+模板結合，生程實體的DOM，替換原始的DOM

## 缺點:
##  每次都要生成一個完整的DOM，非常耗性能，且替換原始的DOM也耗性能

## DOM改良
## 1. 有State數據
## 2. 有JSX模板
## 3. 數據+模板結合，生程實體的DOM，來顯示
## 4. State發生改變
## 5. 數據+模板結合，生程實體的DOM，不直接替換原始DOM
## 6. 新DOM和原始DOM做比對，找差異
## 7. 找出變化地方
## 8. 只使用新DOM中的變化元素，去替換原始DOM的元素

## 比較:
## 雖然改良步驟較多，但整個DOM替換所需性能較大，比對後替換會相對好一點，但不多

## React 虛擬DOM方案
## 1. 有State數據
## 2. 有JSX模板
## 3. 數據+模板結合，生成虛擬DOM(一個JS的描述，一個Object或陣列，用來描述實體的DOM)
##    ['div' , {id : 'abc'} , ['sapn' , {} , 'hello world']] 
## 4. 使用虛擬DOM，生程實體的DOM，來顯示
##    <div id='abc'><span>hello world</span></div>
## 5. State發生改變
## 6. 生成新的虛擬DOM 
##    ['div' , {id : 'abc'} , ['sapn' , {} , 'bye bye']] 
## 7. 比較虛擬DOM的差異 
## 8. 直接改便原始DOM的差異地方

## 比較:
## 在JS中生成一個JS描述，所需性能是極小的，所以在第6步用虛擬DOM取代了實體DOM的生成，提升極大性能
## 且在第7步JS之間的比較也比DOM之間的比較性能損耗大大降低




