## Alert

### Get started

```sh
  npm i "@axa-fr/react-toolkit-alert"
```

### Components

#### Alert

To use this component, you need to provide a classModifier to define the alert type, which will also pick a default icon.
A default icon will be displayed if none is provided in props and the **first** class modifier is :

- error -> glyphicon-exclamation-sign <span class="glyphicon glyphicon-exclamation-sign"/>
- danger -> glyphicon-alert <span class="glyphicon glyphicon-alert"/>
- info -> glyphicon-info-sign <span class="glyphicon glyphicon-info-sign"/>
- success -> glyphicon-ok <span class="glyphicon glyphicon-ok"/>

This example will display an orange alert with the "alert" glyphicon.

```javascript
import Alert from'@axa-fr/react-toolkit-alert';
import '@axa-fr/react-toolkit-alert/dist/af-alert.css';

const AlertComponent = () => (
    <Alert classModifier="danger" icon="minus-sign" title="Warning: information is missing">
    </Alert>
  );

export default AlertComponent;
```

#### AlertCore

This core component does not assign an icon depending on the classModifier.

You have to explicitly define it in the "icon" prop :

```javascript
import {AlertCore} from'@axa-fr/react-toolkit-alert';
import '@axa-fr/react-toolkit-alert/dist/af-alert.css';

const MyErrorAlert = () => (
<AlertCore classModifier="error" iconClassName="glyphicon glyphicon-minus-sign" title="Error !">

  <ul>
    <li>Name is required</li>
    <li>Username is required</li>
    <li>Email is required</li>
    <li>The date format is invalid</li>
  </ul>
  
  </AlertCore>
  );

export default MyErrorAlert;

```

#### AlertWithType

This component has its own prop to declare the Alert type, rather than relying on classModifier.

The prop type has **only** 4 possible values : _error_, _danger_, _info_ and _success_

This example will display a blue alert with an info-sign glyphicon :

```javascript
import {AlertWithType} from'@axa-fr/react-toolkit-alert';
import '@axa-fr/react-toolkit-alert/dist/af-alert.css';

const MyInfoAlert = () => (
<AlertWithType type="info" title="Info: you can also contact an advisor by phone"/>
  );

export default MyInfoAlert;


```
