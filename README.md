# react_redux_concept
describe nitty-gritty concept of react and redux library

# React 
  - what is React?
    - js library for user interfaces
      - encapusulation and increase reusability
      - state management of each component
        - alternative redux
        - less flexible
## HOCs, render props
  - HOCs: a function 
      - with render props, Hocs play a role of direct client of the component which has render props and return the component as return value.
  - render props: function prop to render another component. 
     - a component which has render props holds additional functionality (cross cutting concern) and render wrapped component together.
## Performance
  - reconiliation: how react decide mount/umount/update component when comparing virtual dom and actual dom 
  - Component and PureComponent and shouldComponentUpdate method
  - Immutability: 
    - immutable data structure
      - structure sharing:
      - trie:
    - as a result, reduce time complexity O(N), linear, to O(logN)
# Redux
  - state management
    - read state
    - update sate
  - flow 
    1. implement container component esp mapStateToProps and mapDispatchToPorps (hocs)
    2. associate dispatch to event handler
    3. dispatch action caused by event handler
    4. the action is sent to root reducer
    5. the root reducer deligate the action to specific case reducers
    6. the root reducer return updated state
    7. mapStateToProps of every container component is called to apply the new state
    8. update the associated dumb components
  - reducer
    - root reducer
    - slice reducer
    - handler: object to map actions and case reducer 
    - case reducer
# Thunk
  - middleware of redux
  - detect if action is function not object
  - if action is function, thunk call the function so that you can call any asynch stuff or handle multiple actions.
