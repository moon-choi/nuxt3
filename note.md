* Course #5

# why use NuxtLink instead of anchor tag?
- it wil make a fresh request and set a pre-rendered page. but this is not what SPA wants. hen we output NuxtLink, there is an ability (e.g. intercept the request)
- it auto applies some classes. 

* Course 8
# universal rendering

- useFetch('api url') takes a endpoint from data
- const { data: products } = await useFetch('..')
- code runs both inside the script tag and server 
nuxt can pre run the code in the server

* Course 11
# META DATA: Default
- nuxt.config.ts
# how to overwrite?
1/ useHead ({
  title: 
  meta: [ name: . content:]
})

2/ or use nuxt component
- <template> <Head> <Title> <Meta name= "" :content="">

* Course 12
# Custome server routes
- when you don't want to expose sensitive private key when you make a request (this is required when you are using third party API)
- authentication.. 
- anything you put inside script, it will be exposed to the frontend user.
- server > api > ninja.js: should have a special function. 

export default defineEventHandler( () ==> {
  return {
    message: ``
  }
} )

const { data } = await useFetch('/api/ninja')

* Course 13
# Dynamic server routes
