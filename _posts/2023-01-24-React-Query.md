---
layout: post
title:  React Query, React Hook Form
image: 
  path: /assets/img/blog/jeremy-bishop@0,5x.jpg
description: >
  Version 9 is the most complete version of Hydejack yet.
  Modernized design, big headlines, and big new features.
categories: React
sitemap: false
---

## React Query

useMutation 

- 단순 get이 아닌 Update/delete관련



## React Hook Form

useForm() 

- resgiter

- [공홈]: https://react-hook-form.com/api/useform/register	"공홈 문서"

### TS Support

[SubmitHandler]: https://react-hook-form.com/ts#SubmitHandler

예시

```javascript
import React from "react";
import { useForm, SubmitHandler } from "react-hook-form";

type FormValues = {
  firstName: string;
  lastName: string;
  email: string;
};

export default function App() {
  const { register, handleSubmit } = useForm<FormValues>();
  const onSubmit: SubmitHandler<FormValues> = data => console.log(data);

  return (
    <form onSubmit={handleSubmit(onSubmit)}>
      <input {...register("firstName")} />
      <input {...register("lastName")} />
      <input type="email" {...register("email")} />

      <input type="submit" />
    </form>
  );
}
```

