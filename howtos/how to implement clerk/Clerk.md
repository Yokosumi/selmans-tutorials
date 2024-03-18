
Insert ClerkProvider

**<span style="font-size: 20px; color: blue">main.tsx</span>**

- You can import the `.env variable` with an const using `import.meta.env.NAME_OF_VARIABLE`
- Theres is a error handler implement that throws an error when theres no valid publishable key
- The `<ClerkProvider/>` is a wrapper and needs to wrap the `<App/>` 
	- In this case it wraps the `<RouterProvider/>` because it has the `<App/>` in they router file.


![](images/Pasted%20image%2020240318111429.png)