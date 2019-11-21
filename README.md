## Symlink creator and manager

Example usage to create an item:
```
sym movies ~/media/movies entertainment videos
This creates an item called movies.
Associated with the provided path.
And 2 tags were added to it.
This will create a symlink: ~/sym/movies
It will also create tag symlinks:
~/sym/tags/entertainment/movies
and ~/sym/tags/videos/movies
These 3 symlinks point to the same path.
You can do for instance 'ls ~/sym/movies'
And it will show the contents of
~/media/movies
```    
Remove an item:
```
sym remove movies
or regex...
sym remove re:\\w+
```    
Remove an item by path:
```
sym removepath /media/movies
or regex...
sym removepath re:\\w+
```    
Rename an item:
```
sym rename movies moviez
```    
Add a tag:
```
sym tag movies art
```    
Remove a tag:
```
sym removetag movies art
```
List items:
```
sym list
```
List tags:
```
sym tags
``` 
List paths associated with a tag:
```
sym tag funny
``` 
Change the path of an item:
```
sym changepath movies /media/movies
```
Open a path in the file manager:
```
sym open movies
```

A script can be used with --script

i.e: sym --script=~/myscript.txt

Scripts are 1 command per line.

For example:
```
movies ~/media/movies plot
tag movies woomy
backup
```