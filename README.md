# Saludos en Go

este paquete proporciona una forma simple de obtener saludos personalizados

## instalacion
Ejecutar el siguiente comando para instalar el paquete:
```bash
go get -u github.com/ingidelcas/greetings
```

## Uso
Aqui tienes un ejemplo de como utilizar el paquete en tu codigo :

```go
package main

import (
	"fmt"
	"log"

	"github.com/ingidelcas/greetings"
)

func main() {
	log.SetPrefix("greetings: ")
	log.SetFlags(0)

	names := []string{"idelcas", "Liam", "Lyanna"}

	messages, err := greetings.Hellos(names)
	if err != nil {
		log.Fatal(err)
	}
	fmt.Println(messages)
}
```