Tema 1 - Skyscrapers
Analiza Algoritmilor

Task 1
Pentru task 1 am parcurs doar liniile din matrice si am verificat fiecare combinatie unde o cifra nu se poate repeta

Task 2
Prima oara parcurg pana gasesc ":" si le transform in ";" pt. viitor. Ma mut o pozitie la dreapta, codific cifra intr-un caracter corespunzator doar ei (1 - A, 2 - B, 3 - C, 4 - D), si trec in doua noi stari intermediare care trec peste si schimba urmatoarele ":" pana se ajunge la urmatoarea linie. La final dau reset si o iau de la capat, de data asta merg ignorand toate ";" pe care le-am setat si ma opresc doar cand gasesc o literea, caz in care "repar" caracterul respeciv pt. a fi din nou cifra si ma mut pe urmatoarea pozitie si testez din nou combinatiile.
La final, in caz ca a ramas vreun caracter nereparat,  am o stare care repara tot inputul pt. a fi ca la inceput.

Task 3
La task 3, pe vizibilitatea pe linii, implementarea este asemanatoare cu cea de la task 1, dar aici nu verific decat daca nu se repeta anumite cifre.
Aici verific combinarile posibile pentru fiecare visibilitate, dar verific doar primele 3 cifre din fiecare linie, deoarece ultima s-ar stii care este datorita task-urilor
de mai devreme.
Pt. vizibilitate 1: 4 trebuie sa fie pe prima pozitie
Pt. vizibilitate 2: 14	312
                    24	321
                    34
                    214
                    314
                    324
            Aceste combinari trebuie verificare incepand de la prima pozitie, ce vine dupa ultimul caracter scris nu are sens sa fie verificat deoarce stim care ar fi sau nu ar conta.
Pt. vizibilitate 3: 213
                    231
                    234
                    124
                    132
                    134
Pt. vizibilitate 4: 1234

La final trebuie facuta o parcurgere si din dreapta in stanga pentru a verifica vizibilitatea din partea dreapta a liniilor.

Pt. vizibilitatea pe coloane, implementarea se inspira de la cea de la task 2, iar verrificarile pt. vizibilitati sunt exact la fel ca la linii. Diferenta intre task 2 si Viz. pe Col. este ca nu repar
fiecare litera cand o intalnesc. Astfel la final o sa am un input aproape total codificat. In caz ca imi scapa vreun caracter necodificat, atunci am o stare care codifica tot ce a scapat.
La final, pentru a verifica vizibilitatea de jos, fac acelasi lucru doar ca pe litere in loc de cifre.
Pentru orice caz, mai am o stare care repara tot sirul pentru a fi exact ca la inceput.
