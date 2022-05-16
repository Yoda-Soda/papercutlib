# hugo-alpine-bookshop-template

Starter template for hugo, alpine, bookshop

# Prerequisites

-   Hugo [install](https://gohugo.io/getting-started/installing/). `brew install hugo`
-   Go [install](https://go.dev/learn/). `brew install go`
-   Requires Node >=16 [install](https://nodejs.org/en/)

# Quickstart

1. In the terminal at the root dir, run: `npm i`
2. Start site and bookshop: `npm run dev` OR site alone: `npm run start`

-   By default bookshop live browser will be at : [http://localhost:30775/](http://localhost:30775/)
-   By default the site will be at : [http://localhost:1313/](http://localhost:1313/)

# Create New component

`npm run init` and follow prompts 

- When creating a component, assign the class name to a variable. This makes it easier to maintain and edit classes if they need to be adjusted. Example:

	```
	{{ $c := "c-slideshow" }}

	<div class="{{$c}}">
	    <div class="{{$c}}__slides">
	    </div>
	</div>
	```

- Classnames should use the [BEM naming convention](http://getbem.com/). Example:

	```
	{{ $c := "c-button" }}
	<a class="{{$c}} 
			  {{$c}}--{{ .ButtonVariant | urlize }}"
		href="{{ .LinkUrl }}"
	   {{ if .OpenInNew }}
	       target="_blank"
	   {{ end }}>
	   	<span class="{{$c}}__label">{{ .ButtonLabel }}</span>
	</a>
	```

- CSS variables should be utilitsed for any values that are re-used throughout the theme. Add them to `assets/css/variables.scss`
