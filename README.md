# 42 Get_Next_Line

<div id="desktop-banner">
<pre>
░██████╗░███╗░░██╗██╗░░░░░
██╔════╝░████╗░██║██║░░░░░
██║░░██╗░██╔██╗██║██║░░░░░
██║░░╚██╗██║╚████║██║░░░░░
╚██████╔╝██║░╚███║███████╗
░╚═════╝░╚═╝░░╚══╝╚══════╝
</pre>
</div>

## 📖 What is `get_next_line` 📄?
<details>
<summary><b>A function that reads a line from a file descriptor</b></summary><br>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;get_next_line (GNL) is a project in the curriculum of École 42, a coding school known for its project-based learning approach.
The get_next_line project challenges students to create a function that reads text from a file descriptor line by line, regardless of buffer size or line length.
The goal of this project is to deepen understanding of static variables, memory management, file I/O operations, and buffer manipulation while creating a useful function for future projects.
</p>
</details>

## ✅ Status
<details>
<summary><b>Project completion status</b></summary><br>
<p align="center">
Completed on: 2024-03-28 <br> 125/100</p>
</details>

## 🚀 Usage
To clone:
```shell
git clone https://github.com/Patthh/42_get_next_line.git
cd 42_get_next_line
```

To use in your project:
```c
#include "get_next_line.h"

int main(void)
{
    int     fd;
    char    *line;
    
    fd = open("example.txt", O_RDONLY);
    while ((line = get_next_line(fd)) != NULL)
    {
        printf("%s", line);
        free(line);
    }
    close(fd);
    return (0);
}
```

Compile with:
```shell
cc -Wall -Wextra -Werror your_program.c get_next_line.c get_next_line_utils.c
```
or with this to adjust `BUFFER_SIZE` outside of get_next_line.h
```shell
cc -Wall -Wextra -Werror -D BUFFER_SIZE=42 your_program.c get_next_line.c get_next_line_utils.c
```

## ✨ Features
- 📑 Reads any text file line by line
- 🔄 Works with any buffer size (defined by `BUFFER_SIZE`)
- 📂 Handles multiple file descriptors simultaneously
- 🧹 Clean memory management with no leaks
- 🚀 Efficient string manipulation
- 📋 Proper handling of line endings
- 💼 Works with both text and binary files
- 🔄 Reliable behavior with large files
- ⚠️ Robust error handling

> [!WARNING]
> Function allocates memory for each line that must be freed by the caller

## 🛠️ Implementation Details
<details>
<summary><b>Core Components</b></summary><br>
<p>The Get_Next_Line project consists of these main components:</p>

| Component | Description |
|---------|-------------|
| 📚 get_next_line.c | Main function that reads and returns lines |
| 🧰 get_next_line_utils.c | Helper functions for string manipulation |
| 📋 get_next_line.h | Header file with function prototypes and definitions |
| 🧠 Static Variables | Maintains state between function calls |
| 📦 Buffer Management | Efficient reading and processing of data |
| 📐 Memory Management | Proper allocation and deallocation strategies |
| 🔄 File Descriptor Handling | Support for multiple simultaneous file streams (bonus version) |

</details>

> [!NOTE]
> "Reading between the lines is a skill; reading one line at a time is get_next_line."

<div align="center">
  <a href="https://www.youtube.com/watch?v=unxxm3Q6Ob8"><img src="https://www.musicscore.co.kr/sample/samp7ys7f3ij9wkjid8eujfhsiud843dsijfowejfisojf3490fi0if0sjk09jkr039uf90u/8u4ojsjdjf430foeid409ijef923jerojfgojdofj894jjdsf934f90f40ufj390rfjds/sample_95000/sample_DPsrTl1iJz1h2023061955222.jpg" width="400" alt="Reading Line by Line"></a>
  <br>
  <i>A journey into sequential file reading</i><br><br><br>
</div>

---
<div align="center">
  <p>Made with ❤️ and lots of 📜</p>
</div>
