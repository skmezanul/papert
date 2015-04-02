# Koch Snowflake #
```
to line :count :length
ifelse :count = 1 [fw :length] [
make "count :count -1 
line :count :length
lt 60 line :count :length
rt 120 line :count :length
lt 60 line :count :length]
end

to koch :count :length
rt 30 line :count :length
rt 120 line :count :length
rt 120 line :count :length
end

reset
setxy  45 370
koch 5 5
```


# Hilbert Curve #
```
to r :l :w end

to l :l :w
if :l = 0 [stop]
rt 90
r :l -1 :w
fw :w
lt 90
l :l -1 :w
fw :w
l :l-1 :w
lt 90
fw :w
r :l -1 :w
rt 90
end

to r :l :w
if :l = 0 [stop]
lt 90
l :l -1 :w
fw :w
rt 90
r :l -1 :w
fw :w
r :l -1 :w
right 90
fw :w
l :l -1 :w
lt 90
end

reset
setxy 10 490
penwidth 4
l 6 6
```

# tree fractal #
```
to tree :arms :length :count
if :count < 1 [stop]
repeat :arms [lt 360/:arms
pd fw :length
tree :arms 2 * :length / :arms :count - 1
pu bw :length]
end
reset
tree 7 128 4
```


## spiral ##
```


to spiral :w :a :x :c :ww
if :c = 0 [stop]
penwidth :ww
color [0 0 :w]
lt :x
fw :w
pu
bw :w
rt :x
fw :w
pd 
rt :a
spiral :w +1 :a :x+0.7 :c -1 :ww + 0.1
end
reset
spiral 1 30 10 90 1
```