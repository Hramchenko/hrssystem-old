# hrssystem
HRS Reconstruction System

В данной работе предложена модификация алгоритма объёмного удаления, который был предложен **Brian Cureless** и **Mark Levoy** в статье **«A Volumetric Method for Building Complex Models from Range Images»**.  Этот метод предполагает разбиение пространства на множество элементарных кубических элементов(вокселов), с последующей проверкой принадлежности воксела объёму объекта. В случае, если воксел не лежит внутри объекта, то он должен быть удалён, иначе ему присваивается метка принадлежности объекту. Для представления модели объекта был применён метод иерархического разбиения пространства, предложенный **Kari Pulli** в работе **«Acquisition and visualization of colored 3D objects»**. 

Для определения принадлежности воксела объёму объекта, его необходимо спроектировать на плоскость изображения, полученного с камеры, и сопоставить проекцию и силуэт объекта. Задачу по проектированию можно разбить на три этапа: проецирование вершин воксела на плоскость изображения, растеризация рёбер и заливка площади, ограниченной проекциями рёбер. Если первый этап сводится к простому умножению матриц, то реализация второго и третьего этапов является трудной задачей. 

В данной работе применён новый подход к маркировке вокселов: алгоритмы проецирования вокселов на плоскость изображения, заменены графическим построением на GPU, с последующим сравнением силуэта объекта и в результатов рендеринга. 

Более подробная информация приведена в [презентации...](https://github.com/Hramchenko/hrssystem/blob/master/Docs/hrssystem.pdf)

![Снимок экрана](https://github.com/Hramchenko/hrssystem/blob/master/Docs/stand.png)

![Снимок экрана](https://github.com/Hramchenko/hrssystem/blob/master/Docs/img8.jpeg)

![Снимок экрана](https://github.com/Hramchenko/hrssystem/blob/master/Docs/img2.jpeg)

![Снимок экрана](https://github.com/Hramchenko/hrssystem/blob/master/Docs/img1.jpeg)

