## 📚 C++ STL Data Structures and Their Methods

---

### 🧱 Vector (`#include <vector>`)

```cpp
std::vector<int> v;
```

* `v.push_back(x)`
* `v.pop_back()`
* `v.size()`
* `v.clear()`
* `v.empty()`
* `v[i]`
* `v.front()`, `v.back()`
* `v.begin()`, `v.end()`
* `v.insert(it, x)`
* `v.erase(it)`
* `sort(v.begin(), v.end())`

---

### 🔁 Deque (`#include <deque>`)

```cpp
std::deque<int> dq;
```

* `dq.push_back(x)`
* `dq.push_front(x)`
* `dq.pop_back()`
* `dq.pop_front()`
* `dq.front()`, `dq.back()`
* `dq.size()`
* `dq.empty()`
* `dq.begin()`, `dq.end()`

---

### 🧺 List (`#include <list>`)

```cpp
std::list<int> l;
```

* `l.push_back(x)`
* `l.push_front(x)`
* `l.pop_back()`
* `l.pop_front()`
* `l.insert(it, x)`
* `l.erase(it)`
* `l.size()`
* `l.empty()`
* `l.begin()`, `l.end()`
* `l.reverse()`
* `l.sort()`

---

### ✖️ Stack (`#include <stack>`)

```cpp
std::stack<int> st;
```

* `st.push(x)`
* `st.pop()`
* `st.top()`
* `st.empty()`
* `st.size()`

---

### 🚪 Queue (`#include <queue>`)

```cpp
std::queue<int> q;
```

* `q.push(x)`
* `q.pop()`
* `q.front()`
* `q.back()`
* `q.size()`
* `q.empty()`

---

### 🤑 Priority Queue / Max-Heap (`#include <queue>`)

```cpp
std::priority_queue<int> pq;
```

* `pq.push(x)`
* `pq.pop()`
* `pq.top()`
* `pq.size()`
* `pq.empty()`

> For Min-Heap:

```cpp
std::priority_queue<int, std::vector<int>, std::greater<int>> minpq;
```

---

### 🔠 Set (`#include <set>`)

```cpp
std::set<int> s;
```

* `s.insert(x)`
* `s.erase(x)`
* `s.find(x)`
* `s.count(x)`
* `s.size()`
* `s.empty()`
* `s.begin()`, `s.end()`
* `s.lower_bound(x)`, `s.upper_bound(x)`

---

### 🪜 Unordered Set (`#include <unordered_set>`)

```cpp
std::unordered_set<int> us;
```

* `us.insert(x)`
* `us.erase(x)`
* `us.find(x)`
* `us.count(x)`
* `us.size()`
* `us.empty()`

---

### 💎 Map (`#include <map>`)

```cpp
std::map<int, string> m;
```

* `m[key] = value`
* `m.at(key)`
* `m.insert({key, value})`
* `m.erase(key)`
* `m.find(key)`
* `m.count(key)`
* `m.size()`
* `m.empty()`
* `m.begin()`, `m.end()`

---

### 💰 Unordered Map (`#include <unordered_map>`)

```cpp
std::unordered_map<int, string> um;
```

* `um[key] = value`
* `um.at(key)`
* `um.insert({key, value})`
* `um.erase(key)`
* `um.find(key)`
* `um.count(key)`
* `um.size()`
* `um.empty()`

---

## 🔧 Useful Inbuilt C++ Functions (From `<algorithm>` and `<cmath>`)

### Sorting & Searching

* `sort(v.begin(), v.end())`
* `reverse(v.begin(), v.end())`
* `binary_search(v.begin(), v.end(), x)`
* `lower_bound(v.begin(), v.end(), x)`
* `upper_bound(v.begin(), v.end(), x)`
* `max(a, b)`, `min(a, b)`
* `swap(a, b)`

### Math Functions

* `pow(a, b)`
* `sqrt(x)`
* `abs(x)`
* `ceil(x)`
* `floor(x)`
* `log(x)`
* `sin(x)`, `cos(x)`, `tan(x)`

### Bit Manipulation

* `__builtin_popcount(x)` – Number of 1s
* `__builtin_ctz(x)` – Count trailing zeros
* `__builtin_clz(x)` – Count leading zeros

---

Let me know if you want the Markdown with code samples for each too!
