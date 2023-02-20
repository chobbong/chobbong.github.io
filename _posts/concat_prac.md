```python
import pandas as pd

# 중복 열 이름을 가진 예시 데이터프레임 생성
dataframe_1 = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
dataframe_2 = pd.DataFrame({'A': [7, 8, 9], 'B': [10, 11, 12]})

# 열 이름이 중복되는 데이터프레임 연결 - 열로 나열
combined_dataframe = pd.concat([dataframe_1, dataframe_2], axis=1, ignore_index=True)

# 결과 출력
print(combined_dataframe)
```

       0  1  2   3
    0  1  4  7  10
    1  2  5  8  11
    2  3  6  9  12



```python
# 열 이름이 중복되는 데이터프레임 연결 - 행으로 나열
combined_dataframe_2 = pd.concat([dataframe_1, dataframe_2], axis=0, ignore_index=True)

# 결과 출력
print(combined_dataframe_2)
```

       A   B
    0  1   4
    1  2   5
    2  3   6
    3  7  10
    4  8  11
    5  9  12


