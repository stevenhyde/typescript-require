TypeScript Require Extension
============================

This is a Node.JS `require` extension that enables requiring typescript modules without any preprocessing.

# Install
Install via npm:

    npm install typescript-require

# Use

During the boot up process of your application, require `typescript-require` once;

    require('typescript-require');

After this point, you can require any .ts module just like .js modules. `typescript-require` will find out
and compile the TypeScript file, resolving any necessary dependencies to other scripts.

# Sample

#### app.js
    // Initialize
    require('typescript-require');

    // Get functions.ts
    var funcs = require("./funcs.ts");
    console.log(funcs.lowercase("HELLO!"));

#### funcs.ts
    export function lowercase(val:string) {
        return val.toLowerCase();
    }

    export function uppercase(val:string) {
        return val.toUpperCase();
    }

You should know that;
I've been toying with TypeScript for just a couple of hours now, so I might have some weird bugs here.

Developed By
============

* Ekin Koc - <ekin@eknkc.com>

License
=======

    Copyright 2012 Ekin Koc

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.