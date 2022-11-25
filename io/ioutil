package main

import (
	"bufio"
	"bytes"
	"fmt"
	"io/ioutil"
	"os"
	"time"
)

func main() {
	fmt.Println("Введите любую фразу. Для выхода напишите 'exit'")
	var text string
	var b bytes.Buffer
	in := bufio.NewScanner(os.Stdin)

	for {
		in.Scan()
		text = in.Text()

		if text == "exit" {
			break
		} else {
			t := (time.Now().Format("2006-01-02 15:04:05"))
			b.WriteString(fmt.Sprintf("%v %v\n", t, text))
		}
	}
	if err := ioutil.WriteFile("homework_iountil.txt", b.Bytes(), 0666); err != nil {
		fmt.Println("Ощибка при создании файла и записи из буфера", err)
	}
}
