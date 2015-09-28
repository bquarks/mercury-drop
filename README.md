# &lt;mercury-drop&gt;

> Easy draggable list for web components.

## Demo

[Check it live!](https://github.com/bquarks/mercury-drop)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install mercury-drop --save
```

Or [download as ZIP](https://github.com/bquarks/mercury-drop/archive/master.zip).

## Usage

1. Import polyfill:

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents-lite.min.js"></script>
    ```

2. Import custom element:

    ```html
    <link rel="import" href="bower_components/mercury-drop/mercury-drop.html">
    ```

3. Start using it!

    ```html
    <mercury-drop items="{{data}}" as="item">
      <style>
        .box {
          border: 2px solid #621;
          margin: 5px;
          box-shadow: 1px 1px 1px #444;
          width: 200px;
        }
      </style>
      <template>
        <dom-repeat items={{data}}>
            <li draggable class="box">Hello <span>{{item.name}}</span></li>
        </dom-repeat>
      </template>
    </mercury-drop>
    ```

## Usage

Pass an array of elements to the component, when you drag one element in the list
the data binding go up until your component.

You must use "as" attribute to set the internal variable name.

To make the list elements draggable you must put in the top parent an empty attribute called **draggable**.

To set styles to the temporal box where to place the item, you must use the class
**.phantom-box**

## Development

In order to run it locally you'll need to fetch some dependencies and a basic server setup.

1. Install [bower](http://bower.io/) & [polyserve](https://npmjs.com/polyserve):

    ```sh
    $ npm install -g bower polyserve
    ```

2. Install local dependencies:

    ```sh
    $ bower install
    ```

3. Start development server and open `http://localhost:8080/components/my-repo/`.

    ```sh
    $ polyserve
    ```

## History

For detailed changelog, check [Releases](https://github.com/donflopez/mercury-drop/releases).

## License

[MIT License](http://opensource.org/licenses/MIT)
