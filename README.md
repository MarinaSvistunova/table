<!DOCTYPE html> 
<html> 
  <head> 
    <title>Валюты - таблицы</title> 
    <meta charset="utf-8"><style> 
    table {width: 70%; border: 1px solid; padding: 15px; border-radius: 20px} 
    th {font-weight: bold} 
    th, td {padding: 10px; font: normal 20px sans-serif} 
    th {text-align: left; background: rgb(90,90,90); color: white; border-radius: 10px} 
    tr:nth-child(odd) {background : #CCC} 
    </style> 
  </head> 
  <body> 
    <script src="/j/out"></script> 
    <script src="/j/dblttl"></script> 
    <script>{ console.clear(); 
              const URL = 'https://kodaktor.ru/j/rates'; 
              
              const h = ['Валюта', 'Продажа', 'Покупка']; 
              const f = document.createDocumentFragment(); 
              const t = document.createElement('table'); 
              const td = document.createElement('td'); 
              const th = document.createElement('th'); 
              const tr = document.createElement('tr');
             for (let i = 0; i < 7; ++i){
                if (i === 0) {
                  for (let k = 0; k < 3; ++k){ 
                    const th = document.createElement('th'); 
                    const td = document.createElement('td');
                    const txt = document.createTextNode(h[k]); 
                    th.appendChild(txt); 
                    td.appendChild(th);
                    t.appendChild(td);
                    f.appendChild(t); 
                  }      
                } else {
                  const tr = document.createElement('tr'); 
                   for (let k = 0; k < 3; ++k){ 
                   // const tr = document.createElement('tr'); 
                    const td = document.createElement('td');
                    const txt = document.createTextNode(h[k]); 
                    td.appendChild(txt); 
                    //td.appendChild(tr);
                    tr.appendChild(td);
                     t.appendChild(tr);
                  
                    f.appendChild(t); 
                  }    }
              
              }
               document.body.appendChild(f); 
          /* for (let k = 0; k < 3; ++k){ 
               const tr = document.createElement('tr'); 
                for (let j = 0; j < 3; ++j){ 
                 
                  const txt = document.createTextNode(h[j]); 
                  td.appendChild(txt); 
                  tr.appendChild(td); 
                } 
                t.appendChild(td); 
                f.appendChild(t); 
              }*/
              //document.body.appendChild(f); 
              
              /* 
              let li = document.createElement('li'); 
              li.innerHTML = 1; 
              parent.appendChild(li); */ 
    }</script> 
  </body> 
</html>
