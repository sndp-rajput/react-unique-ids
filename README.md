# React Unique IDS

`React Unique IDS` is a handy tool for React developers. It helps create special IDs for elements in your React apps. You can customize these IDs to suit your needs easily. It's great for managing IDs within React components, making your development process smoother
<br /><br>

### Installation & Usage

- To install and set up the library, run:

  ```bash
  npm install react-unique-ids
  ```

- import the library
  ```jsx
  import reactUniqueIds from "react-unique-ids";
  ```
- Use it
  ```jsx
  reactUniqueIds();
  ```

---

## Customization

- To generate a unique ID, simply call the function:

  ```jsx
  reactUniqueIds();
  ```

  Output: A unique ID is generated with a length of 20 characters, containing uppercase letters, lowercase letters, numbers, and symbols.

  ```jsx
  "bmYZWC*9DuLNxB@zcd5m";
  ```

  <br>

- To specify the length of the ID, pass the desired length as an argument:

  ```jsx
  reactUniqueIds(15);
  ```

  Output: A unique ID is generated with a length of `15` characters, containing uppercase letters, lowercase letters, numbers, and symbols.

  ```jsx
  "NF7&4q#9F@pJH4o";
  ```

  <br>

- You can customize the character requirements by passing an object:

  ```jsx
  const data = {
    length: 10,
    uppercase: true, // true if you need uppercase letters in the unique ID
    lowercase: false, // true if you need lowercase letters in the unique ID
    symbol: false, // true if you need symbol letters in the unique ID
    number: true, // true if you need number letters in the unique ID
  };

  reactUniqueIds(data);
  ```

  OR

  ```jsx
  const data = {
    length: 10,
    lowercase: false, // true if you need lowercase letters in the unique ID
    symbol: false, // true if you need symbol letters in the unique ID
  };

  reactUniqueIds(data);
  ```

  Output: A unique ID is generated based on your customization/requirement.

  ```jsx
  "BFU03WETS56B59U";
  ```

  > [!NOTE]  
  > By default, all types are true.

  - To generate an ID of the format `23573527-aT2s%JR6@-YWDBSCYE`, you can use the following configuration:

    ```jsx
    const data = {
      length: [8, "number", 9, 8, "uppercase"],
      separater: "-",
    };

    reactUniqueIds(data);
    ```

    Output: A unique ID is generated where the first 8 characters are numbers, the next 9 characters can be any type, and the last 8 characters are in uppercase. They are separated using a separator.

    ```jsx
    "72324118-71*xW4fHC-ANTITOWI";
    ```
