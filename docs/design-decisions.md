- IPv4 CIDR chosen to be /24
    * Chose /24 as we'll have enough addresses that IP exhaustion won't be a major concern and we aren't wasting a large number of IP's
    * No current plan to expand close to that IP limit as of now
    * This does mean I would be limited if i choose to expand the scope, however I do not see that being a likely case for the context of this project
- Decided against "Encryption Control"
    * This means AWS will not provide built-in visibility or compliance signals for wheteher or not connected resources are configured to use encryption
    * This is not ideal in a security sense as resources should have these capabilities
    * However, for this project adding security policies and monitoring down the line deliberately which should be more in line with the actual scope of this project
- Creating public subnet: 10.0.0.0/25
    * Creating a subnet to start sectioning off the network for security, only certain tools that need access to outside networks or the internet will be placed here
    * Opted for a /25 CIDR, gives us enough room to build and not worry about IP's while also limiting it to a reasonable amount

