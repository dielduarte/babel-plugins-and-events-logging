- WT* is visitor pattern?
  Visitor is a behavioral design pattern that lets you separate 
  algorithms from the objects on which they operate.
  ref: https://refactoring.guru/design-patterns/visitor

- Diel's words and bringing it to the parsing world
  We are basically saying, Hey Sr Algorithm Please whenever 
  you find a node in this tree from type X, please apply the following transformation
  for me.
  - Example
    https://astexplorer.net/#/gist/5a5be2e148dc3ef672ad75410e6c7836/ea9d22472a3ae110fe23a3ccd298b67ac9584e96
  
  - Another Example is the new blocks framework replace node prop

    ```js
      <Editor 
        replaceNode={
          [
            {
              match: {
                props: ({ blockType }) => blockType === 'Button',
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