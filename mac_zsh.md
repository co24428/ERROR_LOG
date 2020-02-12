~~~
  To update your account to use zsh, please run `chsh -s /bin/zsh`.
~~~  
시키는대로 했더니 갑자기 jupyter notebook이 안먹혔다.  

<hr>
찾아보니 bash를 업데이트한 것이라고 하고 설정 파일이 달라졌다고 한다.
- 기존의 ~/.bash_profile => ~/.zshrc  

확인차 PATH를 확인해보았다.
~~~
  echo $PATH
~~~  
어제까지만 해도 있었던 하둡 설정이 사라졌다..  

~~~
  vi ~/.bash_profile
~~~  
파일 자체에는 설정해주는 코드가 있었기에 copy&paste  
그대로 긁어서 zshrc의 아래 부분에 추가
~~~
  vi ~/.zshrc
~~~  
터미널 재실행하여 source 작업(등록)
~~~
  source ~/.zshrc
~~~  

다시 해보니 경로가 전체 경로가 다시 잡히는 것이 확인되었다.  
~~~
  echo $PATH
~~~  
