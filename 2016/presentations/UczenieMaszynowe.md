#Uczenie maszynowe - czyli jak rozwi�zywa� nietrywialne problemy #

##Streszczenie##

Techniki uczenia maszynowego s� szeroko wykorzystywane w r�nych obszarach codziennego �ycia. Problemy takie jak klasyfikacja czy predykcja, kt�rych rozwi�zanie przy pomocy tradycyjnych algorytm�w si� nie sprawdza, mog� by� z powodzeniem implementowane metodami pozwalaj�cymi nauczy� program podejmowa� trafne decyzje. Python idealnie nadaje si� do wykorzystania tych technik, w czym pomaga bez ma�a kilkadziesi�t mniej lub bardziej wyspecjalizowanych bibliotek.

##Rozw�j znaczenia i metod uczenia mazynowego##

Gdy w roku 1965 na Uniwerstytecie Stanforda powstawa� system Dendral, nikt pewnie nie przypuszcza�, �e ledwie 50 lat p�niej uczenie maszynowe (machine learning, ML) b�dzie technik� wszechobecn�, z kt�rej korzystamy codziennie, niemal na ka�dym kroku.

Dendral by� specjalistycznym oprogramowaniem naukowym, s�u��cym do analizy, grupowania oraz rozpoznawania, nieznanych do tej pory cz�owiekowi, moleku� zwi�zk�w chemicznych. Uzyskane przez program rezultaty zosta�y opublikowane w literaturze naukowej. By�o to pierwsze w historii odkrycie dokonane bezpo�rednio przez komputer, a Dendral uwa�any jest za prekursora system�w wykorzystuj�cych uczenie maszynowe.

Motorem nap�dowym dynamicznego rozwoju technik sztucznej inteligencji oraz uczenia maszynowego by� wzrost ilo�ci gromadzonych danych. Wida� to dobrze na przyk�ad w dziedzinie biologii, gdzie pod koniec XX wieku intensywnie badano sposoby pozyskiwania informacji o sekwencjach nukleotydowych gen�w. W roku 2003 g�o�no by�o o zako�czeniu wielkiego projektu sekwencjonowania ludzkiego genomu (HGP, human genom project). Uzyskanie pierwszej sekwencji ca�ego genomu cz�owieka zaj�o naukowcom 13 lat i kosztowa�o a� 3 mld dolar�w. Dzi� jeste�my w stanie zsekwencjonowa� ca�y genom w ci�gu zaledwie kilku godzin, za kwot� rz�du jedynie tysi�ca dolar�w. Czyste, surowe dane niewiele jednak nam daj�. Nie jest dla nas przecie� wa�na sekwencja sama w sobie, ale wynikaj�ce z niej wnioski, takie jak okre�lenie sk�onno�ci i ryzyka zachorowania na poszczeg�lne choroby, zidentyfikowanie oporno�ci na niekt�re leki (wa�ne przy planowaniu skutecznego leczenia) itp. 

Nawiasem m�wi�c, koszt d�ugotrwa�ego przechowywania danych sekwencyjnych bywa na tyle du�y, �e cz�sto bardziej op�aca si� zachowa� pr�bk� DNA i w razie potrzeby ponownie przeprowadzi� sekwencjonowanie  To kolejny wa�ny aspekt zwi�zany z �er� danych�, kt�ry, jako wykraczaj�cy poza tematyk� artyku�u, pomin� w dalszych rozwa�aniach.
Du�a ilo�� gromadzonych danych nie jest domen� jedynie biologii. Mamy obrazy medyczne, dane meteorologiczne, dane gospodarcze, dane o ruchu w sieci i szereg innych. I podobnie � bazuj�c na tych pozornie bezu�ytecznych surowych danych, chcemy wyci�gn�� konkretne, praktyczne wnioski.

