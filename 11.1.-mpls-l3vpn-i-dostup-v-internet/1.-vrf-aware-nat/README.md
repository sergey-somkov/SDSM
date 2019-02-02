# VRF-Aware NAT

Более правильный и чуть более масштабируемый вариант — настройка трансляции на Egress PE — на выходе в Интернет. В этом случае у нас есть центральный узел, где выполняются все операции, а клиенту не нужно делать ничего.  
![](https://habrastorage.org/getpro/habr/post_images/eb6/6e3/86c/eb66e386c1a85bda7fc9b0ce05aded85.png)

Единственное неудобство: несмотря на то, что, возможно, ни один клиент не подключен к Egress PE непосредственно, этому маршрутизатору придётся поддерживать все VRF, из которых нужно получать доступ в Интернет. Собственно, поэтому он и VRF-Aware.