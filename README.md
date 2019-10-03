# React-Native-TextInput-Height-Auto-Up
React Native TextInput Height Auto Up

![image](https://raw.githubusercontent.com/slackhq/SlackTextViewController/master/Screenshots/slacktextviewcontroller_demo.gif)

# Create State
```
constructor(props) {
    super(props);
    this.state = {
    text: '', //Create State
    height: 0 //Create State
    };
  }
  ```
  # Retrun in class
  
```
 <TextInput
        {...this.props}
        multiline={true}
        onChange={(event) => {
          this.setState({
            text: event.nativeEvent.text,
            height: event.nativeEvent.contentSize.height,
          });
        }}
        style={[styles.default, {height: Math.max(35, this.state.height)}]}
        value={this.state.text}
      />
 ```
 
 # StyleSheet
 
 ```
  default: {
      textAlign: 'center',
      width: '90%',
      marginBottom: 7,
      height: 40,
      borderWidth: 1,
      borderColor: '#075e54',
      borderRadius: 5 ,
  },
 ```
