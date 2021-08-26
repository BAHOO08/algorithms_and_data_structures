# Алгоритмы поиска

- [Бинарный поиск](#binary-search)
- [Тернарный поиск](#ternary_search)


<a href="binary-search"></a>
### Бинарный поиск

Поиск в отсортированном массиве. Заключается в том, что массив делится на половины.

Простая реализация на языке с++

```c++
int search(vector<int>& nums, int target) {
        int left = 0;
        int right = nums.size() - 1;
        while(left <= right)
        {
            int mid = left + (right - left) / 2; 
            if(nums.at(mid) == target)
            {
                return mid;
            }
            else if(nums.at(mid) < target)
            {
                left = mid + 1;
            }
            else
            {
                right = mid - 1;
            }    
        }
        return -1;
    }
```

Приведённый код представляет собой функцию, которая принимает вектор и элемент target, который хотим найти.
