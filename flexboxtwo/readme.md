```

Flex Box bu Default is aligned to the Column.


Flex properties


(a)flex-direction

It is by default row.

it can be overridden to the following

flex-direction:row,
flex-direction:row-reverse
flex-direction:column,
flex-direction:column-reverse

By default if i do not apply flexbox, elements occupy the full width.


```

**Child Flex Properties**

```

By doing flex on the Parent, the child has some properties that they inherit and utilize.

.child1 {
  order: 3;
  flex-grow: 1;
}

.child2 {
  order: 2;
  flex-grow: 5;
}

.child3 {
  order: 1;
  flex-grow: 1;
}


if i want to change the alignment of the Child i can use the align self property.

```

**Commonly Used Properties**

```
Justify content-->How do i want to justify the content of our children elements inside of the Parent

By  default is is at flex start.

It can also be set to : flex-end, center, 

space-around (add space verywhere there is an edge), 
space-between(adds even space but only between your elements and not the edges)
space-evenly (does not discriminate)


Align Items

Exactly the same as justify content but for the Opposite axis.



```