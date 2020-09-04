# Lab 5
Tarefas do laboratório 5 - Renato César Alves de Oliveira

## Tarefa 1
![Diagrama de Subcomponentes](images/subcomponentes_checkout.jpg)

## Tarefa 2
Link para o projeto no Codepen: [Tarefa 2 React - Dinossauro Codepen](https://codepen.io/renato2808/pen/KKzXeMB)

**HTML**
~~~html
<div id="root"></div>
~~~

**JavaScript**
~~~javascript
function Button(props) {
    return <button className="button" onClick={props.onClick}>
      {props.value}
    </button>;
}

class Dinossauro extends React.Component {
  constructor(props) {
    super(props);
    this.options = ["Pulou na lama", "Pulou no lago.", "Pulou no mar."];
    this.state = "";
  }
  
  renderOption(i) {
    return <Button value={this.options[i]}
             onClick={() => this.handleClick(i)} />;
  }
  
  handleClick(i) {
    if (i == 0){
      this.setState({state: "O dinossauro está sujo."})
    }
    
    if (i == 1){
      this.setState({state: "O dinossauro está molhado."})
    }
    
    if (i == 2){
      this.setState({state: "O dinossauro se afogou."})
    }
  }
  
  render() {
    let status;
    status = this.state.state;
          return (
                 <div className="dinossauro">
                   <h2>O dinossauro (clique em uma ação):</h2>
                   {this.renderOption(0)}
                   {this.renderOption(1)}
                   {this.renderOption(2)}
                   <div className="status">
                      <br></br>
                      <div>{status}</div>
                   </div>
                 </div>
            );
  }
}

ReactDOM.render(<Dinossauro />, 
        document.getElementById("root"));
~~~
