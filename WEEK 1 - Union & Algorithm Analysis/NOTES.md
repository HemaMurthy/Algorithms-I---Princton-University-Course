# Dynamic Connectivity Problem

## Problem Statement:
    
Given a set of N objects, 'union' command can connect two objects,

 find query: is there a path connecting two objects?

Assumptions:
    
* Reflexive: p is connected to p
* Symmetric: if p is connected to q, then q is connected to p
* transitive: if p is connected to q, and q is connected to r, then p is connected to r

Border Cases:

max number of unions given n elements

## Solution 1: Quick find

Approach: two elements are connected if they have the same id (in an array) 

Find() : checks if two elements have the same id
Union(): Merges two element's id as the same as well as all the other connected elements

Cost: 
Union: O(n)
Find: 1

(-) Union is too expensive in case of larger arrays

## Solution 2: Quick Union

Approach: using trees/ forests data structures

Find(): Check if two elements have the same root
Union(): merge components containing p and q, set id of p's root to id of q's root

