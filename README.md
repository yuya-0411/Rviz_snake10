# snake
URDFとそれをRviz上に表示するプログラムを格納

## フォルダ構成

snake_rviz
- launch
  - snake_rviz.launch
- mesh
  - adaptor.stl
  - dynamixel.stl
- rviz
  - snake10.rviz
- urdf
  - snake_stl.xacro
- CMakeLists.txt
- package.xml

## xacroとurdf
urdfフォルダの中にはurdfファイルの代わりにxacroファイルが入っている。
urdfファイルでも構わないが、urdfを作成する際にxacroで作っておいた方が汎用性を高められる。
urdfファイルが必要な際は以下のようにしてxacroファイルからurdfファイルを作成することができる。

xacroファイルのあるディレクトリに移動
```
rosrun xacro xacro snake_stl.xacro >snake_stl.urdf
```

xacroファイルについては以下のサイトが参考になる。
- https://qiita.com/srs/items/43528d00ee789171367f
- https://gbiggs.github.io/rosjp_urdf_tutorial_text/manipulator_urdf.html
