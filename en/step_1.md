- Writing data to a file with Python is very easy. First you need some data to write. Here it's stored as a variable called `text`.

	```python
	text = 'This is some data to write'
	```

- The next stage is to open a file. You need to pass the name of the file to the `open` function. The function also needs to know with which **mode** to open the file. Here the mode is `w`, which is short for "write".

	```python
	f = open('my_document.txt', 'w', encoding="utf-8")
	```
- Next, the data can be written to the file.

	```python
  f.write(text)
  ```
  
- Lastly, the file needs to be closed.

  ```python
  f.close()
  ```

- Another way of doing this is to automatically **close** the file by using the keyword `with`. This is often preferable, as it is easy to forget to **close** the file.

  ```python
  text = 'This is some data to write'
  with open('my_document.txt', 'w', encoding="utf-8") as f:
	  f.write(text)
  ```
