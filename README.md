# React
Aprendendo

3 Coisas a saber sorbe STATE -> setState()

1 - Nao modifique o State diretamente
  Errado -> this.state.comment = 'hello world'
  Certo - > this.setState({comment: 'hello world'});
  
2 - State updates devem ser assincronos
  Mesmo que this.props e this.state possam ser assincronos, voce nao deve confiar no valor deles para calcular o proximo valor.
  // Wrong
    this.setState({
      counter: this.state.counter + this.props.increment,
    });
  // Correct
    this.setState((state, props) => ({
      counter: state.counter + props.increment
    }));
    
3 - State updates are Merged
