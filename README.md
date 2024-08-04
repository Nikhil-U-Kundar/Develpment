// /* Write a program to find roots of a quadratic equation in C++*/
// #include <bits/stdc++.h>
// using namespace std;
 
// void findRoots(int a, int b, int c)
// {
//     if (a == 0) {
//         cout << "Invalid"; return; } int d = b * b - 4 * a * c; 
//         double sqrt_val = sqrt(abs(d)); if (d > 0) {
//         cout << "Roots are real and different \n";
//         cout << (double)(-b + sqrt_val) / (2 * a) << "\n"<< (double)(-b - sqrt_val) / (2 * a);
//     }
//     else if (d == 0) {
//         cout << "Roots are real and same \n";
//         cout << -(double)b / (2 * a);
//     }
//     else // d < 0
//     {
//         cout << "Roots are complex \n";
//         cout << -(double)b / (2 * a) << " + i" << sqrt_val<< "\n" << -(double)b / (2 * a) << " - i" << sqrt_val;
//     }
// }
 
// // Driver code
// int main()
// {
//     int a = 1, b = 4, c = 4;
   
//     findRoots(a, b, c);
//     return 0;
// }


::::::::::use effect:::::::::::::::
useEffect(()=>{
    prevstate=input;
},[input])  
here-----> [input] is dependendies


// ::::::::::: context api and use context:::::::

create contetx:: used to to create the context
provider:: wrapping od data will takes place

:::::::::;::::::::::;;The Context API :::::::::::::::::
provides a means to share values like state, functions, or any data across the component tree withou
 passing props down manually at every level. 

:::::::::::how to create context::::::::::::
   
syntax::  const AppState= createContext();
example:: const AppData= useContext(AppState)
replacement of context api we are using use context


:::::::::::::::useRef HOOK::::::::::::::::::::

1. mutable value can be stored  which dont allow to rerendering ...
2. by using this dom elements are directly accesed
 ref::refer the documentation...


:::::::Important::::::::::::::


import { useEffect } from "react";


////////////////fetching of the api
useEffect(()=>{
    async function getData(){
        const call= await fetch(" API link is pasted here");
        const res= await call.json();
        console.log(res);
        SetData(res);
    }
    getData();
},[])


////////////////to mapping  from the above api

{Data.map((element,index)=>{
    return <h1 key={index}>{element.firstname}</h1>
})}


:::::::::::::::::::::::::Use memo  Hook::::::::::::::::

when the problem occured that the user page became slow due to some large calculation 
we are going with the usememohook---
   -> used for memorize the values we says when to runn 
   ->memorize is done in storage
   -> prevent from unnecessary writing or calling..
syntax:
usememohook(()=>{
   ............
},[])  
here-----> [] is dependendiesi

:::::::::::Spread Operator::::::::::::::::::::::::
The JavaScript spread operator (...) 
allows us to quickly copy all or part of an existing array or object into another array or object

::::::::::::use call back::::::::::::
 ->fuction memorize is done here -- prevents from rerendering again and again


::::::::::::::::::operator:: React loaders and toastify::::::::::::::::::::
 
toastify is usedb y by important by using theby the package
useEffect(()=>{
    setloading(true);
    async function getData(){
        const res=await fetch(");
        const finalres=await res.json();
        SetData(finalres);
        setloading(false);
        toast.error("sucessfuly fetched the data");
            }
            getData();
},[])


:::::::::::::::::::::::::::class componentsin React:::::::::::::::::::::::::::::::::::
 life cylce methods
 mounting: creating  a component
 componentDidMount(){

 }


 update: growth of commponent
  componentDidUpdate(){

 }
 unmounting: death of the components
 componentDidUnMount(){

 }


 this is used in class based component(this.props)

 :::::::::::::::::::state::::::::::::::::::
state={
    name:"nikhil,
    age:12
    }
    render(){
        return(
            <.>
            <h1>class components</h1>
            <h1>{this.state.name}</h1>
            <h1>{this.state.age}</h1>
            </>
        )
    }
