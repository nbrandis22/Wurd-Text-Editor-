# Wurd-Text-Editor-
Wurd is a text editor with features such as undo (ctrl + z), spell check, and loading and saving files.

The undo function utilizes a stack to store data for what to do when the user wants to undo the last action. My program "batches" together actions of the same kind, so pressing undo will undo all of those actions simultaneously, much like a professional text editor (ex: typing "Wurd is great!" and then pressing ctrl + z will delete that entire line at once, rather than deleting just the last character).

The spell check function finds words that aren't in the dictionary and gives one or more spelling suggestions of what the user could have meant to type. This function uses a trie implementation, which is like a tree except it's space-efficient for words that share a lot of letters. Every "node" of the trie represents a letter at some point in a word, and contains an array of child pointers to subsequent letters in the word. This is particularly useful for finding if a word is in the dictionary, because you can just follow the characters in the trie until the end of the word, at which point the node should be a leaf.

If you want to see the details of how I implemented this program (i.e. the code), you can download the wurdcode.zip file and have a look for yourself.

Download and extract the wurd.zip file and run Wurd.exe to test out the program for yourself. To load a file, press ctrl + L and type out the name of the file you wish to load. If you want, you can load one of the few .txt files already in the zip file (like warandpeace.txt). If you write something you want to save, you can do that by pressing ctrl + s and typing the name of the file to create/overwrite. 