Zastosowania algorytm�w uczenia maszynowego widzimy na co dzie�. Kto z nas wpisuj�c has�o do popularnej wyszukiwarki nie zwr�ci� uwagi na pojawiaj�ce si� sugestie? Mamy podpowiedzi w pasku przegl�darki, po witrynach oprowadzaj� nas wirtualni asystenci, w pisaniu tekst�w pomaga autokorekta, porz�dek w poczcie zapewniaj� wykrywacze spamu, dostajemy propozycje artyku��w podobnych do aktualnie czytanego, sugestie podobnych tematycznie film�w, wyselekcjonowane reklamy. Uczenie maszynowe pozwala na stworzenie szybkich i wiarygodnych prognoz pogody, wspomaga ocen� zdolno�ci kredytowej, prognozy ekonomiczne, obecne jest w nawigacji samochodowej, grach komputerowych. Do bardziej zaawansowanych problem�w nale�� rozpoznawanie mowy, pisma odr�cznego, interpretacja obraz�w medycznych i wiele, wiele innych.

Uczenie maszynowe rozumiemy jako zdolno�� programu do uczenia si�, do generalizacji. Algorytm konstruuje si� zwykle w ten spos�b, �e uruchamia si� program na niewielkim wycinku dost�pnych danych, na podstawie kt�rych dokonuje on parametryzacji, czyli inaczej m�wi�c � uczy si�. Je�eli uczenie przebieg�o pomy�lnie, w�wczas program b�dzie w stanie podj�� w�a�ciw� decyzj� nawet, je�eli oka�emy mu dane, z kt�rymi nigdy wcze�niej nie mia� do czynienia.
Istot� problem�w kt�re rozwi�zujemy metodami uczenia maszynowego s� klasyfikacja oraz predykcja. Nie jest moim celem om�wienie tutaj konkretnych technik, do kt�rych zaliczy� mo�emy m.in. sztuczne sieci neuronowe (ANN, *artificial neural networks*) b�d�ce (mocno uproszczon�) imitacj� procesu uczenia zachodz�cego w m�zgu, maszyny wektor�w no�nych (SVM, *support vector machines*), kt�rych idea polega na optymalizacji granicy decyzyjnej, ukryte modele markowa (HMM, *hidden markov models*) maj�ce zastosowanie w analizie proces�w stochastycznych czy drzewa decyzyjne (DT, decision trees), kt�re dokonuj� klasyfikacji na podstawie odpowiednio wygenerowaniej struktury drzewiastej. W ostatnich latach furor� robi uczenie g��bokie (*deep learning*), kt�re jest swego rodzaju rozszerzeniem i udoskonaleniem troch� ju� odchodz�cej na boczny tor idei sieci neuronowych. W�r�d popularnych technik jest oczywiscie stary, ale jary algorytm k-�rednich i wiele, wiele innych. Czytelnik�w zainteresowanych g��bszym wyja�nieniem poszczeg�lnych algorytm�w odsy�am do jak�e bogatej literatury, np. [3].

##Najpopularniejsze biblioteki ML##

