# Secretary-problem


W klasycznym problemie sekretarek zakładamy, ze przesłuchujemy kolejno N kandydatek o róznym poziomie umiejetnosci. Po przesłuchaniu kazdej podejmujemy decyzje: przyjac ja lub odrzucic. Jezeli przyjmiemy ja, pozostałe odprawiamy. Jezeli 
odrzucimy ja, nie mozemy jej złozyc ponownie oferty. Celem gry jest znalezienie strategii gwarantujacej wybór najlepszej kandydatki z najwyzszym prawdopodobienstwem. Problem ten ma rozwiazanie scisłe: nalezy przesłuchac r = N/e pierwszych
kandydatek, sprawdzic, jaki był najwyzszy poziom umiejetno sci wsród nich, po czym sposród pozostałych N − r kandydatek wybrac pierwsza, której poziom umiejetno sci bedzie wyzszy od wczeniej zbadanego maksimum. Prawdopodobienstwo znalezienia optymalnej kandydatki dla duzych N jest bliskie 1/e.
Problem jest nastepujacy. Przesłuchujemy kolejno 80 analityków, 100 programistek i 120 testerów o umiej˛etnosciach b˛ed ˛acych liczbami losowymi z rozkładu N(M,S),
gdzie M ∼ N(0,1), S ∼ U(0.8,1.5) (przy przesłuchiwaniu kandydatów nie wiemy z jakiego rozkładu pochodza ich umiejetnosci; zmienne M,S generujemy raz na poczatku -
zapobiegaja one wykorzystaniu exploitów do tego problemu). Odrzuceni kandydaci nie
wracaja. Potrzebujemy zatrudnic 3 analityków, 3 programistki i 3 testerów. Za pomoca metod Monte-Carlo opracuj (np. symulacyjnie) strategie, która z duzym prawdopodobienstwem bedzie nam zwracac najlepszych kandydatów, mianowicie

• zmaksymalizujemy prawdopodobienstwo π, ze wszyscy trzej analitycy beda najlepsi sposród grupy kandydatów 

• zmaksymalizujemy srednia sume σ umiejetnosci trzech zatrudnionych programistek

• zmaksymalizujemy prawdopodobienstwo ρ, ze wszyscy trzej zatrudnieni testerzy znajda sie wsród 10% najlepszych sposród kandydatów.

Po zatrudnieniu pracowników o umiejetnosciach a1,a2,a3, p1, p2, p3,t1,t2,t3 (kolejno analitycy, programistki, testerzy) przychodzi czas na wybór zlecen do zrealizowania. Przegladamy zlecenia kolejno w nieskonczonosc tak długo az wybierzemy z nich trzy, jednak za kazde z nich musimy zapłacic kwote bedaca zmienna losowa o rozkładzie wykładniczym ze srednia max {0.5,2.5 − min{a1,a2,a3}}.
Wartosc kazdego pojawiajacego sie zlecenia jest zmienna losowa z rozkładu wykładniczego o sredniej równej sumie umiejetnosci zatrudnionych programistek. ´ Jesli ta suma jest ujemna,to wartosci zlecen sa zmiennymi losowymi X, gdzie X jest zmienna losowa z rozkładu wykładniczego o sredniej równej minus suma umiejetnosci programistek.
Do kazdego zlecenia przyporzadkowujemy jednego testera. Tester o umiejetnosci ti wykrywa bład w swoim zleceniu z prawdopodobienstwem Φ(ti), gdzie Φ jest dystrybuanta rozkładu normalnego. Jesli tester nie wykryje błedu, to zapłata za zlecenie przepada.

• Wybierz strategie przyjmowania zlecen i przydzielania do nich testerów tak, aby zmaksymalizowac oczekiwany zysk z.

• Narysuj histogram zysków uzyskiwanych na podstawie przyjetej strategii zatrudniania pracowników i przyjmowania zlecen i oszacuj prawdopodobienstwo 
bankructwa (tzn. uzyskania ujemnych zysków).
