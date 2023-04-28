### GeoPandas / OSMNX 실습  
  
-- 강의자료의 코드대로 했을 때 오류 발생하는 경우가 다수 보임  
1. NoneType Error -> 실습 시 사하구의 도로 환경 등이 바뀌어서 기존과 데이터가 살짝 달라진 것으로 보입니다. 해결은 if문으로 None인 경우를 제외했습니다.  
2. 구글 Colab에서 numpy와 scipy 버전 충돌 문제가 발생하는 경우가 있습니다. 그래서 anaconda, jupyter lab으로 실습했습니다.  
3. descartes 모듈 오류로 실행되지 않는 경우가 있습니다. (등시성 맵 구현 부분) 이것은 코드 수정으로 해결해야 합니다. 같은 폴더에 있는 patch.py가 해당 내용입니다.
다음 경로를 따라가(컴퓨터마다 다릅니다.) 수정해야합니다. \~/anaconda3/envs/python/Lib/site-packages/descartes 여기에서 patch.py를 열고 63~64번 줄의 내용을 다음과 같이 바꿉니다.
```python
        concatenate([asarray(t.exterior.coords)[:, :2]] +
                    [asarray(r)[:, :2] for r in t.interiors])
```  

줄맞춤에 유의하시기 바랍니다.
