# Github pages project site
theme from scratch

https://pages.github.com/



# Github pages limitations
one site per GitHub account and organization,
and unlimited project sites

https://pages.github.com/

Types of GitHub Pages sites
three types of GitHub Pages sites: project, user, and organization
Project sites are connected to a specific project hosted on GitHub
User and organization sites are connected to a specific account on GitHub.com

publish a user site, you must create a repository owned by your personal account that's named <username>.github.io
publish an organization site, you must create a repository owned by an organization that's named <organization>.github.io
one user or organization site for each account on GitHub
Project sites, whether owned by an organization or a personal account, are unlimited

GitHub Pages source repositories have a recommended limit of 1 GB. For more information, see "About large files on GitHub"
Published GitHub Pages sites may be no larger than 1 GB.
GitHub Pages deployments will timeout if they take longer than 10 minutes.
GitHub Pages sites have a soft bandwidth limit of 100 GB per month.
GitHub Pages sites have a soft limit of 10 builds per hour. This limit does not apply if you build and publish your site with a custom GitHub Actions workflow

https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages

File size limits
GitHub blocks files larger than 100 MiB
files beyond this limit, you must use Git Large File Storage (Git LFS

If you attempt to add or update a file that is larger than 50 MiB, you will receive a warning
If you add a file to a repository via a browser, the file can be no larger than 25 MiB

https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github


Repository size limits
recommend repositories remain small, ideally less than 1 GB, and less than 5 GB is strongly recommended

https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github




# Three.js Installation

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8">
<script async src="https://unpkg.com/es-module-shims@1.8.0/dist/es-module-shims.js"></script>

<script type="importmap">
  {
    "imports": {
      "three": "https://unpkg.com/three@0.156.1/build/three.module.js",
      "three/addons/": "https://unpkg.com/three@0.156.1/examples/jsm/"
    }
  }
</script>
		<style>
			body { margin: 0; }
		</style>
	</head>
	<body>
		<script type="module" src="reponame/main.js"></script>
	</body>
</html>
```

index.html we'll need to add an import map defining where to get the package
Put the code below inside the <head></head> tag, after the styles
import maps are not yet supported by some major browsers, we include the polyfill es-module-shims.js

replace <version> with an actual version of three.js, like "v0.149.0"
most recent version can be found on the npm version list

host these files at URL where the web browser can access them
to deploy your web application, push the source files to your web hosting provider
no need to build or compile anything
keep the import map updated with any dependencies (and dependencies of dependencies!)
IMPORTANT: Import all dependencies from the same version of three.js, and from the same CDN

three.js components — such as controls, loaders, and post-processing effects — are part of the addons/
Addons do not need to be installed separately, but do need to be imported separately

https://threejs.org/docs/#manual/en/introduction/Installation
