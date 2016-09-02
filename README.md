# Đệ quy - Chia để trị
### 1. Tìm kiếm tuyến tính bằng phép đệ quy.
__Problem__
> Cho một mảng __A__ gồm __N__ phần tử và một số nguyên K.
Trả về _i_ mà __A[i] = K__. Nếu không tìm thấy trả về __NOT_FOUND__.

| INPUT | OUTPUT |
|-------|:--------:|
|5 2 | |
|3 1 2 4 6|3|


```
LinearSearch(A, low, high, K){
    if (high < low) return NOT_FOUND
    if A[low] = key
      return low
    return LinearSearch(A, low + 1, high, K)
}
```

### 2. Tìm kiếm nhị phân.
__Problem__
> Cho một mảng A đã sắp xếp gồm N phần tử và một số nguyên K. Trả về i mà A[i] = K.
Nếu không tìm thấy trả về giá trị i lớn nhất mà A[i] < K. Ngược lại nếu (k < A[low]), kết quả là (low - 1).

__Ví dụ__
> Cho mảng A[] = [3, 5, 8, 20, 30, 50, 60]

|Query| Result|
|-----|-------|
|`search(2)`|0|
|`search(3)`|1|
|`search(4)`|1|
|`search(20)`|4|

```
BinarySearch(A, low, high, K){
  if (high < low) return (low - 1)

  mid = low + (high - low)/2
  if key = A[mid] return (mid)

  else if key < A[mid]
    return BinarySearch(A, low, mid - 1, K)

  else return BinarySearch(A, mid + 1, high, K)

}
```
