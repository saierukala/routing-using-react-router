## Web Apps

* Web Apps are of two types, based on how we get content:

* Multi-page application (MPA)
* Single-page application (SPA)

# Multi-page application (MPA)

* Every URL is associated with corresponding resources (HTML, CSS, JS).
The browser downloads these resources when you access them or navigate between URLs.

#  Single-page application (SPA)
 
* All URLs are associated with a single HTML page.
On navigating we only get the additional content (Component - HTML, CSS, JS).

#  Advantages of using Single-page application (SPA)

* Faster Page loading - since they load only necessary Component (HTML, CSS, JS) resources on subsequent requests.
React is mainly used to build Single-page applications.
------------------------------------------------------------------------

 # React Router

 * In React, we build Single-page applications using React Router.

* To implement routing, React Router provides various components:

* BrowserRouter
* Link
* Route
* Switch

# BrowserRouter

* To add routing wrap all the Components with BrowserRouter

# Syntax:

<BrowserRouter>
  <Component 1>
  <Component 2>
  ... 
</BrowserRouter>
-----------------------------------------------------------------------

# Link

Link Component creates hyperlinks that allows to navigate around in application.


# Syntax:

<Link to="Path"> Display Text</Link>

The to prop specifies absolute path.
------------------------------------------------------------------------


# Route

The Route component renders specific UI component when path matches current URL.

<Route path="Path" component={Component} />
------------------------------------------------------------------------

#  Exact

Renders the route if path matches exactly the current url

<Route exact path="Path1" component={Component1} />
------------------------------------------------------------------------

#  Switch

The Switch component will only render the first route that matches the path. If no path matches, it renders the Not Found component.

<Switch>
  <Route path="Path1" component={Component1} />
  <Route path="Path2" component={Component2} />
 <Route component={NotFound} />
</Switch>
------------------------------------------------------------------------

# react-router-dom


import { BrowserRouter, Route, Switch } from 'react-router-dom'
import Header from './components/Header'
import Home from './components/Home'
import About from './components/About'
import Contact from './components/Contact'
import NotFound from './components/NotFound'

const App = () => (
  <BrowserRouter>
    <Header />
    <Switch>
      <Route exact path="/" component={Home} />
      <Route exact path="/about" component={About} />
      <Route exact path="/contact" component={Contact} />
      <Route component={NotFound} />
    </Switch>
  </BrowserRouter>
)

export default App
------------------------------------------------------------------------
