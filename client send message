package main

import "net"
import "fmt"
import "bufio"
import "os"

func main() {


conn, _ := net.Dial("tcp", "192.168.18.1:8081")
for {
reader := bufio.NewReader(os.Stdin)
fmt.Print("Text to send: ")
text, _ := reader.ReadString('\n')

fmt.Fprintf(conn, text + "\n")

message, _ := bufio.NewReader(conn).ReadString('\n')
fmt.Println("Message reverse from server: ", Reverse(message))
}
}


func Reverse(message string) string {
    var reverse string
    for i := len(message)-1; i >= 0; i-- {
        reverse += string(message[i])
    }
    return reverse 
}
