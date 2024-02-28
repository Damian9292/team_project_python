Cel i opis projektu
Pracujesz w zespole jako analityk danych. Do Twoich codziennych obowiązków należy pozyskiwanie, składowanie oraz interpretacja danych i wydanie rekomendacji na ich podstawie.

Ponieważ zadań jest coraz więcej, postanowiono, że mają zostać zatrudnione nowe osoby na następujące stanowiska:

data analyst,
data engineer,
data scientist
w celu sprawniejszego dostarczania rekomendacji dla klienta wewnętrznego.

Zespół HR poprosił Twojego szefa, aby dostarczył następujące informacje:

jaki jest szacunkowy wydatek na zatrudnienie takich ludzi,
jakie widełki powinna zawierać każda z ofert,
w jakich miastach można zatrudnić takie osoby,
czy istnieje możliwość, aby zespół został powołany w jednym mieście.
Oferty zatrudnienia mają pojawić się na stronie nofluffjobs i ona ma zostać użyta jako podstawa do analizy.

Szkic przebiegu warsztatu
W trakcie rozwiązywania tego zadania będziemy korzystać z następujących modułów:

Selenium - do pobrania informacji o aktualnie istniejących ofertach pracy,
BeautifulSoup - w celu przetworzenia danych niestrukturyzowanych (kodu HTML) w dane tabelaryczne (DataSet),
Pandas - w celu wykonania transformacji danych,
MatplotLib - do prezentacji wyników.



Struktura projektu
Aby ułatwić sobie pracę w trakcie rozwiązywania warsztatu, przyjmiemy pewne założenia co do struktury projektu. Praca z tą samą strukturą pozwoli na uniknięcie dodatkowej pracy przy współdzieleniu rozwiązania.

project            <-- folder projektu np. CodersLab_Warsztat
|____ data         <-- folder, w którym znajdują się dane
|   |__ raw        <-- folder z danymi źródłowymi
|   |__ interim    <-- folder z danymi częściowo przetworzonymi
|   |__ processed  <-- folder z danymi gotowymi do analizy
|
|____ drivers      <-- folder ze sterownikami do Selenium
|
|____ notebooks    <-- folder z plikami *.ipynb
|
|____ venv         <-- (opcjonalnie) folder ze środowiskiem wirtualnym

data
W tym folderze znajdować się będą wszystkie dane, które wytworzysz w trakcie rozwiązywania zadania.

data/raw (dane źródłowe)
Tutaj umieścimy surowe pliki .html, pobrane ze strony NoFluffJobs. Będą to pliki nieprzetworzone, bez żadnej dodatkowej obróbki - innymi słowy czysta kopia html.

Pomijając kontekst projektu, często pliki źródłowe przychodzą w formie plików Excel, które łatwo ręcznie zmodyfikować. Dobra praktyka mówi o tym, że pliki źródłowe są nieedytowalne tj., wszystkie zmiany powinny być w skryptach, w celu późniejszej replikacji pracy.

data/interim (dane tymczasowe)
Tutaj będziemy zamieszczać wynik parsowania danych z folderu raw do postaci ramki danych zapisanej jako plik csv. Dopiero dane z tego folderu zostaną przekazane dalej w celu obróbki/transformacji.

data/processed (dane wynikowe)
Ten folder będzie zawierał dane wynikowe - oczyszczone, gotowe do dalszej analizy. W kontekście warsztatu to na ich podstawie będziemy wyciągać wnioski oraz rekomendacje.

drivers
Wymagane sterowniki do użycia Selenium

notebooks
Tutaj będziemy zamieszczać wszystko notebooki stworzone w trakcie warsztatu. Ich nazewnictwo powinno być następując <krok>-<opis>.ipynb, dzięki temu w momencie próby odtworzenia warsztatu będzie znana kolejność wykonywanych kroków.

venv (opcjonalny)
Folder zawierający wirtualne środowisko python'a wraz z zainstalowanymi tylko tymi paczkami, które są potrzebne do jego poprawnego działania. Opis tworzenia jest dodatkowo opisany w materiałach po zjeździe.



