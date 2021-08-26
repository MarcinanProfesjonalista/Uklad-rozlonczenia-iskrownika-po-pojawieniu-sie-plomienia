# Uklad-rozlonczenia-iskrownika-po-pojawieniu-sie-plomienia
Opis

![alt text](https://github.com/MarcinanBarbarzynca/Uklad-rozlonczenia-iskrownika-po-pojawieniu-sie-plomienia/blob/main/IMG_20210826_142713.jpg)

## Co to jest?
Układ rozbudowuje funkcję kontrolera iskrownika planika gazu. Wystąpił problem z wyłączeniem iskry po odpaleniu ognia. Układ podawał iskrę cały czas, co doprowadzało do uszkodzenia generatora iskry. Po wymianie układu sterowania odkryto że można założyć do niego datkowy czujnik temperatury. Na wyjściu ukłądu pomiarowego otrzymałem napięcie stałe, które wpuściłem w mosfetową bramkę NOT i teraz iskra jest podawana cały czas do momentu pojawienia się płomienia. Przewód sterowania trafem przepuszczono przez SSR który jest sterowany "nowym układem kontroli iskry"

Link do edytora. 
https://oshwlab.com/polaski/za-cznik-iskrownika

Aby odtworzyć układ zobacz sobie co to mosfet Not gate.

## Algorytm działania:
1. Sterownik głowny załącza "nowy" układ pomocniczy dla iskrownika
2. Uruchomiony układ kontrolera iskrownika sprawdza temperaturę za pomocą dodatkowej sondy (tj. świecy nazwanej czujnikiem)
3. "nowy" układ zezwala na działanie cewki iskrownika aż do momentu otrzymania sygnału 6V od kontrolera
4. Po pojawieniu się płomienia kontroler badający temperaturę daje sygnał na "nowy" układ iskrownika a on wyłącza cewkę. 

## Prawidłowa funkcja działania:
Po pojawieniu się ognia gaśnie iskra.


