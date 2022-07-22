# ego.js

```ts
import { Model, Entity, String } from "ego";

const Todo = new Entity<string>({
  name: new String(),
});

const model = new Model({
  Todo
});

const readTodo = model.usecase({
  operation: "read",
  target: model.Todo({
    name: include("name"),
  }),
});
```
