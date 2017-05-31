# prial
currency formating library for javascript based on [rialjs](https://github.com/habibpour/rial.js) by [saeid habibpour](https://github.com/habibpour).

## installation
### npm
`npm install prial --save`

### yarn
`yarn add prial`

## api

### Rial
```
import { Rial } from 'prial'
//or es5 model
const Rial = require('prial').Rial

const rial = new Rial({
	decimal : ",",
	alphabet : "fa",
	currency : "هزار ریال",
	cut : 3,
});

rial.get("425420000000");
// ۴۲۵,۴۲۰,۰۰۰ هزار ریال

rial.Alphabet("en").Currency("ریال").Cut(0).get("425420000000");
// 425,420,000,000 ریال

rial.Decimal(".").Alphabet("en").Currency("").Cut(0).get("۴۲۵,۴۲۰,۰۰۰");
// 425.420.000
```

### formatToman
```
import { formatTooman } from 'prial'
//or es5 model
const formatToman = require('prial').formatToman

formatToman('123456')
// 123,456 تومان
```
