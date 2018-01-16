## Gun-ui elements
Gun-Ui is a set of - Polymer -webcomponents that enables you - the frontend developer - to build complex - Gun - applications without writing any ( well...almost) javascript

Every gun-ui- element has just 2 required attributes "soul" and "prop" that will link the element to a certain data-point.

## Purpose of gun-ui-data-provider
* Delivers your Gun data as an Array
* Keeps this Array in sync with changes in GunUi
* Updates your Dom on changes
* Prevents multiple entries of the same soul


## Dependencies
Like all Gun-Ui elements, `gun-ui-data-provider` requires `gun-ui` to be placed in your main document. Please read the [docs for `gun-ui`](https://github.com/Stefdv/gun-ui)


## But Why?
Ever wanted to create a list of your data ? Like 'contacts' ? And how would you update your DOM if something changes ? Right...

With 'gun-ui-data-provider' ( and Polymer) you don't have to think about that again.

### Installation
( still bower...sorry. When Polymer 3 arrives i will switch to yarn)
```
bower install gun-ui-data-provider --save
```
import it
```
<link rel="import" href="/bower_components/gun-ui-data-provider/gun-ui-data-provider.html">
```
Use it
```
 <gun-ui-data-provider soul="contacts" items="{{myContacts}}"></gun-ui-data-provider>

 <template is="dom-repeat" items="[[contacts]]" as="contact">

      <div>
        <span>Name : [[contact.name]]</span>
        <span>email : [[contact.email]]</span>
      </div>

 </template>
```
#### That's it!  No javascript!
