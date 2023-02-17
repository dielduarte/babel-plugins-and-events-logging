# Visitor Pattern

- WT* is visitor pattern?
  Visitor is a behavioral design pattern that lets you separate 
  algorithms from the objects on which they operate.
  ref: https://refactoring.guru/design-patterns/visitor

- Diel's words and bringing it to the parsing world
  
  We are basically saying: Hey Sr Algorithm, please whenever 
  you find a node in this tree from type X, please apply the following transformation
  for me.
  - Example
    https://astexplorer.net/#/gist/5a5be2e148dc3ef672ad75410e6c7836/7ee7595262575a3b1f61b126b07d9184e3e31c1c
  
  - Another Example is the new blocks framework replace node prop

    ```js
      <Editor 
        replaceNode={
          [
            {
              match: {
                props: ({ blockType }) => blockType === 'Button',
                version: (v) => v === 2
              },
              replaceWith: node => ({
                ...node,
                props: {
                  ...node.props,
                  blockType: 'Button',
                  children: ['my replaced button'],
                },
              }),
            },
          ]
        }
      />
    ```