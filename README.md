Jak wyeksportować stan bota postawionego na FatherBot? 
Chodzi o coś jak kontener. 

Czy nowa instancja FatherBota może zostać stworzona w sposób zautomatyzowany, na VPSie? 

Komponenty niezbędne do działania: 
	- Bot, ten z githuba, będzie mógł być dostosowany do naszych potrzeb, bo kod jest dostępny 
    https://github.com/Der-Henning/tgtg
	- ChatID użytkownika - unikalny chatID, każdy użytkownik dostaje inny 
	- Token bota - bot może obsługiwać wielu użytkowników, a token jest jeden 
	- Metody na przesłanie tokenów do programu docelowego
    - Wuchty wolnego czasu na ogarnięcie tego pierdolnika

O co tu chodzi?
Bot odpowiada na najbardziej palącą potrzebę każdego człowieka - pożywienie. 
Pożywienie można otrzymać w restauracji, sklepie, albo w domu rodziców. 
Co w takim razie robilibyśmy lepiej? Skutecznie łączyli owe miejsca. 
Istnieją serwisy, które to robią: pyszne.pl, wolt, uber eats. 
Ich problemem jest to, że cena jest standardowa, a nawet wyższa. Do tego dochodzi prowizja, którą pobierają te serwisy. Problem ceny rozwiązują inne serwisy takie jak:
TooGoodToGo, Foodsi i Facebookowe grupki.
Tam cena towaru jest niższa, bo są tam paczki niespodzianki, ale użytkownik nie otrzymuje powiadomień. Taka jest ich idea, aby dawać równe szanse. 
Usługa Foodie-Woodie rozwiązuje ten problem poprzez wysyłanie użytkownikowi powiadomień na temat nowych paczek. Korzystając z Foodie-Woodie dostajemy dostęp do tańszego pożywienia i o to chodzi.

PoC, DoD, JwP
Definition of Done czyli tłumacząc na polski jakoś-to-działa to w przypadku tej usługi: 
	- Czat-bot na Telegram, który umożliwia dostęp do powiadomień w TooGoodToGo.
	- Zanim użytkownik dostanie się do tej usługi powinien on przejść przez krótką inicjację. Od usera potrzebujemy przede wszystkim lokalizacji. Weryfikacji użytkownika w jakiś sposób - to załatwia nam Telegram, bo do TG podpięty jest numer telefonu, więc tak można zidentyfikować użytkownika. Inicjacja ma dać wsad niezbędnych danych do bota właściwego.
	- Informacje, czyli współrzędne i tokeny powinny być przechowywane w osobnym pliku - najlepiej szyfrowanym.
	- Usługa musi działać na naszych urządzeniach co najmniej tydzień, żebyśmy wiedzieli o tym, czy jest niezawodna. Tydzień to niby niewiele, ale po tygodniu możemy złapać wnioski płynące z korzystania i udostępnić serwis beta-testerom.
	- Grafiki - od samego rozpoczęcia korzystania z bota, od inicjacji użytkownik ma zostać wciągnięty i "attracted". Kolorowe grafiki tłumaczące procesy konfiguracji, ograniczenie tekstu do minimum, klawiatura zawierająca tylko opcje do wyboru, suwaki i menu kontekstowe zamiast ręcznego wpisywania wartości.
	- Proces płatności - użytkownik ma być w stanie w prosty sposób zapłacić za usługę. Na początku (pierwszy tydzień/miesiąc) byłby bezpłatny. Ten punkt może przysporzyć największy kłopot, bo do obsługi tego trzeba by mieć działalność. Płatności w krypto są mało user-friendly, a BLIKi wyglądają podejrzanie. Płatność jednak, to najmniejszy problem, którym martwić będzie się można dopiero po wydaniu wersji wstępnej.

Zespół odpowiedzialny za produkt
Rafał Wiśniewski - coder
Michał Laskowski - integrator
Olka Moryson - designer