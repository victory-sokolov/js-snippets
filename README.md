# JavaScript snippets
Various reusable JavaScript snippets


### Generate random number in a given range
```javascript
const getRandomNumber = (min, max) => Math.round(Math.random() * (max - min) + min);

getRandomNumber(2, 10)
```

### Generate random HEX color

```javascript
const hex = '#'+(Math.random()*0xFFFFFF<<0).toString(16);
```

### Generate uuid

```javascript
const uuid = () => Date.now().toString(36) + Math.random().toString(36).substr(2);

uuid(); // ky34p5wacqyn2xu7su
```

## Objects

### Omit specific keys from object

```javascript
const omit = (obj, ...props) => {
  const filteredArray = Object.entries(obj).filter(([key, value]) => !props.includes(key));
	return Object.fromEntries(filteredArray);
}

omit(obj, "name", "age"); // return obj with salary

```

### Pick specific keys from object
```javascript
const pick = (obj, ...props) => {
  const filteredArray = Object.entries(obj).filter(([key, value]) => props.includes(key));
	return Object.fromEntries(filteredArray);
}

pick(obj, "name", "age"); // return obj with name and age
```
