# vscode
## Windows下pipenv将虚环境文件的位置设置在项目根目录下   
在windows下使用pipenv shell时，虚拟环境文件夹会在C：\Users\Administrator\.virtualenvs\目录下默认创建，为了方便管理，将这个虚环境的文件的位置更改一下。

新建一个名为“ WORKON_HOME ”的环境变量（如果已存在就忽略此步骤），然后将环境变量的值设置为“ PIPENV_VENV_IN_PROJECT ” （其他名字也行？还试过）

我觉得重点是在 WORKON_HOME 这个变量名。


![环境变量设置](https://img2018.cnblogs.com/blog/1242355/201812/1242355-20181202165716332-1135930178.png "WORKON_HOME")

完毕后使用 pipenv shell 时会在当前项目的文件夹里看到一个 “PIPENV_VENV_IN_PROJECT”的文件，然后里面就有虚环境的文件了。