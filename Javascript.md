# ***Javascript***

Trong javascript không có class, chỉ có function. Function là object trong JS. \
Function trong JS có các method tồn tại sẵn có nằm trong function prototype ( bind, call, apply, v.v.. )

## ***1. Falsy values:***

- Là các giá trị undefined, 0, false, null, v.v....
- Lọc các giá trị falsy trong array:

```js
array.filter(Boolean)
```

## ***2. Closure:***

## ***3. This / Bind / Call / Apply:***

- ### **This**
  
  - Là đối tượng object của ngữ cảnh mà function chứa từ khoá this được gọi.
  - Trong trường hợp **strict mode**, với ngữ cảnh global thì this có giá trị **undefined**
  - Khi sử dụng this, chỉ có 2 loại ngữ cảnh
    - Object chứa method
    - Object global ( window object )

  - 4 trường hợp dễ nhầm lẫn khi sử dụng ***this***
    - Hàm được truyền vào như một callback
    ```text
    Khi object có sử dụng this được truyền vào như 1 callback, để tránh việc this hiểu sai ngữ cảnh, phải sử dụng anonymous function hoặc bind method khi truyền vào callback
    ```

    - Sử dụng this trong anonymous function
    ```text
    Không sử dụng this trong các array property method ( forEach, map, ...) hoặc phải gán 1 biến = this và dùng biến đó để lấy item bên trong this
    ```

    - Hàm được gán vào 1 biến
    ```text
    Phải sử dịng bind, nếu không this sẽ trỏ đến object global (window) không phải object trong ngữ cảnh của hàm
    ```

    - Sử dụng this trong borrowing function
    ```text
    Phải sử dụng Apply trong trường hợp mượn method
    ```

- ### Bind

- ### Call

- ### Apply

## ***4. Reduce / Map / Filter /  ..v..v....v..***

## ***5. Even loop:***

## ***6. Callback function:***

- Là truyền tham số là 1 function ( 1 sự kiện ) vào một function khác, tại một thời điểm nào nó khi chạy function thì sự kiện được truyền vào sẽ được thực thi

- Callback function có vai trò quan trọng trong xử lí bất đồng bộ đối với ngôn ngữ sự kiện JS

- Vấn đề **Callback Hell** là hàng loạt các callback function nằm trong callback function dẫn đến một vòng lặp vô tận, không thẩm mĩ, không thể maintain => ***Sử dụng promises / async await***

```text
- Một số lưu ý:
    - Callback function chỉ được thực hiện sau khi gán với '()'

    - Kiểm tra tham số đầu vào phải là function hay không mới có thể chạy sự kiện truyền vào đó được, nếu không sẽ lỗi

    - Cẩn thận khi sử dụng this trong callback function, phải sử dụng Apply thể trỏ đúng object trong ngữ cảnh của function
```
