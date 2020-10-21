# Ant Design Pro table issue

This project is initialized with [Ant Design Pro](https://pro.ant.design). 

The only modification is adding an 'Table' componment into Welcome.tsx.

Follow is the new Table code:

const columns = [
  {
    title: 'Name',
    dataIndex: 'name',
    key: 'name',
    render: text => <div>{text}</div>,
  },
];
const data = [
  {
    key: '1',
    name: 'John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown John Brown ',
  },
  {
    key: '2',
    name: 'Jim Green',
  },
  {
    key: '3',
    name: 'Joe Black',
  },
];

<Table columns={columns} dataSource={data} bordered={true} showHeader={false} pagination={false} style={{ wordWrap: 'break-word', wordBreak: 'break-word' }}/>


This app do right thing when the page width is big, the long name "John Brown John Brown John ..." is displayed multiline auto. But when the page width shinks to very little value, the Table text switch to single line from multiline display.

Why?
