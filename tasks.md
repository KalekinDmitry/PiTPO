# Задачи со звёздочкой. Сразу на автомат. Без лаб. Без других задач.
(достаточно любых двух, можно не делать лабы и не решать другие задачи)  

1. Перебрать все варианты шахматных ходов за две стороны глубиной 5 и найти все случаи, когда одна из сторон ставит мат.    
Результат вывести в виде статистики:   
мат в два хода: 1 комбинация,   
мат в три хода 16 комбинаций,   
мат в 4 хода...   
Посмотреть партии по номерам, где достигается мат, можно в формате PGN. [https://ru.wikipedia.org/wiki/Portable_Game_Notation]  
Можно вывести партию в консоль или сбросить в файл - опционально.  
Перебирать варианты нужно в несколько потоков.  


2. Написать клиент для REST-API сервера.  
Эндпоинты моего сервера будут чуть позже вида:  
`GET /game/create` - создать игру  
`GET /game/{game_id}` - получить состояние игры в формате FEN [https://ru.wikipedia.org/wiki/Нотация_Форсайта_—_Эдвардса] и сторону, за которую ходить   
`POST /game/{game_id}/move` - отправить ход в формате PGN.  
Ваш клиент цепляется к серверу, создаётся игра. Возможно подцепиться несколькими клиентами.  
Клиенты с периодичностью опрашивают сервер и совершают ходы.  


3. Еще не придумано - зарезервировал

4. Еще не придумано - зарезервировал




# Задачи, которые необходимо прорешать в течение семестра 

1. **Шахматный конь**  

Дано крестообразное поле. N - стартовая позиция коня.  
Обойти всё поле, побывав в каждой клетке по одному разу.  
Найти все такие маршруты.   
```
......[ ][ ]......
......[ ][ ]......
[ ][ ][ ][ ][ ][ ]
[ ][ ][ ][ ][ ][ ]
......[ ][ ]......
......[ ][N]......
```








---------------------  Ниже наброски из практики, не смотрите сюда ) ----------------------


```
m*n
A*
[a][0][0][0][0][9]
[6][5][.][.][.][.]
[.][7][5][.][.][.]
[.][.][.][8][.][.]
[.][.][6][.][.][.]
[.][.][.][.][.][b]

N = (m-1) + (n-1)

for (i=0; i<2^N; i++)
	i--> Бинарное представление, дополненное 
	слева нулями 000000000000


0000000000000000 -- код маршрута
0000000000000001
0000000000000010
...
1111111111111111


0000
0001

0001
0010

0010
0011
```










 
