---
title: 'React Rating Component'
date: '2022-11-15'
link: "https://www.npmjs.com/package/react-rating-comp?activeTab=versions"
---

# Getting Started with Rating component
 This component is basically to take the opinins or experiance from the user.
A basic rating component which supports Disabled Mode, Read only  and Interactive mode with default Star Icon and Custom Icons

##  Demo

![](https://cdn.pixabay.com/animation/2022/12/03/11/57/11-57-35-512_512.gif)

## Codesandbox Examples
[Code Sand box Examples](https://codesandbox.io/s/wizardly-water-rg1o5i?file=/src/App.js)

##  Install
  npm i react-star-rating-component
## `Usage`

```jsx
    <Rating
        iconType={"IoIosStar"}
        emptyIconType={"IoIosStarOutline"}
        rating={rating}
        setRating={(value) => setRatingValue(value)}
    />
    <Rating
        iconType={"IoMdHeart"}
        emptyIconType={"IoMdHeartEmpty"}
        rating={rating}
        setRating={(value) => setRatingValue(value)}
        numberOfIcons={10}
    />
    <Rating
        iconType={"IoMdHeart"}
        emptyIconType={"IoMdHeartEmpty"}
        rating={rating}
        setRating={(value) => setRatingValue(value)}
        numberOfIcons={10}
        emptyIconStyle={{color: "red"}}
        filledIconStyle={{color: "red"}}
    />
```


## `Example`
```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Rating from "react-rating-comp/src";

class App extends React.Component {
  constructor() {
    super();
    this.state = {
      rating: 1
    };
  }

  onClick(value) {
    this.setState({rating: value});
  }

  render() {
    const { rating } = this.state;
    
    return (                
      <div>
        <h2>Rating from state: {rating}</h2>
        <Rating
          iconType={"IoMdHeart"}
          emptyIconType={"IoMdHeartEmpty"}
          rating={rating}
          setRating={(value) => this.onClick(value)}
          numberOfIcons={10}
          emptyIconStyle={{color: "red"}}
          filledIconStyle={{color: "red"}}
        />
      </div>
    );
  }
}

ReactDOM.render(
  <App />, 
  document.getElementById('app')
);
```