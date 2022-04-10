# Linux Essential commands
## File System Commands
| Command | Options            | Description                                       | Full Form |
| ------- | ---------------- | ------------------------------------------------- | ------------- |
| **cd**    | `-`              | Navigate to last dir                              | *Change Directory* |
|         | `~`              | Navigate to home                                  | |
|         | `~username`      | Navigate to home of specified user                | |
| **pwd**   |                  | Print working dir                                 | *Print Working Directory* |
| **ls**    |                  | Print dir content                                 | *List* |
|         | `-l`             | Format as list                                    | |
|         | `-a`             | Show hidden items (`-A` without `.` and `..`)     | |
|         | `-r`             | Invert order                                      | |
|         | `-R`             | Recurse                                           | |
|         | `-S`             | Sort by size                                      | |
|         | `-t`             | Sort by date modified                             | |
| **mkdir** | `-p`             | Create dir with parents                           | *Make Directory* |
| **cp**    | `-r`             | Copy dir                                          | *Copy* |
| **rmdir** | `-p`             | Remove dir and empty parents                      | *Reomove Directory* |
| **rm**    | `-rf`            | Remove dir recursively, `-f` without confirmation | *Remove* |
| **mv**    |                  | Move recursively                                  | *Move* |
| **find**  | `-iname pattern` | Search dir/file case-insensitive                  | |
|         | `-mmin n`        | Last modified n minutes ago                       | |
|         | `-mtime n`       | Last modified n days ago                          | |
|         | `-regex pattern` | Path matches pattern                              | |

Note: If you want any command to print in only one line at a time, you can use **-1** flag with any command. An example for it is shown below.

![ls -1](https://user-images.githubusercontent.com/85234103/162622969-a3e27e03-a93e-4886-9eb4-edbfbf5d33ad.png)
---
## File Manipulation

| Command | Options                                      | Description                                | Full Form |
| ------- | ------------------------------------------ | ------------------------------------------ | -------- |
| **cat**   | `file`                                     | Print content                              | *Concatenate* |
| **tac**   | `file`                                     | Print content inverted                     | *Reverse of CAT* |
| **sort**  | `file`                                     | Print sorted                               | |
|         | `file -r -u`                               | Print sorted descending without dublicates | |
| **head**  | `-n10 file`                            | Print  first lines 5-10                           | |
| **tail**  | `-n10 file`                                  | Print last lines 5-10              | |
| **file**  | `file`                                     | Get file type                              | |
| **wc**    | `file`                                     | Count Lines, Words, Chars (Bytes)          | *Word Count* | 

## Stream redirection
`>` overwrite

`>>` append

For better understanding, I have created a text file and used the above commands on it and provided the images below.
- I have also used "**Echo**" Command in the below images, If you want to know more about [Echo](https://github.com/bobbyiliev/101-linux-commands-ebook/blob/main/ebook/en/content/021-the-echo-command.md), Go to the link provided.
- As we have only 4 lines in our text file, I used 2 in the head and tail commands and added one more duplicate line through Echo command.
![lec1](https://user-images.githubusercontent.com/85234103/162624376-d3668926-2690-4f09-9d6b-22df7adf3e67.png)
![lec2](https://user-images.githubusercontent.com/85234103/162624386-d15d1176-40f1-47c3-a27e-fef0ff426367.png)
![lec3](https://user-images.githubusercontent.com/85234103/162624389-914832ce-e9cb-4f29-b736-51910cd7625b.png)


