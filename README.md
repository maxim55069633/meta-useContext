# meta-useContext
1. ```const ThemeContext = createContext(undefined);```
Why do we set "undefined" in the createContext?
Because we don't know the theme status beforehand.

3.
```
export const ThemeProvider = ({ children }) => {
const [theme, setTheme] = useState("light");

const toggleTheme = () => {
setTheme(prevTheme => (prevTheme === "light" ? "dark" : "light"));
};
return <ThemeContext.Provider
value={{theme, toggleTheme}}
>{ children }</ThemeContext.Provider>
};
```
Why do we use double curly brackets here? 
Because an object works as a single object + javaScript object literal.
