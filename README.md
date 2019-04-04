![freeCodeCamp Social Banner](https://s3.amazonaws.com/freecodecamp/wide-social-banner.png)

# The freeCodeCamp Guide
React and Redux: Manage State Locally First

class DisplayMessages extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: '',
      messages: []
    }
  }
  // add handleChange() and submitMessage() methods here
  handleChange(event){
      this.setState({
        input: event.target.value
      })
  }

  submitMessage(){
    this.setState({
      messages: this.state.messages.concat(this.state.input),
      input: ''
    })
  }

  render() {
    return (
      <div>
        <h2>Type in a new Message:</h2>
        { /* render an input, button, and ul here */ }
          <input value={this.state.input} onChange={this.handleChange.bind(this)} />
          <button onClick={this.submitMessage.bind(this)}>Add message</button>
          <ul> 
          {
            this.state.messages.map((message)=><li>{message}</li>)
            }
          
          </ul>

        { /* change code above this line */ }
      </div>
    );
  }
};
