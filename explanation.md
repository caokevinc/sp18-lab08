### What's going on in `Mystery.sol`?

##### Answer:
Mystery.sol is a function that sets address add to a. There is a fallback function, which first takes the gas and uint's it so that its value can be used later in the assembly code. o_code marks the first free memory block, such that everything else will be relevant to it.

Next, the class variables are loaded into addr through sload. The contract at addr is then called, sending the gas. Finally, it checks whether the return destination is valid, and returns the first 32 bytes of o_code.
