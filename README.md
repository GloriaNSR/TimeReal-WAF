# TimeReal-WAF

Detector de script malicioso de login

WAF en tiempo real que recibe diferentes llamadas a endpoints de usuarios y detecta patrones de login repetidos durante X segundos. En el caso de que exista ese patrón en esa ventana de eventos, se decide banear a ese usuario durante un tiempo determinado.

Los eventos vendrán con el timestamp del evento, la ip origen y el endpoint que solicita.

El sistema debe simular los eventos, creamos un Waf que recibe los eventos y los filtra y banea a usuarios a través de la detección del patrón de ataque. Por último nuestro consumidor que devuelve datos agregados de los eventos filtrados por el waf.
