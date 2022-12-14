В данной лабораторной работе необходимо было реализовать перемножение матриц. Работа выполнялась на GPU и CPU.

На gpu работа выполнялась с использованием cuda. Механизм следующий: на хосте выделялась память под переменные, далее они инициализировались и отправлялись на девайс, где происходили вычисления, и уже оттуда отправлялись обратно на хост.
Т.к. видеокарта считает очень быстро, то необходимо было использовать библиотеку chrono и засекать время в наносекундах.
Распаралеливалось умножение строки на столбец.
Для проверки результата выполнялось умножение матриц на cpu, и результат сравнивался непосредственно с результатами на gpu.

Ниже на графике приведено время работы каждого из методов в наносекундах. Очевидно, что на видеокарте вычисления идут в разы быстрее, чем на процессоре.

![image](https://user-images.githubusercontent.com/87262680/205246814-b5b0dae2-ff5e-4f32-b117-7bd8c7d6e1f7.png)

Ниже приведен график ускорения работы алгоритма(время выполнения работы последовательного варианта, на время работы параллельного)

![image](https://user-images.githubusercontent.com/87262680/205247540-ea8d04cd-5340-471b-bc7d-56a94ae722af.png)
