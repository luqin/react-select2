# react-select2

Wrapper for [Select2](https://select2.github.io/)

[![NPM version][npm-badge]][npm] [![Build Status][travis-ci-image]][travis-ci-url]

[![Dependency Status][deps-badge]][deps]
[![devDependency Status][dev-deps-badge]][dev-deps]
[![peerDependency Status][peer-deps-badge]][peer-deps]

## Installation

```
npm install react-select2 --save
```

## Usage

### Basic usage

```js
import Select2 from 'react-select2';
…

<Select2
  multiple
  data={['bug', 'feature', 'documents', 'discussion']}
  options={
    {
      placeholder: 'search by tags',
    }
  }
/>
```

### Data as an object

```js
<Select2
  data={[
    { text: 'bug', id: 1 },
    { text: 'feature', id: 2 },
    { text: 'documents', id: 3 },
    { text: 'discussion', id: 4 },
  ]}
  options={{
    placeholder: 'search by tags',
  }}
/>
```

### Callbacks

```js
<Select2
  multiple
  data={['bug', 'feature', 'documents', 'discussion']}
  onOpen={this.cbOpen}
  onClose={this.cbClose}
  onSelect={this.cbSelect}
  onChange={this.cbChange}
  onUnselect={this.cbUnselect}
  options={{
    placeholder: 'search by tags',
  }
}
/>
```

### Default value

```js
<Select2
  defaultValue={2} // or as string | array
  data={[
    { text: 'bug', id: 1 },
    { text: 'feature', id: 2 },
    { text: 'documents', id: 3, disabled: true },
    { text: 'discussion', id: 4 },
  ]}
  options={{
    placeholder: 'search by tags',
  }}
/>
```

### Default multiple value

```js
<Select2
  multiple
  defaultValue={[1, 4]}
  data={[
    { text: 'bug', id: 1 },
    { text: 'feature', id: 2 },
    { text: 'documents', id: 3 },
    { text: 'discussion', id: 4 },
  ]}
  options={{
    placeholder: 'search by tags',
  }}
/>
```

### Value

Also possible to change the current value using `value` property

```js
const { value } = this.props;
…
<Select2
  value={ value }
  data={[
    { text: 'bug', id: 1 },
    { text: 'feature', id: 2 },
    { text: 'documents', id: 3, disabled: true },
    { text: 'discussion', id: 4 },
  ]}
  options={{
    placeholder: 'search by tags',
  }}
/>
```

### Option Groups

```js
<Select2
  multiple
  data={[
    { text: 'Development',
      children: [
        { text: 'bug', id: 1 },
        { text: 'feature', id: 2 },
      ],
    },
    { text: 'documents', id: 3 },
    { text: 'discussion', id: 4 },
  ]}
  options={{
    placeholder: 'search by tags',
  }}
/>
```

### Parent element for dropdown

```js
<Select2
  options={{
    dropdownParent: '#element'
  …
```

### Properties

You can pass any properties such as `class`, `id`, `data-*` attributes

```js
<Select2 className="selector" … />
```

### Access to select2

You can access to select2 as follows
```js
// assign a ref attribute
<Select2 ref="tags" />
// somewhere in your code, access via `this.refs`
this.refs.tags.el
```

## Themes

Default theme in [css/select2.css](css/select2.css)

```js
import 'react-select2/css/select2.css';
```

## Development

- Run webpack-dev-server
  ```
  npm run start
  ```

- Run webpack in watch mode
  ```
  npm run watch
  ```

- Run webpack for build
  ```
  npm run build
  ```


[npm-badge]: http://badge.fury.io/js/react-select2.svg
[npm]: https://www.npmjs.com/package/react-select2

[deps-badge]: https://david-dm.org/luqin/react-select2.svg
[deps]: https://david-dm.org/luqin/react-select2

[dev-deps-badge]: https://david-dm.org/luqin/react-select2/dev-status.svg
[dev-deps]: https://david-dm.org/luqin/react-select2#info=devDependencies

[peer-deps-badge]: https://david-dm.org/luqin/react-select2/peer-status.svg
[peer-deps]: https://david-dm.org/luqin/react-select2#info=peerDependencies 

[travis-ci-image]: https://travis-ci.org/luqin/react-select2.svg
[travis-ci-url]: https://travis-ci.org/luqin/react-select2
