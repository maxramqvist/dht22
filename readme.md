Greetings do it yourselfers!

It's AM2302/DHT22 library. No external c libraries. 
Forked from: github.com/morus12/dht22

## installation 
`go get github.com/maxramqvist/dht22`

## usage
```
package main

import "github.com/maxramqvist/dht22"

func main () {

    sensor := dht22.New("GPIO_4")
    
    data, err := sensor.Read()
    if err != nil {
        return err
    }
    
    fmt.Printf("Temperature is %f C and humidity %f %." data.Temperature, data.Humidity)
}
```

## testing environmnet 
- Raspberry Pi Zero WH
- One DHT22 sensor
- go1.19.5 linux/arm
- Raspberry Pi OS (32-bit), 2022-09-30