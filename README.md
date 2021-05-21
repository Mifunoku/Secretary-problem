# Secretary-problem

#ENGLISH VERSION

The basic form of the problem is the following: imagine an administrator who wants to hire the best secretary out of {\displaystyle n}n rankable applicants for a position. The applicants are interviewed one by one in random order. A decision about each particular applicant is to be made immediately after the interview. Once rejected, an applicant cannot be recalled. During the interview, the administrator gains information sufficient to rank the applicant among all applicants interviewed so far, but is unaware of the quality of yet unseen applicants. The question is about the optimal strategy (stopping rule) to maximize the probability of selecting the best applicant. If the decision can be deferred to the end, this can be solved by the simple maximum selection algorithm of tracking the running maximum (and who achieved it), and selecting the overall maximum at the end. The difficulty is that the decision must be made immediately.The optimal stopping rule prescribes always rejecting the first {\displaystyle \sim n/e}{\displaystyle \sim n/e} applicants that are interviewed and then stopping at the first applicant who is better than every applicant interviewed so far (or continuing to the last applicant if this never occurs). Sometimes this strategy is called the 1/e stopping rule, because the probability of stopping at the best applicant with this strategy is about {\displaystyle 1/e}1/e already for moderate values of n.  ~Wikipedia

The problem is as follows. We interview successively 80 analysts, 100 programmers and 120 testers with skills that are random numbers from the N(M, S) normal distribution,
where M ∼ N (0,1), S ∼ U (0.8,1.5) (when interviewing candidates we do not know what distribution of their skills comes from; the variables M, S are generated once at the beginning -
they prevent exploits from being used for this problem). Rejected candidates do not coming back. We need to hire 3 analysts, 3 programmers and 3 testers. Using the Monte-Carlo method, develop (e.g. simulation) strategies that will most likely return the best candidates to us:

• we will maximize the probability π that all three analysts will be the best among the group of candidates

• we will maximize the average sum σ of skills of three employed programmers

• we will maximize the probability ρ that all three hired testers will be among the top 10% of candidates.

After hiring employees with the skills a1, a2, a3, p1, p2, p3, t1, t2, t3 (analysts, programmers, testers in turn), it is time to choose the orders to be carried out. We look through the orders indefinitely until we choose three of them, but for each of them we have to pay the amount of a random variable with an exponential distribution with the average max {0.5,2.5 - min {a1, a2, a3}}.
The value of each appearing order is a random variable from the exponential distribution with an average equal to the sum of the skills of the employed programmers. If this sum is negative, the order values are random variables X, where X is an exponential random variable with the mean minus the sum of the programming skills.
We assign one tester to each order. A tester with the ability ti detects an error in this order with a probability of Φ (ti), where Φ is the cumulative distribution of the normal distribution. If the tester does not detect an error, the payment for the order is forfeited.

• Choose strategies for accepting orders and assigning testers to them so as to maximize the expected profit.

• Draw a histogram of the profits obtained on the basis of the adopted strategy of hiring employees and accepting orders and estimate the probability
bankruptcy (i.e. obtaining negative profits).





#POLISH VERSION (originally)




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
