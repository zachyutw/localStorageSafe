# zach-local-storage-safe

> power up window localStorage, with obj, array, string support, initialize data type, expire time.

[![NPM](https://img.shields.io/npm/v/zach-local-storage-safesvg)](https://www.npmjs.com/package/react-use-is-scrolled-into-view) 
[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Table of Contents

- [Install](#install)
- [Quick Start](#quick-start)
- [Usage](#usage)
  - [`Individual components`](#inview)
- [FAQ](#faq)
- [Thanks](#thanks)
- [Contributing](#contributing)
- [License](#license)

## Install

```bash
# Yarn
yarn add zach-local-storage-safe

# NPM
npm install --save zach-local-storage-safe
```

## Quick Start

```jsx
//
// Individual components
//
import {useState,useCallback} from 'react';
import locaslStorageSafe from 'zach-local-storage-safe';
const Example = () => {
    const [state,setState] = useState(locaslStorageSafe.getItem('myState','object') );
    const _onClick = useCallback((e)=>{
            const id = e.target.getAttribute('data-id');
             const data = {id};
             locaslStorageSafe.setItem('myState',data,30000);
            setState(()=>data)
    },[])
    return (
        <div onClick={_onClick}  data-id={state.id}>
            Test
        </div>
    );
};
```

## Usage

## Related projects

## Thanks
This repo was setup with the help of the excellent [`create-react-library`](https://www.npmjs.com/package/create-react-library) and [`redux-react-hook`](https://github.com/facebookincubator/redux-react-hook/blob/master/README.md).

## Contributing
Zach Yu zachyu.tw@gmail.com

## License

MIT 