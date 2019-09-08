1. 开始之前
	 - 创建~/.spacemacs.d/目录，并将 ~/.spacemacs copy 到这个目录
	 - 或者直接clone 这个仓库. git clone git@github.com:hellochengkai/ck_spacemacs.git ~/.spacemacs.d

2. 拼写检查spell报错

   1. ```
      Error enabling Flyspell mode:
      (Error: No word lists can be found for the language "zh_CN".)
      ```

   2. [http://blog.lujun9972.win/blog/2018/02/07/%E4%BD%BF%E7%94%A8aspell%E6%A3%80%E6%9F%A5%E8%8B%B1%E6%96%87%E6%8B%BC%E5%86%99%E9%94%99%E8%AF%AF/](http://blog.lujun9972.win/blog/2018/02/07/使用aspell检查英文拼写错误/)

   3. https://emacs-china.org/t/spacemacs-flyspell/2158

   4. ```
      sudo pacman -S aspell aspell-en
      pacman -Ss aspell
      aspell dump modes
      
      ;; use aspell as ispell backend
      (setq-default ispell-program-name "aspell")  
      ;; use American English as ispell default dictionary  
      (ispell-change-dictionary "american" t)
      ```