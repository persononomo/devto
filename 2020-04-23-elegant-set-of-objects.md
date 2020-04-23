# title
Elegant set of objects

# tags
- javascript
- python

# body
Once, at the same time, I needed to do the same thing in two different languages: javascript and python. I needed to do a set of unique objects from an array of non-unique objects.
Of course, I could create the extra array and fill it by looping for input array with some if statement with some extra logic. But JSON helped me :)

javascript
```
let filteredList = [...new Set(myList.map(JSON.stringify))].map(JSON.parse);
```
python
```
filtered_list = list(map(lambda x: json.loads(x), set(map(lambda x: json.dumps(x), my_list))))
```
As for me very elegant - but I think somebody can find some issues in this simple code. If regarding javascript I am overall calm, another thing is python. For me is not so clear. But I leave this part of code because I like it :)
