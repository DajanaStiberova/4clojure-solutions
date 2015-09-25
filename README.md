#4clojure solutions

#####Problem 1
Nothing but the Truth
```clojure
(= 1 1)
```

#####Problem 2
Simple Math
```clojure
4
```

#####Problem 3
Intro to Strings
```clojure
"HELLO WORLD"
```
#####Problem 4
Intro to Lists
```clojure
 :a :b :c
```

#####Problem 5
Lists: conj
```clojure
'(1 2 3 4)
```

#####Problem 6
Intro to Vectors
```clojure
 :a :b :c
```

#####Problem 7
Vectors: conj
```clojure
 [1 2 3 4]
```

#####Problem 8
Intro to Sets
```clojure
 #{:a :b :c :d}
```

#####Problem 9
Sets: conj
```clojure
 2
```

#####Problem 10
Intro to Maps
```clojure
 20
```

#####Problem 11
Maps: conj
```clojure
 [:b 2]
```

#####Problem 12
Intro to Sequences
```clojure
 3
```

#####Problem 13
Sequences: rest
```clojure
 '(20 30 40)
```

#####Problem 14
Intro to Functions
```clojure
 8
```

#####Problem 15
Double Down
```clojure
 #(* 2 %)
```

#####Problem 16
Hello World
```clojure
 #(str "Hello, " % "!")
```

#####Problem 17
Sequences: map
```clojure
'(6 7 8)
```

#####Problem 18
Sequences: filter
```clojure
'(6 7)
```

#####Problem 19
Last Element
```clojure
#(first (reverse %))
```

#####Problem 20
Penultimate Element
```clojure
#(second (reverse %))
```

#####Problem 21
Nth Element
```clojure
#(get (vec %1) %2)
```

#####Problem 22
Count a Sequence
```clojure
#(reduce (fn [acc x]
                  (inc acc))
              0 %)
```

#####Problem 23
Reverse a Sequence
```clojure
#(reduce (fn [acc x]
            (cons x acc)) 
            (empty %) %)
```

#####Problem 24
Sum It All Up
```clojure
#(apply + %)
```

#####Problem 25
Find the odd numbers
```clojure
#(reverse (reduce (fn [acc x]
                         (if (odd? x)
                           (conj acc x)
                           acc))
                       '() %))
```

#####Problem 26
Fibonacci Sequence
```clojure
#(loop [x [1 1]]                                                                    
        (if (= (count x) %)                                             
          x                                                                               
          (recur (conj x (apply + (take 2 (reverse x)))))))
```


#####Problem 27
Palindrome Detector
```clojure
(if (string? %)
   (= (clojure.string/reverse %) %) 
   (= (reverse %) %))
```

#####Problem 28
Flatten a Sequence
```clojure
#(reverse (reduce
                (fn rec-flatten [acc item]
                  (if (coll? item) (reduce rec-flatten acc item)
                      (conj acc item)))
                '()
                %))
```

#####Problem 29
Get the Caps
```clojure
#(apply str(filter (set (map char (range 65 91))) %)) 
```

#####Problem 30
Compress a Sequence
```clojure
#(map first (partition-by identity %))  
```

#####Problem 32 
Duplicate a Sequence
```clojure
#(seq (reduce (fn [acc item]                                                         
                     (-> acc                                                              
                         (conj item)                                                      
                         (conj item)))                                                    
                  [] %)) 
```

#####Problem 33 
Replicate a Sequence
```clojure
#(mapcat (fn [item]                                                      
             (take %2 (repeat item)))                                              
          %1) 
```

#####Problem 34
Implement range
```clojure
#(take (- %2 %1) (iterate inc %1))
```

#####Problem 35
Local bindings
```clojure
7
```

#####Problem 36
Let it Be
```clojure
[x 7 y 3 z 1]
```

#####Problem 37
Regular Expressions
```clojure
"ABC"
```

#####Problem 38
Maximum value
```clojure
(fn [& args]
  (last (sort args)))
```

#####Problem 39
Interleave Two Seqs
```clojure
#(flatten (map (fn [f s]
                      (conj '() s f))
                    %1 %2))
```

#####Problem 42
Factorial Fun
```clojure
#(apply * (range 1 (+ 1 %)))
```

#####Problem 48
Intro to some
```clojure
6
```

#####Problem 57
Simple Recursion
```clojure
'(5 4 3 2 1)
```

#####Problem 64
Intro to reduce
```clojure
+
```

#####Problem 68
Recurring Theme
```clojure
[7 6 5 4 3]
```

#####Problem 71
Rearranging Code: ->
```clojure
last
```

#####Problem 72
Rearranging Code: ->>
```clojure
reduce +
```

#####Problem 134
A nil key
```clojure
(fn [k m]
 (and (contains? m k)
      (nil? (m k))))
```

#####Problem 145
For the win
```clojure
'(1 5 9 13 17 21 25 29 33 37)
```

#####Problem 156
Map Defaults
```clojure
#(zipmap %2 (repeat %1))
```

#####Problem 161
Subset and Superset
```clojure
#{1 2}
```

#####Problem 162
Logical falsity and truth
```clojure
1
```
