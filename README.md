# Park Rozrywki

## Cel Projektu:
Celem projektu jest stworzenie kompletnego systemu analizy danych, obejmującego bazy danych, hurtownię danych (ETL), model OLAP oraz interaktywne dashboardy w środowisku Power BI Desktop.

Projekt jest realizowany w zespołach pięcioosobowych na potrzeby przedmiotu Analityczne Bazy Danych (ABD).

## Narzędzia:

- **SQL Server Management Studio 19**
- **Toad Data Modeler 7.2**
- **Visual Studio 2019**

Projekt realizowany jest w zespołach pięcioosobowych i składa się z 4 etapów.

## Organizacja Pracy:

### Ukończone: 
#### ETAP I (26.02.2024 - 11.03.2024)
**Cel:** Opracowanie dwóch relacyjnych baz danych w środowisku MS SQL Server.

BAZA I

![BazaI](img/schematpierwszy.png)

BAZA II

![BazaII](img/schemat1.jpg)


### W trakcie: 
#### ETAP II (11.03.2024 - 15.04.2024)
**Cel:** Celem tego etapu projektu jest implementacja hurtowni danych przy użyciu technologii ETL (Microsoft SQL Server Integration Services - SSIS) oraz opartej na modelu konstelacji gwiazdy. Celem jest stworzenie dwóch tabel faktów oraz pięciu tabel wymiarów.

**Projekt gwiazdy**
  
Pierwsza faza polegała na zaprojektowaniu modelu gwaizdy dla każdej z dwóch wcześniej stworzonych baz relacyjnych.
  
**ODS**
  
Następnie wcześniej stworzony model danych został poddany kolejnej modyfikacji, celem utworzenia warstwy pośredniej między systemem OLTP a hurtownią danych. Po zdefiniowaniu struktury ODS, skonfigurowano procesy w środowisku Visual Studio, umożliwiające pobieranie danych z baz źródłowych do ODS. Opracowano również mechanizm inkrementalny, który pozwala na przesyłanie do ODS tylko tych rekordów z baz źródłowych, które uległy zmianie.



BAZA I
1. Modelowanie i implementacja schematu struktur hurtowni danych - stoworzenie modelu konstelacji gwiazdy
   
   ![Model gwiazdy baza I](img/schematFaktBiletu.png)
   
2. Modelowanie schematu struktur ODS
   
   ![ODS 1](img/scheamt_ODS.png)

BAZA II
1. Konstelacja gwiazdy dla bazy drugiej
   ![Model gwiazdy baza II](img/gwiazda2.png)
2. ODS dla bazy drugiej 
   ![ODS 2](img/ods2.png)



#### ETAP III (15.04.2024 - 13.05.2024)
- **Cel:** Projekt i implementacja modelu OLAP w formie bazy tabelarycznej (MS SSAS) wraz z
zasilaniem

Etap 3 polegał na zaprojektowaniu i implementacji modelu OLAP w technologii SSAS Tabular na podstawie wcześniej przygotowanej hurtowni danych. Zbudowano model tabelaryczny obejmujący fakty „Bilety” i „AkcjaMarketingowa”, utworzono relacje między tabelami oraz dodano kluczowe miary analityczne, takie jak całkowity przychód, średni koszt biletu, liczba wejść, liczba unikalnych klientów czy koszty kampanii. Wprowadzono również perspektywy tematyczne (np. Marketing, Uczestnik) w celu uproszczenia analiz. Na podstawie modelu przygotowano raporty w Excelu w formie tabel przestawnych. Podjęto także próbę wdrożenia mechanizmu codziennego odświeżania danych, jednak ze względu na ograniczenia techniczne nie został on w pełni uruchomiony.

#### ETAP IV (13.05.2024 - 03.06.2024)
- **Cel:** Dashboardy w narzędziu analizy Microsoft Power BI Desktop.

W tym etapie przygotowano interaktywne dashboardy w Power BI na podstawie modelu SSAS Tabular. Opracowane raporty prezentują analizę sprzedaży biletów, koszty działań marketingowych, lokalizacje wydarzeń oraz dane statystyczne dotyczące uczestników.



