| rank | ▲ | ✰ | vote | url |
|:-:|:-:|:-:|:-:|:-:|
|  49  | 432 | 198 | 616 | [url](http://stackoverflow.com/questions/72899/how-do-i-sort-a-list-of-dictionaries-by-values-of-the-dictionary-in-python) |

***

## 通过列表中字典的值对列表进行排序

我的到了一个字典的列表,我想对字典的值进行排序.

```python
[{'name':'Homer', 'age':39}, {'name':'Bart', 'age':10}]
```

对name进行排序,应当是:

```python
[{'name':'Bart', 'age':10}, {'name':'Homer', 'age':39}]
```

***

用key比用cmp更清晰明了:

```python
newlist = sorted(list_to_be_sorted, key=lambda k: k['name'])
```

或者其他人的建议:

```python
from operator import itemgetter
newlist = sorted(list_to_be_sorted, key=itemgetter('name'))
```

