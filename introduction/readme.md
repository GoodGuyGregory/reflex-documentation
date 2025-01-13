## Reflex

Reflex offers (Similar to Streamlit) over 50 prebuilt components [Component Library](https://reflex.dev/docs/library/) for you to use and express yourself with.

a basic application has **three main component**

### 1. State

the state of an application's page and elements that pertain to memory of objects and management belong within the `State` class

```python
class State(rx.State):
    albums_count: int = 0
    albums: Album[] = []
```

### 2. Event Handlers

these are what handle the changes to state and event syncronicities within your application

```python
def add_record(self):
    self.albums_count += 1

def remove_record(self):
    self.albums_count -= 1

```

### 3. User Interface (UI)

this is the fun part of development using the lego style plug and play components from the component library to form a new application from nothing in no time at all.

```python
def index():
    return rx.hstack(
        rx.button(
            "Decrement",
            color_scheme="ruby",
            on_click=State.remove_record,
        ),
        rx.heading(State.count, font_size="2em"),
        rx.button(
            "Increment",
            color_scheme="grass",
            on_click=State.add_record,
        ),
        spacing="4",
    )

```


### Related Documentation


**Tutorials**

 [Dashboard App](https://reflex.dev/docs/getting-started/dashboard-tutorial/)  
 [Chatbot App](https://reflex.dev/docs/getting-started/chatapp-tutorial/)

