# HTTP observations (Lab 4, Task 1)

| Question | My answer |
|----------|-----------|
| Request method for index.html | GET |
| Status code with Disable cache ticked | 200 OK |
| Status code on a normal reload | 304 Not Modified |
| Status code for /nothing-here.html | 404 Not Found |
| Value of the Content-Type response header | text/html |
| Remote Address (IP and port) | 127.0.0.1:5500 |
| Protocol in the address bar (http or https) | http |

## Why is this address http and not https?
This address uses HTTP because 127.0.0.1 is localhost, meaning traffic stays within the local machine and does not travel over an external network where encryption is required.
## Form validation tests (Task 3)
- Name empty: ...please fill out this field
- Name "Al": ...please lengthen the text to 3 or more characters (you arecurrently using 2 characters)
- Phone 12345: ...please match the requested format, 11 digits starting with 03,for example 03001234567
- Quantity 0 or 11: ...
- Pickup 07:30 or 19:00: ...
- Item not chosen: ...please select an item in list
## localStorage and XSS (Task 3)
If the code used row.innerHTML = "<td>" + order.name + "</td>", what could an attacker type as a name?
An attacker could type a malicious HTML string containing JavaScript event handlers or script tags
Example:<svg onload="alert('Hacked')">
