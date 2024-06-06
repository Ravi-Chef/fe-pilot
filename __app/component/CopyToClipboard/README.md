# CopyToClipboard

  The Component has the capability to ```copy``` any value like (Element, String, Number)

## Demo

A minimal [Demo Link](https://6jpxdq.csb.app/?component=CopyToClipboard)

## Usage/Examples

| Value |  Used as a  | Description|
|--------- | -------- |-----------------|
| <b>CopyToClipboard</b> | :white_check_mark: Component | Can be used as Component |
| <b>copyToClipboard<b> | :white_check_mark: Service | Can be used as Service |


  ##### 1. Here's an example of basic usage with Default Import:
  ```javascript
 // Default import will return a Component
  import CopyToClipboard from 'fe-pilot/CopyToClipboard';

  <CopyToClipboard elementToBeCopy={`<div>Element to be Copy<div>`} />
  ```

  ##### 2. Here's an example of basic usage with Multiple Import:
  ```javascript
  import { CopyToClipboard, copyToClipboard } from 'fe-pilot/CopyToClipboard';

  // Used as a Component
  <CopyToClipboard elementToBeCopy={`<div>Element to be Copy<div>`} />

  // Used as a Service
  copyToClipboard({ elementToBeCopy={`Element to be Copy`} });
  ```

  ##### 3. Here's an example of a advance usage:

  ```javascript
  import { CopyToClipboard } from 'fe-pilot/CopyToClipboard';

  const successCb = (response) => {
    console.log("success response:", response);
  }

  const failureCb = (response) => {
    console.log("failure response:", response);
  }

  return (
    <CopyToClipboard
      successCb={successCb}
      failureCb={failureCb}
      elementToBeCopy={`A string text To Copy`}
    >
      Pass clickable element (button, anchor, string, icon etc)
    </CopyToClipboard>
  );

  ```

  ### Props

  <table>
    <tr>
      <th>
        Props
      </th>
      <th>
        Type
      </th>
      <th>
        Description
      </th>
      <th>
        Response
      </th>
    </tr>
    <tr>
      <td>
          successCb
      </td>
      <td>Function</td>
      <td> It will be called on success</td>
      <td>
        <pre>
  {
      data: "Can be array/object/string/number",
      msgType: "SUCCESSFUL",
      msg: "A success msg",
      status: "SUCCESS"
  }
        </pre>
      </td>
    </tr>
    <tr>
      <td>
          loadingCb
      </td>
      <td>Function</td>
      <td>
        It will be called before success/failure.
      </td>
      <td>
        <pre>
  {
    msgType: "LOADING",
    msg: "LOADING...",
    status: "LOADING"
  }
  </pre>
      </td>
    </tr>
    <tr>
      <td>
          failureCb
      </td>
      <td>Function</td>
      <td>
        It will be called on failure
      </td>
      <td>
         <pre>
  {
    msgType: "ERROR",
    msg: "A failed msg",
    status: "FAILURE"
  }
         </pre>
      </td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <th>
      Props
    </th>
    <th>
        Type
    </th>
    <th>
        Description
    </th>
    <th>
        Default Values
    </th>
    <tr>
      <td>
          showForever
      </td>
       <td>Boolean</td>
      <td>To hide/remove unsupported feature, make it <b>false</b>.</td>
      <td>Default value is <b>true</b></td>
    </tr>
    <tr>
      <td>elementToBeCopy*</td>
      <td>Element</td>
      <td>Pass the text/element/number to be copy</td>
      <td> <pre>---</pre> </td>
    </tr>
  </table>

