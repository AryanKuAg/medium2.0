# Notes

Incremental static regeneration
Static pages which will serve dynamic like pages

`sanity.io`

### Tech Stack
- Next.js
- TailwindCSS 3.0
- TypeScript (for strongly type checking)
- React
- Sanity CMS (will create a mini project inside your project)
- GROQ

--- 
Manually Go to `sanity.io/manage` for the dashboard </br>
Link from next.js will pre-fetch the page and make it faster </br>
`object-contain` will keep the aspect ratio of the image </br>
Anything without breakpoints like md, lg, sm will apply to mobile (mobile first design)</br>
`space-x-<number>`: for space between flex items </br>
We have two apps running-
- Next.js (front end)
- Sanity Studio (back end) (`sanity start` - this runs our local studio) MAKE SURE TO RUN THIS COMMAND INSIDE THE SANITY MINI PROJECT

Run this query on front end and pull in the information from sanity, This query is in GROQ
```
*[_type == "post"]{
  _id,
  title,
  slug,
  author -> {
    name, 
    image
  }
}
```
create `sanity.js` inside your next.js project
`npm i next-sanity` -> inside your next.js project</br>
Make `.env.local` and store your environment variables. 
</br>
Environment variables will only visible to the api of next.js, means your credentials will never get leaked to the client. </br>
`typings.d.ts`: Definition typescript file
---
You will get an error for `createImageUrlBuilder`.
Solution: https://stackoverflow.com/questions/71277628/typeerror-0-next-sanity-webpack-imported-module-0-createimageurlbuilder
---
