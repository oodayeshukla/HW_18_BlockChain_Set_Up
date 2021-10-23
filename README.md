# Homework 18: Blockchain Set Up

In this Homework, we use the tools to set up a simulated blockchain and execute transactions. 

1: Download the file geth-alltools-linux-amd64-1.9.7 from https://geth.ethereum.org/downloads/.

2: Unzip the file (depending on your OS)

3: Ensure that the applications geth, and puppeth are in the uncompressed folder 

4: Execute the following commands: 
  ./geth --datadir node1 account new
  ./geth --datadir node2 account new
  Where node1 and node2 will be the new directories that will be created to hold the newly created blockchain node information. 



5: Follow the instructions for setting up the nodes using the prompts as shown in the following ![screenshot]( https://github.com/oodayeshukla/HW_18_BlockChain_Set_Up/blob/main/1_Screenshot%20from%202021-10-10%2019-12-28.png).

The node addresses are:  

NODE 1
Public address of the key:   0x066f81B90B11FdCE0323eBAF79dA4BEb8C01a0D5
Path of the secret key file: node1/keystore/UTC--2021-10-10T23-07-48.876839289Z--066f81b90b11fdce0323ebaf79da4beb8c01a0d5

NODE 2
Public address of the key:   0xCB211eaC05270fc3Be62fF671654f14be76AD734
Path of the secret key file: node2/keystore/UTC--2021-10-10T23-08-24.809312896Z--cb211eac05270fc3be62ff671654f14be76ad734

# Make sure that the port numbers on Node 1 and Node 2 do not clash!

6: Once both nodes have been configured, execute the following command, in separate command windows, one for each node: 

./geth --datadir node1 --unlock "0x066f81B90B11FdCE0323eBAF79dA4BEb8C01a0D5" --mine --rpc --allow-insecure-unlock

7: To launch the second node, copy the enode address that is generated when node1 is launched as shown below. 

./geth --datadir node2 --unlock "0xCB211eaC05270fc3Be62fF671654f14be76AD734" --mine --port 30304 --bootnodes "enode://59d5e1f25013842bd1bcdf969d80a3adb7afe1ae9c0a99cb39a234acc25616971301a778147be9b92161f3db9f79433d4722c205cc38b991f549bf4af245e823@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock

8: Once both nodes are executing (and set up for mining) the following will be executing in two separate command windows, one for each node.  The command window on the left is Node 1, the Genesis node, and the command window on the left is node2 connected to node1.  The screen shot showing both nodes executing are is shown here on this ![screenshot](https://github.com/oodayeshukla/HW_18_BlockChain_Set_Up/blob/main/2_Screenshot%20from%202021-10-10%2019-20-10.png) 

9: Use the MyCrypto app to send transactions from one node (address) to another as shown ![below](https://github.com/oodayeshukla/HW_18_BlockChain_Set_Up/blob/main/3_Screenshot%20from%202021-10-10%2019-48-41.png)  
  
10: On the MyCrypto application you can check the status of your transaction as shown ![below](https://github.com/oodayeshukla/HW_18_BlockChain_Set_Up/blob/main/5_Screenshot%20from%202021-10-10%2019-50-48.png)

11: You call also check recent transactions as shown ![below](https://github.com/oodayeshukla/HW_18_BlockChain_Set_Up/blob/main/7_Screenshot%20from%202021-10-10%2021-19-36.png)

12: Once a transaction is complete you will get the following succesful transaction notice as shown ![below](https://github.com/oodayeshukla/HW_18_BlockChain_Set_Up/blob/main/8_Screenshot%20from%202021-10-10%2021-19-58.png) 
