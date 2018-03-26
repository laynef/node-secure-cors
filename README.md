# Secure CORS

## Installation
`npm i -S secure-cors`

## Why Secure CORS
    Use secure CORS because it gives errors when you use wild cards for origins.
    Allowing any wild cards in your CORS allows you to use your server with any domain under that wildcard.
    Be sure to specify the exact urls you need.

    const express = require('express');
    const cors = require('secure-cors');

    const app = express();

    app.use(cors({
        origin: 'https://www.example.com' // never '*' or '*.example.com'
    }));

    app.listen(3000);