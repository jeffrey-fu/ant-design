---
order: 0
title:
  zh-CN: 基本使用
  en-US: Basic usage
---

## zh-CN

基本使用。

## en-US

Basic usage example.

```jsx
import React, { useState } from 'react';
import { Input } from 'antd';

const MyComp = () => {
  const [query, setQuery] = useState({ v1: '', v2: '' });

  return (
    <>
      <Input
        value={query.v2}
        onChange={e => {
          console.log({ change: e.target.value });
          setQuery(prevStatus => {
            console.log({ v2: e.target.value });
            return { ...prevStatus, v2: e.target.value };
          });
        }}
        allowClear
      />
    </>
  );
};

ReactDOM.render(<MyComp />, mountNode);
```
