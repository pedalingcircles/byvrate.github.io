
In PowerShell

`docker pull jekyll/jekyll`

Runs the Jekyll container
`docker run --rm --volume="$(Get-Location):/srv/jekyll" -it jekyll/jekyll jekyll new .`

Builds Jekyll
`docker run --rm --volume="$(Get-Location):/srv/jekyll" -it jekyll/jekyll jekyll build`

Serves Jekyll locally
`docker run --name blog --volume="$(Get-Location):/srv/jekyll" -p 3000:4000 -it jekyll/jekyll jekyll serve --watch --drafts`

Drafts don't really run that well, better to restart if changes are needed
`docker restart blog`

