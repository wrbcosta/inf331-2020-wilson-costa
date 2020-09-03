# Tarefa 1

![Detalhamento de componentes e interfaces](images/tarefa01.png)

# Tarefa 2

Link para o projeto no Codepen: [React 03 - Componente Barra](https://codepen.io/wrbcosta/pen/WNwZgLE)

## HTML
~~~html
<div id="root"></div>
~~~

## JavaScript
~~~~javascript
class Barra extends React.Component {
  render() {
    let resultado = "";
    for (let b = 1; b <= this.props.tamanho; b++)
      resultado += this.props.estilo;
    return resultado;
  }
}

const elemento = <div>
                   <h2>O dinossauro</h2>
                   <Barra tamanho="20" estilo="+"/>
                   <h2>pulou na lama.</h2>
                 </div>
ReactDOM.render(elemento, 
        document.getElementById("root"));

