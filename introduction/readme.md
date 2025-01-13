## Reflex

Reflex offers (Similar to Streamlit) over 50 prebuilt components [Component Library](https://reflex.dev/docs/library/) for you to use and express yourself with.

a basic application has **three main component**

### 1. State

the state of an application's page and elements that pertain to memory of objects and management belong within the `State` class

```python
class State(rx.State):
    count: int = 0
    
```

