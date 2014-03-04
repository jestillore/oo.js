oo.js
=====

Object-Oriented JavaScript

```javascript
var A = Class.create({
	constructor: function () {

	},
	abstract: {
		methods: ['walk']
	},
	properties: {
		firstname: 'Jillberth',
		lastname: 'Estillore',
		fullname: function () {
			return this.firstname + ' ' + this.lastname;
		}
	}
});

var I = Interface.create({
	methods: ['one', 'two']
});

var B = Class.create({
	constructor: function () {

	},
	extend: A,
	properties: {
		walk: function () {

		}
	}
});

var C = Class.create({
	implement: [I],
	properties: {
		one: function () {

		},
		two: function () {

		}
	}
});

var c = new C();
console.log(c instanceof I); // true
```