Inspiracj� do napisania tego artyku�u by�o dla mnie znalezione w sieci zestawienie 20 bibliotek ML dla Pythona [6] uporz�dkowanych wed�ug do�� oryginalnego kryterium popularno�ci � wyra�a�o si� ono liczb� commit�w na githubie oraz os�b bior�cych udzia� w tworzeniu biblioteki (contributors). Liczba dost�pnych bibliotek jest jednak znacznie wi�ksza. Joseph Misiti w swoim repozytorium zgromadzi� zestawienie listuj�ce grubo ponad 150 r�nych bibliotek dla Pythona, kt�re w jakim� stopniu s� wykorzystywane w uczeniu maszynowym [5].*
Niew�tpliwie najpopularniejsz� bibliotek� oraz de facto standardem jest **scikit-learn* (https://github.com/scikit-learn/scikit-learn) . Biblioteka ta, oparta na popularnych pakietach numerycznych i naukowych, NumPy oraz SciPy cieszy si� te� du�ym wsparciem spo�eczno�ci. Jest bibliotek� og�lnego zastosowania � zawiera wiele modu��w implementuj�cych r�ne algorytmy oraz techniki ML. Biblioteka jest bardzo �atwa w u�yciu i wydajna. Jednak za t� �atwo�� i mnogo�� zastosowa� p�aci si� elastyczno�ci�. Trudno w scikit-learn zmodyfikowa� szczeg�owe parametry algorytmu, dopasowuj�c go do konkretnego problemu. Dlatego, gdy chcemy wykonywaa� operacje bardziej niskopoziomowe, warto si�gn�� po dedykowan�, bardziej elastyczn� bibliotek�, jak np. **PyBrain** (https://github.com/pybrain/pybrain), pozwalaj�c� skonstruowa� praktycznie dowoln� sie� neuronow�, modyfikuj�c np. funkcje aktywacji itp. PyBrain r�wnie� wykorzystuje SciPy.

Istniej� te� biblioteki, kt�re rozszerzaj� funkcjonalno�� pakietu scikit-learn, np. **Nilearn** (https://github.com/nilearn/nilearn), zawieraj�ca funkcje szczeg�lnie przydatne w analizie obraz�w aktywno�ci m�zgu.

Poniewa� metody uczenia maszynowego wymagaj� zwykle oblicze� na macierzach i innych z�o�onych strukturach matematycznych, wiele bibliotek bazuje na specjalistycznych bibliotekach numerycznych. Wspomniany wy�ej scikit-learn wymaga SciPy i NumPy. Inn� bibliotek� implementuj�c� zaawansowane obliczenia numeryczne jest **Theano** (https://github.com/Theano/Theano). Theano mo�e r�wnie� by� samodzielnie wykorzystywana do ML, szczeg�lnie w implementacji sieci neuronowych oraz uczenia g��bokiego. Theano implementuje r�wnie� rozwi�zania pozwalaj�ce efektywnie wykonywa� obliczenia na procesorach graficznych (GPU). 

W�r�d bibliotek bazuj�cych na Theano warto wskaza� **Pylearn2** (https://github.com/lisa-lab/pylearn2) oraz **Block** (https://github.com/mila-udem/blocks), **Keras** (https://github.com/fchollet/keras) i **Lasagne** *(https://github.com/Lasagne/Lasagne).

Ciekawym pakietem jest r�wnie� **Tensorflow** (https://github.com/tensorflow/tensorflow), stworzony w ramach projektu Google Brain. Implementuje wysokopoziomowy dost�p do sieci neuronowych. Do niew�tpliwych zalet zaliczy� tu nale�y obs�ug� oblicze� r�wnoleg�ych oraz na procesorach graficznych. Biblioteka napisana jest w wi�kszo�ci w C++, ale posiada niezb�dne wi�zania do Pythona.

W�r�d bibliotek naj�atwiej znajdziemy te wspieraj�ce sieci neuronowe czy uczenie g��bokie. Nie brakuje jednak te� modu��w pozwalaj�cych na u�ycie mniej popularnych metod, np. **Pyevolve** (https://github.com/perone/Pyevolve) jest przyk�adem biblioteki implementuj�cej algorytmy genetyczne. Z kolei **NuPIC** (https://github.com/numenta/nupic) implementuje metod� hierarchical temporal memory (HTM). Technika HTM architektur� przypomina sieci neuronowe, ma jednak inne pod�o�e biologiczne i zasad� dzia�ania.

**Nltk** (http://www.nltk.org/) jest bibliotek� dedykowan� dla problem�w przetwarzania j�zyka naturalnego.

Bibliotek� og�lnego przeznaczenia, bez zale�no�ci od SciPy i Theano jest **Pattern** (https://github.com/clips/pattern), dedykowana w szczeg�lno�ci do eksploracji witryn internetowych. Wspomnie� nale�y r�wnie� biblioteki **H2O** (https://github.com/h2oai/h2o-3)  i **caffe** (https://github.com/BVLC/caffe).

Zwie�czeniem tej niezwykle skr�towej prezentacji niech b�dzie **fuel** (https://github.com/mila-udem/fuel), biblioteka zapewniaj�ca �atwy dost�p do popularnych zbior�w danych takich jak MNIST (baza danych pisma odr�cznego). CIFAR-10 (baza obraz�w) czy Google's One Billion Words (beza tekstowa). Z kolei **Python Machine Learning Samples** (https://github.com/awslabs/machine-learning-samples) zawiera zbi�r przyk�adowych aplikacji wykorzystuj�cych ML.
 
Tabela 1. Wybrane biblioteki ML dla pythona uporz�dkowane wg liczby wsp�autor�w (contributors) [dane liczbowe wg stanu z 31.08.2016].
|    Biblioteka                  |    commits    |    contributors    |    github                                                 |
|--------------------------------|---------------|--------------------|-----------------------------------------------------------|
|    scikit-learn                |    21148      |    661             |    https://github.com/scikit-learn/scikit-learn           |
|    tensorflow                  |    7339       |    372             |    https://github.com/tensorflow/tensorflow               |
|    Theano                      |    23286      |    250             |    https://github.com/Theano/Theano                       |
|    keras                       |    2592       |    250             |    https://github.com/fchollet/keras                      |
|    caffe                       |    3766       |    208             |    https://github.com/BVLC/caffe                          |
|    pylearn2                    |    7100       |    116             | https://github.com/lisa-lab/pylearn2                      |
|    NuPIC                       |    5986       |    73              | https://github.com/numenta/nupic                          |
|    H2O                         |    19092      |    62              | https://github.com/h2oai/h2o-3                            |
|    lasagne                     |    1050       |    51              |    https://github.com/Lasagne/Lasagne                     |
|    blocks                      |    3175       |    48              |    https://github.com/mila-udem/blocks                    |
|    nilearn                     |    5145       |    45              |    https://github.com/nilearn/nilearn                     |
|    pybrain                     |    984        |    31              | https://github.com/pybrain/pybrain                        |
|    fuel                        |    1035       |    28              |    https://github.com/mila-udem/fuel                      |
|    pattern                     |    943        |    20              | https://github.com/clips/pattern                          |
|    fann                        |    156        |    19              |    https://github.com/libfann/fann                        |
|    machine-learning-samples    |    29         |    13              |    https://github.com/awslabs/machine-learning-samples    |
|    Pyevolve                    |    168        |    12              |    https://github.com/perone/Pyevolve                     |


##Bibliografia##

1.	Britz D., Implementing a Neural Network from Scratch in Python � An Introduction, http://www.wildml.com/2015/09/implementing-a-neural-network-from-scratch/
2.	G�recki P., Uczenie maszynowe, sztuczna inteligencja i (samo)�wiadomo��, 2014,  http://www.tabletowo.pl/2014/11/23/uczenie-maszynowe-sztuczna-inteligencja-i-samoswiadomosc/
3.	Holehouse AS., Stanford Machine Learning , http://www.holehouse.org/mlclass/
4.	Mayo M., 7 Steps to Mastering Machine Learning With Python, 2015, http://www.kdnuggets.com/2015/11/seven-steps-machine-learning-python.html
5.	Misiti J., Awesome Machine Learning, https://github.com/josephmisiti/awesome-machine-learning#python-cv
6.	Peddibhotla G.B., Top 20 Python Machine Learning Open Source Projects, 2015, http://www.kdnuggets.com/2015/06/top-20-python-machine-learning-open-source-projects.html
7.	Python Tools for Machine Learning, 2014, https://www.cbinsights.com/blog/python-tools-machine-learning/ 
8.	Robinson S., The Best Machine Learning Libraries in Python, 2015, http://stackabuse.com/the-best-machine-learning-libraries-in-python/ 
9.	Rosebrock A., My Top 9 Favorite Python Deep Learning Libraries, 2016, https://www.pyimagesearch.com/2016/06/27/my-top-9-favorite-python-deep-learning-libraries/ 
10.	Scikit-learn. Machine Learning in Python, http://scikit-learn.org/
