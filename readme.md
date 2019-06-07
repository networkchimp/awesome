# Awesome Cloudflare Workers

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of awesome articles & code for [Cloudflare Workers](https://workers.cloudflare.com/).  They are similar to [browsers' Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API), but in the cloud--flare.

Inspired by the [awesome](https://github.com/sindresorhus/awesome) list.  (A bit different, since the CSV dump contains many other links that didn't make the 'awesome' list, but are still very good to look into.  Perhaps someday I'll make a seperate website for all those, but until then I have a script to build this 'best of' list.)

Please use the [Suggestion Form](https://airtable.com/shr1cr5TqmnwuQU3W) to add an URL to this list.  Use Issues only to fix something, suggest a new catgory, tag, etc.

## Contents

 - [Official](#official)
 - [Boss](#boss)
 - [Article](#article)
 - [GraphQL](#GraphQL)
 - [Local-dev](#local-dev)
 - [Localization](#localization)
 - [Security](#security)
 - [Tool](#tool)
 - [Msc](#msc)
 - [Related](#related)


## Official

- [Wrangler: offiical CLI tool](github.com/cloudflare/wrangler) [WASM,CLI,tool,Rust] ([annoucement blog post](blog.cloudflare.com/just-write-code-improving-developer-experience-for-cloudflare-workers/#wrangler-the-official-workers-cli)) available via `npm` & `cargo`, can build & deploy JS, Rust, & C/C++ projects via templates
- [Official Documentation](developers.cloudflare.com/workers/about/) [article,JS] general docs, includes configuration, Cf KV, and recipes
- [Official Blog](blog.cloudflare.com/tag/workers/) [article] Cloudflare's blog posts tagged 'worker'

## Boss

- [Diving into Technical SEO](blog.cloudflare.com/diving-into-technical-seo-cloudflare-workers/) [article,optmimize,SEO,TypeScript] modifying incomming & outgoing requests, inject Hreflang tags,, redirects, etc
- [Serverless PWA using React](github.com/cloudflare/workers-react-pwa-example) [article,ReactJS,JS] ([Cloudflare article builds up example script](blog.cloudflare.com/serverless-pwa-react-cloudflare-workers/)) terraform deploy srcipt included
- [Serverless Meetup with Cloudflare](www.heavybit.com/library/blog/serverless-meetup-with-cloudflare/) [video,JS] ([cued to examples of CFWorker usage](youtu.be/kGeu2GzyVKw?t=473)) several talks describing CfWorkers
- [image shrinking with WebAssembly](github.com/cloudflare/cloudflare-workers-wasm-demo) [optmimize,image,WASM,C] image resizing that runs on Cloudflare's edge network

## Article

- [URL shortener with LavaRand](github.com/obezuk/cf-workers-link-shortener) [route,app,JS] ([short blog post](levi.lol/url-shortener-built-on-cloudflare/)) url shortener built with Cloudflare Workers and LavaRand
- [FSharp tutorial](github.com/jbeeko/cfworker-web-api) [app,F#] FSharp example: CRUD contact manager
- [API gateway / redirect](github.com/jamesbibby/cloudflare-api-gateway) [REST,proxy,JS] ([diagramed article on use case](bibs.codes/posts/cloudflare-worker-api-gatway/)) reverse proxy layer to improve performance (HTTP1 vs HTTP2)
- [Supercharge Google Fonts](medium.com/@pierluc/supercharge-google-fonts-with-cloudflare-and-service-workers-25c37462fb6a) [optmimize,CDN,JS] ([author's live site](www.jirafe.io/)) inlines font requests with CfWorker, then caches in browser
- [Cryptocurrency API Gateway using Typescript+Workers](github.com/stevenpack/cryptoserviceworker) [gatekeeper,route,TypeScript] ([blog post at CloudFlare](blog.cloudflare.com/cryptocurrency-api-gateway-typescript-workers/)) mini http request routing, then gateway to multiple crypto API providers in 1 file
- [Maintenance Mode static page](www.resdevops.com/2018/03/20/cloudflare-workers-maintenance-mode-static-page/) [static,JS] includes PowerShell script to toggle

## GraphQL

- [Apollo Server Cloudflare & Prisma Concept](gitlab.com/travis-projects/cloudflare-workers-graphql-server) [JS] uses apollo-server-cloudflare to create a GraphQL server on Cloudflare Workers, and it also uses graphql-request to connect to a Prisma server
- [Hasura GraphQL Cloudflare Worker](github.com/nathanwaters/hasura-cloudflare-worker) [auth,JS] Example for Facebook-based authorization and GraphQL proxy queries with Hasura
- [GraphQL on Edge Workers](github.com/cloudflare/workers-graphql-gateway-example) [video,JS] ([video demo of GaphiQL app at Cloudflare](youtu.be/E9sDH6ylQc4)) Workers GraphQL Gateway Example

## Local-dev

- [Serverless framework Blueprint](github.com/signalnerve/serverless-cloudflare-workers-blueprint) [Serverless,tool,deploy,JS] configure your `.env`, & `serverless deploy` away
- [Run Cloudflare Worker scripts locally](github.com/dollarshaveclub/cloudworker) [tool,JS] uses Docker, nice API, includes WASM build support
- [Codeship to automatically update your Cloudflare Workers](github.com/karllhughes/workers-codeship-example) [deploy,example,JS] Automated Deployment

## Localization

- [Serve cookie consent banner to EU visitors](github.com/pioug/cookie-choice) [inject,app,JS] ([live demo](github.com/stevenpack/cryptoserviceworker)) banner only shows if cllient is in EU

## Security

- [Set Google Analytics Client ID Cookie](gist.github.com/dustinrecko/9f34969250f2e0668d4c4fe4808520a7#file-worker-snippet-js) [article,analytics,JS] ([article: Google Analytics ITP 2.1 Prevention ](omr.ruhr/google-analytics-itp-2-1-prevention-http-set-cookie-snippet-182092779d40)) Fool Wbkit's Intelligent Tracking Prevention,  HTTP Set-Cookie /snippet/
- [Workaround Cloudflare 1 Anti-DDoS Protection](github.com/hrbrmstr/cfhttr) [tool,Rust] Workaround Cloudflare Anti-DDoS Protection

## Tool

- [Local cloudflare-workers-kv](github.com/bitquant/cloudflare-workers-kv) [KV,local-dev,JS] Workers KV in your local environment or within a CF Workers env.  Chunks large values above 64kB
- [KV interactive viewer](github.com/jroyal/cloudflare-workers-kv-viewer) [CLI,JS] nice CLI tool to explore keys & values of a Cloudflare account
- [CF KV Client for .NET](github.com/aozd4v/cloudflare-workers-kv-dotnet-client) [KV,.NET] .NET Standard 1.4-2.0
- [cloudflare-worker-local](github.com/gja/cloudflare-worker-local) [test,JS] test a Cloudflare Worker Locally
- [Kv Web Explorer](github.com/bcnzer/kv-explorer-ui) [VueJS,KV,JS] Vue.js SPA for viewing Cloudflare KV data
- [Cloudflare Workers Time Tests](github.com/EverlastingBugstopper/cf-workers-benchmark) [test,JS] Example development environment with three patterns for benchmarking Cloudflare edge workers
- [echo](github.com/lebinh/cloudflare-workers#workers-zoo) [test,TypeScript] echo back the request/response from worker point of view

## Msc

- [x-host: override host proxy](github.com/pmeenan/cf-workers/tree/master/xhost) [proxy,JS] includes Chrome plugin.  mimics WebPageTest's overrideHost command for local testing. Rewrite all requests to a different host while adding an x-Host header
- [proxies-on-cloudflare](github.com/GitbookIO/proxies-on-cloudflare) [proxy,loadbalance,TypeScript] proxies for Friebase & Mixpanel, simple routing, fallbacks, etc
- [simple todo list app using KV & 2 workers](github.com/signalnerve/cloudflare-workers-todos) [app,frontend,KV,JS] ([live demo](todo.kristianfreeman.com/)) includes static HTML, get & put workers
- [app to flip images](github.com/Kellel/image_flipper) [app,image,WASM,Rust] uses Rust's wasm-pack-template
- [tools for creating an app](github.com/postlight/cloudflare-worker-app-kit) [tool,Preact,TypeScript] build & deploy scripts
- [go/WASM AMP-transformer](github.com/gabbifish/amp-transform-wasm) [AMP,WASM,GoLang] go/WASM port of the AMP packager transform library
- [Streaming Optimizations](github.com/pmeenan/cf-workers/tree/master/streaming-optimizations) [optmimize,cache,JS] caches 3rd party scripts & dynamic HTML, inlines Google Fonts CSS.  Non-streaming blocking [version is avaiable](github.com/pmeenan/cf-workers/tree/master/optimization-pack) for the rare cases flushing is needed
- [Blue / Green Deployments](github.com/DigitalOptimizationGroup/blue-green-cloudflare-workers) [test,deploy,proxy,JS] ([live demo - read repo for instruction](edge-stack.org/)) implementing Canary releasing and A/B testing, release versioning,bash scripts for deploying, uses cookies to lock in version
- [simple integration to Cloudflare Workers APIs](github.com/jspies/cloudflare-workers-toolkit) [tool,deploy,JS] deploy workers, get & remove routs, KV storage, etc
- [Writing an API at the Edge with Workers and Cloud Firestore](blog.cloudflare.com/api-at-the-edge-workers-and-firestore/) [article,app,GCS,JS] uses Google's Cloud Firestore for storage & JWT for authentication
- [Serverless JavaScript App Servers](codeburst.io/100-app-servers-for-5-per-month-2560d5d2f46e) [article,template,route,JS] ([related: flag a client as malicious](apility.io/2018/03/14/cloudflare-workers-example-apility/)) app tutorial, includes routing
- [Airtable Proxy Cloudflare Worker](github.com/portable-cto/airtable-proxy-worker) [AirTable,REST,security,JS] Hides Airtable Base ID and API Key, Limit requests to specific methods and table, push updates via Travis-CL
- [rtouting middleware](github.com/bitquant/cloudflare-workers) [route,tool,JS] basic routing handlers
- [hashing service](github.com/windbirds/workers_examples/blob/master/hash/index.js) [service,JS] JSON responce with SHA1, SHA286, SHA384, & SHA512 hash responce
- [Preact Progressive Web App](github.com/DigitalOptimizationGroup/cloudflare-worker-preact-pwa) [frontend,optmimize,Preact,JS] ([Preact worker demo](growthcloud.io/)) example PWA created by preact-cli
- [Wasabi CDN cheap website](github.com/mraerino/cdn-static) [static,CDN,TypeScript] serves static website from wasabi.com's cheap cloud storage
- [Thin wrapper for Cloudflare Workers KV](github.com/Zertz/cloudflare-kv) [KV,JS] get, put, & delete for Cloudflare KV
- [CI/CD pipeline for CfWorkers using Serverless in Azure](medium.com/gettimely/how-to-set-up-ci-cd-pipeline-for-cloudflare-workers-using-serverless-framework-in-azure-devops-aka-1e904e91e130) [article,CI/CD,Serverless] walkthough for a code pipeline with Serverless Framework
- [CI/CD with Azure](github.com/daniel-simpson/Cloudflare-Enterprise-Workers) [deploy,JS] 
- [DNS lookup and dig app](github.com/matthewgall/beta.dnsjson.com) [app,frontend,JS] ([dnsjson.com - live app](beta.dnsjson.com/)) 

## Related

- [Awesome Service Workers](github.com/TalAter/awesome-service-workers#awesome-service-workers-) [article] CfSW are based on browser SW