 # Project 3 with General Assembly: MERN web app.
 ## Overview
A 10 day project with three other team members, where we planned, designed and built a CRUD app using MERN stack.
My contributions in this project were the Index page and Navbar coding and styling, and copy on front and index pages. The back-end was team-coded.

 ### Tools used: 
 * MongoDB & Mongoose
 * Express
 * ReactJS 
 * Node
 * React Bootstrap
 * Git & GitHub
 
 
Our team loves teas and coffees, and to celebrate our course cohort and our diverse backgrounds, we built a service to introduce and celebrate different types and preparation methods of teas and coffees from around the world.


 ## The app: “Heiss Drinks” 
![https://raw.githubusercontent.com/daria-kafler/GA-SEI56-Project-03/main/client/src/styles/images/project02screenshot01.png](https://raw.githubusercontent.com/daria-kafler/GA-SEI56-Project-03/main/client/src/styles/images/project02screenshot01.png)

![https://raw.githubusercontent.com/daria-kafler/GA-SEI56-Project-03/main/client/src/styles/images/project02screenshot02.png](https://raw.githubusercontent.com/daria-kafler/GA-SEI56-Project-03/main/client/src/styles/images/project02screenshot02.png)

You can check it out here >>> [https://sei56-project-3.herokuapp.com/](https://sei56-project-3.herokuapp.com/)

Our team loves teas and coffees, and to celebrate our course cohort and our diverse backgrounds, we built a service to introduce and celebrate different types and preparation methods of teas and coffees from around the world.

## Approach
On this project we were 4 contributors and everything was managed with daily standups and Trello. 
The team decided to go with the ideas I suggested for the type and design of the app (inspired by the [Weezy frontpage](https://weezy.co.uk/)), and of the teammembers made a wireframe:

![home page wirefarme](https://raw.githubusercontent.com/daria-kafler/GA-SEI56-Project-03/main/client/src/styles/images/HomePage.png)
![index page wireframe](https://raw.githubusercontent.com/daria-kafler/GA-SEI56-Project-03/main/client/src/styles/images/Index%20page.png)

We pair-coded the backend set-up for CRUD functionality, and split tasks up and posted them onto the task board, and cracked on with the front-end.

![project 3 taskboard](https://raw.githubusercontent.com/daria-kafler/GA-SEI56-Project-03/main/client/src/styles/images/project3taskboard.png)

My main responsibilities were the Navbar, Index page which shows and filters the different drinks, and copy for index and frontpage. 
This was the first time I used React Bootstrap, and I really enjoyed how simply structured it was, making code more readable.

```javascript
<Container fluid sticky="top" className="nav-container-pages">
        <NavHomepage />
      </Container >

      <Container className="index-wrapper">
        <Row className="align-items-center index-hero-row">

          <Col className="index-hero-txt">
            <h2>Fresh brew</h2>
            <article>
              <p>Discover your new favourite brew with Teas and Coffees that you didnt even know existed.
                Browse our a range of tastes and preparation methods you’ll love, and choose the right new brew for you.</p>
            </article>
          </Col>

          <Col className="index-hero-img"></Col>
        </Row>

        <Breadcrumb className="show-drink-breadcrumb">
          <Breadcrumb.Item href="/">Home</Breadcrumb.Item>
          <Breadcrumb.Item active>Browse Drinks</Breadcrumb.Item>
        </Breadcrumb>
        
        <Row>
```

However, it wasn'r always perfect, and when I tried implementing the code for collapsable navbar, I just couldn't get it to work. So in that case resorted to a more Frankensetin approach, due to lack of time.

```javascript
<div className="container-fluid">
        <nav className="homepage-navbar-wrapper">
          <div className="nav-logo-div">
            <Link to="/" className="navbar-logo">
          Heiss
            </Link>
          </div>

          <div className="menu-icon" onClick={handleClick}>
            <i className={click ? 'fas fa-times' : 'fas fa-bars'} />
          </div>
          <div>
            {/* empty div for a layout oriented teen */}
          </div>
          <ul className={click ? 'nav-menu active' : 'nav-menu'}>
            <li className="nav-item">
              <Link to="/drinks" className="nav-links" onClick={closeMobileMenu}>
                Our Drinks
              </Link>
            </li>
            <li className="nav-item">
              <Link to="/heiss-room" className="nav-links" onClick={closeMobileMenu}>
                Heiss Room
              </Link>
            </li>
```

For the app copy, it was important to me the make sure users see the emphasis on the unieaquness of the drinks.

![Frontpage copy explaining about drinks service](https://raw.githubusercontent.com/daria-kafler/GA-SEI56-Project-03/main/client/src/styles/Screenshot%202021-08-12%20at%2014.42.11.png)

![Indexpage copy](https://raw.githubusercontent.com/daria-kafler/GA-SEI56-Project-03/main/client/src/styles/Screenshot%202021-08-12%20at%2014.38.11.png)


## Challenges
* When displaying the drinks on the index page, I couldn't get filtering to be both on the type of drink as well as its origin. After spending a full day on it, I had decided to limit the filtering options:

![Screenshot of commented out code](https://raw.githubusercontent.com/daria-kafler/GA-SEI56-Project-03/main/client/src/styles/images/Screenshot%202021-08-10%20at%2016.15.39.png)

* Our team had some trouble working on styling. We chose to all work on the `main.scss` file, but didn't forsee just how accurate we would need to get with tags and class names, so ended up overwriting each other's styling.
After a couple of days to allow everyone to sort their targeting in the styling file, we nominated one person to edit and amend the file, while having everyone together on Zoom and making sure everyone understands the changes and is happy with them.
Thankfuly, SASS allows nesting!

```index-wrapper.container {
  .sorting-row-wrapper.container {
    margin: 0 30px;
    display: flex;
  }
  .sorting-buttons {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    padding-right: 50px;
    button {
      padding: 5px 10px;
      width: 100px;
      border: none;
      background-color: white;
      color: $primaryBrown;
      border-right: $primaryBrown;
      font-family: 'raleway', sans-serif;
      font-size: 1.2em;
    }
    button:hover {
      // text-decoration: underline;
      border-bottom: 2px solid $primaryBrown;
      transition: all 0.2s ease-out;
    }
```

## Individual Wins
* Successfully advocated for overall idea and design while making sure all contributors were happy and felt heard.
* To lead during standups to make sure individual tasks are clear and team members are meeting self-imposed deadlines. 
* Fixed a design element that's been stumping the team for a few days, where we couldnt get the zig-zag seperator to cover all screen sizes:

![Screenshot of horizontal break line too short](https://raw.githubusercontent.com/daria-kafler/GA-SEI56-Project-03/main/client/src/styles/zigzagshort.jpg)

We didn't have any knowledge on SVG and treated SVG files as simple image files, which didn't help. I dove into SVG documentation and examples, and was able to fix the zig-zag line so it covers to full screen. The shape now lost its rounded edges, and I plan to come back and fix that as well in the future. 

![Screenshot of horizontal break line fixed](https://raw.githubusercontent.com/daria-kafler/GA-SEI56-Project-03/main/client/src/styles/zigzagfixed.png)



## Bugs
* When checking out default screen should be 'Oops, thing isn't possible yet' instead of 'Successful!'.
* Error for Login with unregistered email should be 'User/email not found'.
* Submit function isn't working when registering or logging in.
* Basket can only be reached via the 'checkout' button on a specific drink. Needs to also link from the navbar.

## Future features
* Fix bugs.
* Filter drinks by origin.
* Improve styling.

## Key takeaways
* Our team was too excited to get to coding, when we could have taken more time to plan out the front-end.
* Figma is a great tool and I should learn to use it!
* Working in a team is a fantastic learning experience- Not only in communicating and accomodating others, but also learning to accept others help and support.
* Deadlines help to adopt a 'good enough' mentality vs 'need to make it perfect' (which risks not shipping anything at all).

## Acknowledgements
[Bex Jones](https://github.com/simplythebex) 🧡
[Victoria Olanipekun](https://github.com/victoriaolanipekun) 🧡
[Ole Nascimento](https://github.com/eintrittfrei)
