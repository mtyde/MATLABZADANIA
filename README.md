MATLABZADANIA
=============
%zad.1 Opór

R1=input('podaj opór R1=')
R2=input('podaj opór R2=')
R3=input('podaj opór R3=')
R=1/(1/R1+1/R2+1/R3)

%zad.2 Fahrenheit na Celsius

ftemp=input('Podaj temperaturę w Fahrenheitach ftemp=')
F=ftemp
C=(F-32)*(5/9)
ctemp=C

%zad.3 wspolrzedne kartezjańskie

disp('wspolrzedne biegunowe')
r=input('Podaj wartość r:')
phi=input('Podaj wartość phi:')

disp('wspolrzedne kartezjanskie') 
x=r*cos(phi)
y=r*sin(phi)


%zad.4 pierwiastek potęga tangens

x1=sqrt(17)
x2=3^1.3
x3=tan(pi)

clear
clf
x1=[-5:0.1:5];
y1=sqrt(x1);
x2=[-5:0.1:5];
y2=3.^x2;
x3=[-5:0.1:5];
y3=tan(x3);
plot(x1,y1,x2,y2,x3,y3);
title('Wykresy funkcji');
xlabel('X');
ylabel('Y');
axis([-5 5 -5 5])
grid;

%zad.5 liczby losowe

clc
disp('Rzeczywista liczba losowa z przedziału (0,1)')
rand
disp('Rzeczywista liczba losowa z przedziału (0,20)')
rand*20
disp('Rzeczywista liczba losowa z przedziału (20,50)')
((50-20)*rand)+20
disp('Całkowita liczba losowa z przedziału (0,10)')
randi(10,1)
disp('Całkowita liczba losowa z przedziału (0,11)')
randi(11,1)
disp('Całkowita liczba losowa z przedziału (50,100)')
randi([20,50],1)

%zad.6 wektory

clc
disp('Utwórz wektor 3 4 5 6')
a=[3:1:6]
disp('Utwórz wektor 1.0000 1.5000 2.0000 2.5000 3.0000')
b=[1:0.5:3]
disp('Utwórz wektor 5 4 3 2')
c=[5:-1:2]


%zad.7 operacje na macierzy

clc
disp('Generuję żądaną macierz')
A=[7:1:10;12:-2:6]
disp('Element w pierwszym wiersza i trzeciej kolumny')
A(1,3)
disp('Wszystkie elementy drugiego wiersza')
A(2,:)
disp('Pierwsze dwie kolumny')
A(:,1:2)


%zad.8 macierz zeros

clc
disp('Utworzenie macierzy a')
a=zeros(4,2)
disp('Przypisanie macierzy do zmiennej x')
x=a
disp('Zastąpienie drugiego wiersza przez 3 i 6')
x(2,1)=3
x(2,2)=6


%zad.9 równoodległe punkty

x=linspace(-pi, pi, 21)
y=power(x,2)-4*x+3

plot(x,y,'ro');
title('Wykres funkcji');
xlabel('oś x');
ylabel('oś y');
grid;



%zad.10 usuwanie wiersza macierzy losowej

clc
disp('Losowa macierz (3x5)')
A=rand(3,5)
disp('Usunięcie wiersza trzeciego')
A(3,:)=[]



%zad.11 obliczanie obj wydrążonej kuli

clc

rz=input('Podaj promień zewnętrzny kuli rz=')
rw=input('Podaj promień wewnętrzny kuli rw=')
disp('Objętość wydrążonej kuli wynosi')
V=((4*pi)/3)*(rz^3-rw^3)


%zad.12 niebieskie punkty +

clc

hold on
for i=1:10
    x=rand();
    y=rand();
    title('Niebieskie punkty +');
    xlabel('oś x');
    ylabel('oś y');
    plot(x,y,'+','MarkerFaceColor','b')
end
hold off


%zad.13 wykres funkcji plot i bar
clc

x=[0:5:100]
y=exp(-power(x,2))
%y1=exp(-x.^2)
figure(1)
plot(x,y);
 title('Wykres przy użyciu funkcji plot');
    xlabel('x');
    ylabel('y');


figure(2)
bar(x,y);    
title('Wykres przy użyciu funkcji bar');
    xlabel('x');
    ylabel('y');



 %zad.14 10 i 100 punktów z zakresu od 0 do pi
 
 clc
 
 x=linspace(0,pi,10)
 y=(power(2,x)-(2*x-x.^2))
  
 x1=linspace(0,pi)
 y1=(power(2,x1)-(2*x1-x1.^2))
 
 figure(1)
 plot(x,y,'o');
 title('10 punktów z zakresu od 0 do pi');
    xlabel('x');
    ylabel('y');
 
 figure(2)
 plot(x1,y1,'o');
 title('100 punktów z zakresu od 0 do pi');
    xlabel('x');
    ylabel('y');


%zad.15 oblicz pole prostokąta

Najpierw trzeba otworzyć File>New.Function
Następnie wpisujemy treść:

function [P] = obliczpoleprost(a,b)
a=input('Podaj wartość a= ')
b=input('Podaj wartość b= ')

disp('Pole prostokąta obliczone za pomocą funkcji obliczpoleprost wynosi')

wynik=a*b

end

Potem w Command Window wywołujemy funkcję

>> obliczpoleprost
Podaj wartość a= 1

a =

     1

Podaj wartość b= 2

b =

     2

Pole prostokąta obliczone za pomocą funkcji obliczpoleprost wynosi

wynik =

     2


%zad.16 hipsin

Najpierw trzeba otworzyć File>New.Function
Następnie wpisujemy treść:

function [hipersinus] = hipsin(x)

x=input('Podaj wartość x=')
disp('Warość sinusa hiperbolicznego dla podanej warotści x wynosi')
sinh(x)=(exp(1).^x-exp(1).^-x)/2

end

Potem w Command Window wywołujemy funkcję

>> hipsin
Podaj wartość x=1

x =

     1

Warość sinusa hiperbolicznego dla podanej warotści x wynosi

sinh =

    1.1752



%zad.17 suma pieniedzy

Najpierw trzeba otworzyć File>New.Function
Następnie wpisujemy treść:

%function[Tn]=sumapieniedzy(P,r,n)
function[Sp]=sumapieniedzy(P,r,n)
P=input('Podaj kapital poczatkowy P= ');
while P<=0
    disp('Wartosc musi być większa od zera')
    P=input('Podaj kapital poczatkowy P= ')
    
end
    r=input('Podaj oprocentowaie r= ');
while r<=0
    disp('Wartosc musi być większa od zera')
    r=input('Podaj oprocentowanie r= ')
end

    n=input('Podaj okres w latach n= ');
while n<=0
    
    disp('Wartosc musi być większa od zera')
    n=input('Podaj okres w latach n= ')
    
end

disp('      ')
disp('Odłożona suma pieniędzy wynosi')

Tn=P*(1+r)^n
end


Potem w Command Window wywołujemy funkcję

>> sumapieniedzy
Podaj kapital poczatkowy P= 1000
Podaj oprocentowaie r= 0.5
Podaj okres w latach n= 10
      
Odłożona suma pieniędzy wynosi

Tn =

        57665
