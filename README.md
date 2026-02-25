## Github Pages for React App:

1.	`npx create-react-app my-app`
2. 	`cd my-app`
3. 	`git init`
4. 	`git remote add origin https://github.com/{username}/{repo-name}.git`
5. 	`git add .`
6. 	`git commit -m "added files"`
7. 	`git push origin main`

8. 	`npm install gh-pages --save-dev`
9. 	Go to package.json ->

      (i). Add a homepage property in this format*:
          https://{username}.github.io/{repo-name}
   	
      eg:
   	  ```
   	    {
   	        "name": "my-app",
   	        "version": "0.1.0",
   	        + "homepage": "https://{username}.github.io/{repo-name}",
            "private": true
        }
   	  ```
      (ii). Add a predeploy property and a deploy property to the scripts object
   	  
      eg:
   	  ```
   	  "scripts": {
                + "predeploy": "npm run build",
                + "deploy": "gh-pages -d build",
                "start": "react-scripts start",
                "build": "react-scripts build"
              }
      ```
11. `npm run deploy -- -m "Deploy React app to GitHub Pages"`

12. Setup github pages for the repo. Set the branch to 'gh-pages'
