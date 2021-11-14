## Benchmark for Laravel Docker/Sail based apps

The present repo is a clone of the source code for **"Build a Voting App"** 
series on Laracasts: https://laracasts.com/series/build-a-voting-app.
This great project is used to measure the performance of different computers with the goal
of finding the ideal and most efficient laptop for PHP Web Developers.

## Requirements

You need Docker Desktop or Docker with docker-compose already installed and running
for the following steps to work. It's important that the benchmarks are run in a Docker
environment because most modern web development is done like this.

## Installation

1. Clone this repo (laravel_docker_benchmark) and `cd` into it
1. Rename or copy `.env.example` file to `.env`
1. `chmod +x ./build.sh`
1. `./build.sh`
1. `alias sail='[ -f sail ] && bash sail || bash vendor/bin/sail'`
1. `sail up -d`
1. `sail artisan key:generate`
1. `sail artisan migrate`
1. `sail npm install`
1. `sail npm run dev`

## Run Benchmarks
1. `sail artisan db:seed` Take note of the time reported at the end (it's seconds)
1. `sail artisan test` Take note of the time reported at the end

## Try out the app
1. Visit `http://localhost` in your browser if you're curious about the app itself.
