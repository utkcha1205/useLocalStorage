# useLocalStorage Hook

A custom React hook that provides an easy way to manage data in local
storage.

**Installation**
You can install the useLocalStorage package using npm or yarn:\
``` JSX
npm install localstorage-hook-react 
# or 
yarn add
localstorage-hook-react

```
**Usage**

Here's how you can use the useLocalStorage hook in your React
components:

```JSX 

import React from 'react'; 
import { useLocalStorage } from 'localstorage-hook-react'; 
function MyComponent() { /
    // Usage example
    const [value, setValue] = useLocalStorage('myKey', 'defaultvalue'); 
    return (
        <div> <input type="text" value={value} onChange={(e) => setValue(e.target.value)} placeholder="Enter value..." /> 
        </div> 
    ); 
    } 
export default MyComponent;

```



**API**

useLocalStorage(key: string, initialValue: any): [storedValue,
setValue]

-   key: The key to use for storing the value in local storage.

-   initialValue: The initial value to use if no value is found in local
    storage.
    Returns an array with two elements:

```{=html}
<!-- -->
```
-   storedValue: The current value stored in local storage.

-   setValue: A function to update the value in local storage.
    **Example**

    ```JSX

    import React from 'react'; 
    import { useLocalStorage } from 'localstorage-hook-react'; 
    function MyComponent() { const [count,setCount] = React.useState(0); 
    const [storedCount,setStoredCount] = useLocalStorage('count', 0);
    React.useEffect(()=> { 
        console.log('Stored count:', storedCount); 
        },[storedCount\]); 
        return ( 
            <div> <button onClick={() =>setCount((prev) => prev + 1)}> Increment </button> 
            <p>Count:{count}</p> 
            <p>Stored Count: {storedCount}</p> 
            </div> 
            ); 
        }
    export default MyComponent;
    
    
    ```
    
    **License**
    This package is licensed under the MIT License - see the
    [[LICENSE](https://chat.openai.com/LICENSE)]{.underline} file for
    details.
    **Contributing**\
    **Thank you for using debounce-hook-react. If you have any issues, suggestions, or contributions, feel free to open an issue or a pull request on the [GitHub repository](https://github.com/utkcha1205/useLocalStorage). Happy coding!**
