# netpractice

internet protocol or: how i learned to stop worrying and love the router


[references](https://github.com/lpaube/NetPractice)
korean translation comming soon (ish)


## Things to remember

### IPv4

- 0 ~ 255 * 4 = 4 bytes = 32 bits

### Private IPv4 addresses

- can be only used within the same network
- 10.0.0.0/8
- 172.16.0.0/12
- 192.168.0.0./16

### Subnet Masks

- apply AND ops to get the network address
- CIDR notation = `/{number of 1s in binary}`
- first and last of an address range is reserved
  - first: network ID address
  - last: broadcast address

### Interface

- network is like shouting numbers at each other
- so individual's address must not overlap with others
- interfaces will decide to only listen to numbers within their range
- that range is the subnet mask

### Switch
- distributes packets to local network
- can be ignored in the subject, since it doesn't do much

### Router
- connects multiple **different** network addresses
- so its addresses (and their ranges) must not overlap

### Routing table
- if a packet's destination address is not within local network, the router won't know where to send
- but it could 'toss' the packet to another router, so that router may know where to send it
- if one of the destination in routing table match with packet's, the router will send it to the 'next hop'
- if 'next hop' knows the destination, it will send it to the destination, if not, hop again and again...
- `default` == 0.0.0.0/0, since every ip address would match

## Levels

### [Basics: subnet mask, network address, and ip range](doc/basic.md)

### [Intermidiate: routing, routing table](doc/intermediate.md)
