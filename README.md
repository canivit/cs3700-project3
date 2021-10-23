# Project 3- BGP Router

## My Approach:
- I followed the suggested implementation order given in the assigment description.

## Challenges I Faced:
One big challenge I faced was figuring out what should be the src and dest fields of 'no route' messages. Another big challenge I faced was figuring out how to do path aggregation. I managed to make it work by encoding ip adresses as a string of ones and zeros: '110100...'. The biggest challenge I faced was disaggregation. Then I realized that path aggregation builds a tree where the new route is the parent node and the aggregated routes are the children. This allowed me to develop a recursive algortihm that can succesfully disaggregate routes of any complexity. 

## How I Tested My Code:
I used json.dumps(object, indent = 2) to print out packets I received and sent, as well as the routing table to console in a nice, easy to follow format. This helped me to catch my bugs quickly.
