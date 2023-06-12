# Possible bug in astro

Encoding the percent sign in a path parameter causes an error. To reproduce:

* npm install
* npm run dev
* visit `localhost:3000`
* Enter any value containing the `%` character and submit the form.

You will see a `URI malformed` with reference to a line where `decodeURIComponent` is called.

I am rather sure that this is caused by `decodeURIComponent` being called with a value that has been previously decoded via `decodeURIComponent` or `decodeURI`.
