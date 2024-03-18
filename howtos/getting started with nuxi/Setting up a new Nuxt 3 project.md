
For prepration of  the upcoming event today I'm gonna set up a Nuxt 3 project with `Nuxi` 

Following this guide: https://vueschool.io/articles/vuejs-tutorials/getting-started-with-nuxi-nuxt-cli/


- first check node version, because Nuxt.js 3 requires `Node.js 16.11+` versions
- Node version seems to be up to date:
	- ![](images/Pasted%20image%2020240304162449.png)
- creating a new Nuxt 3 project with `nuxi init`
	- `npx nuxi init projectname`
- the command asks me to install a package:
	- ![](images/Pasted%20image%2020240304162841.png)
	- apparently I have to install `nuxi@3.10.1` first
- I'm asked which package-manager i want to choose
	- ![](images/Pasted%20image%2020240304162954.png)
	- I will pick `npm` as my package-manger
- I'm asked if I want it to be a GitHub Repo
	- ![](images/Pasted%20image%2020240304163243.png)
	- I answers yes
- apprently you can start the developement server also with `npm run dev`
	- ![](images/Pasted%20image%2020240304163344.png)
	- inside VS Code, this is how it intially looks like:
	- ![](images/Pasted%20image%2020240304163504.png)
	- I have started the dev server without problems
	- the side looks like this:
	- ![](images/Pasted%20image%2020240304163640.png)
	- now I will try something
	- `npx nuxi add component Navbar`
		- this is what I get:
		- ![](images/Pasted%20image%2020240304164026.png)
		- it also generated a `/components` directory to put it in.
	- The component is apparently already imported(?)
		- I just added it to _app.vue_ 
			- ![](images/Pasted%20image%2020240304165444.png)
	- Trying to generate a about page:
		- `npx nuxi add page about`
	- When I generated that about page, the server was restarting and I get an Error: 404
	- ![](images/Pasted%20image%2020240304165817.png)
	- my assumption is that the new page is not implemented in the `vue-router` yet
	- I created a category page with an id
		- ![](images/Pasted%20image%2020240304170717.png)
	- I cannot find the router
		- maybe I have to implement it myself
	- I had to enable vue routing via vue dev tools `Shift + Alt + D`
		-  the dev tools are toggleable
			- ![](images/Pasted%20image%2020240304172216.png)
			
	- tailwind installed: https://tailwindcss.com/docs/guides/nuxtjs
	- Pinia is the equivalent to redux
	- TypeScript is better with Composition API
	- Dynamic Routes (research)
	- Need `<NuxtPage/>` to render pages
	- Slots (research)
		- when multiple slots we need to bind the wanted slot
