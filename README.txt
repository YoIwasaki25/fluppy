C++とSFLMを使ってFlappyBirdをつくる。


HomebrewでSFLMをいれる


コンパイル方法

 clang++ -stdlib=libc++  main.cpp -I /usr/local/Cellar/sfml/2.5.1/include -o main -L /usr/local/Cellar/sfml/2.5.1/lib/ -lsfml-graphics -lsfml-window -lsfml-system


 export LD_LIBRARY_PATH=/usr/local/Cellar/sfml/2.5.1/lib && ./main