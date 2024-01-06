[Isolated RS-232 Framework Expansion Card](https://medo64.com/rs232isofec/)
===========================================================================

This Framework laptop expansion card will show up on your system as a serial
device and allow for isolated RS-232 communication up to 460,800 baud rate.


## UART Pinout

To connect to this board, one has to use a 5-pin JST XH connector. The following
table represents the pinout, pin 1 being on the left as looking into the
expansion card. Note that pins 1 and 5 are not internally connected.

| # | Ref | Description                     | DB9 |
|--:|:---:|---------------------------------|----:|
| 1 |  -  | Not connected                   |  8  |
| 2 | RXD | Receive data                    |  2  |
| 3 | GND | Ground connection               |  5  |
| 4 | TXD | Transmit data                   |  3  |
| 5 |  -  | Not connected                   |  7  |

As power consumption is low, wires can be almost any AWG. I would recommend
using 24 AWG wire 0.25 mm² as they allow for greater compatibility with other
connectors.


## Supported Speeds

This board employs the FT232R as its UART chip, and consequently, it supports
all the baud rates this chip [can handle](https://ftdichip.com/Documents/AppNotes/AN232B-05_BaudRates.pdf)
up to 460,800 baud which is the limit of isolator chip used. The table below
lists the standard baud rates.

| Baud rate |    Actual | Error |    Divisor |
|----------:|----------:|------:|-----------:|
|       300 |       300 | 0.00% |  10000.000 |
|       600 |       600 | 0.00% |   5000.000 |
|     1,200 |     1,200 | 0.00% |   2500.000 |
|     1,800 |     1,800 | 0.00% |   1666.625 |
|     2,400 |     2,400 | 0.00% |   1250.000 |
|     4,800 |     4,800 | 0.00% |    625.000 |
|     7,200 |     7,201 | 0.01% |    416.625 |
|     9,600 |     9,600 | 0.00% |    312.500 |
|    14,400 |    14,406 | 0.04% |    208.250 |
|    19,200 |    19,200 | 0.00% |    156.250 |
|    28,800 |    28,812 | 0.04% |    104.125 |
|    38,400 |    38,400 | 0.00% |     78.125 |
|    57,600 |    57,692 | 0.16% |     52.000 |
|   115,200 |   115,385 | 0.16% |     26.000 |
|   230,400 |   230,769 | 0.16% |     13.000 |
|   460,800 |   461,538 | 0.16% |      6.500 |

While rates above this can be set, they are not guaranteed to work.


---
*You can check my blog and other projects at [www.medo64.com](https://www.medo64.com/electronics/).*
