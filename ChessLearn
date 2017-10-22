#include<iostream>
#include<math.h>
#include<stdlib.h>
#include<time.h>
#include<string>
#include<cstdlib>
#include<conio.h>

struct SCell{
           int Row;
           int Col;
  };
  
  char fPawn = 'i';
  char fRook = '#';
  char fKnight = '?';
  char fBishop = '!';
  char fQueen = 'Q';
  char fKing = 'K';
  char fEmpty = '_';
  
  
  
using namespace std;

bool Queen(SCell From, SCell To);

bool Pawn(SCell From, SCell To);

bool King(SCell From, SCell To);

bool Rook(SCell From, SCell To);

bool Bishop(SCell From, SCell To);

bool Knight(SCell From, SCell To);

void DisplayRes( bool Res);

const int R1 = 8;
const int R2 = 8;

void DisplayBoard( char Mass [ ] [ R2 ],int R1,  int R2);
void EraseBoard ( char Board [ ] [ R2 ], int R1, int R2);
void BeginBoard ( char Board [ ] [ R2 ], int R1, int R2);

int main()
{ 
srand(time (NULL));
  //  рандом от 1 до 9: rand()%10;
 
 char Board [ R1 ] [ R2 ] = {};
 cout << "Пустая шахматная доска:"<<endl;
 
 EraseBoard (Board, R1, R2);
 DisplayBoard (Board, R1, R2);
 
 int contin1;
cout<<"Продолжить....нажмите 1: ";
cin >> contin1;
if ( contin1 == 1) {
		clrscr();
 
 cout << "Шахматная доска с расставленными фигурами на Вашей стороне"<< endl;

 BeginBoard (Board, R1, R2);
 DisplayBoard (Board, R1, R2);
 
cout << "Изучите фигуры и решите какой хотите походить,"<<endl<<"чтобы это сделать надо записать начальную координату фигуры и конечную, например,"<< endl<<"? - конь, 2 1 - нач. коор., 3 3 - конеч. коор."<< endl;
cout<<"Нумерация ячеек от 1 до 8, начиная с левого нижнего угла"<<endl<<endl;


int contin2;
cout<<"Продолжить....нажмите 1: ";
cin >> contin2;
if ( contin2 == 1) {
      
      while ( true ) {
	bool Wrong;
			clrscr();
	DisplayBoard (Board, R1, R2);
	
	if ( Wrong ) cout << "Так ходить нельзя" << endl;
	Wrong = false;

SCell From, To, Input, Output;

cout<<"Откуда ходим - столбец: ";
cin >> Input.Col;
cout<<"Откуда ходим - ряд: ";
cin >> Input.Row;
cout<<"Куда ходим - столбец: ";
cin >> Output.Col;
cout<<"Куда ходим - ряд: ";
cin >> Output.Row;

From.Row = 8 - Input.Row;
From.Col = Input.Col - 1;
To.Row = 8 - Output.Row;
To.Col = Output.Col - 1;

char figure;  // фигура игрока
figure = Board [ From.Row ] [ From.Col ];

// ходит Ладья
	if ( figure == fRook )
	   {
	   		if ( Rook ( From, To )) {
 		 	Board [ From.Row ] [ From.Col ] = fEmpty;
 		 	Board [ To.Row ] [ To.Col ] = fRook;
 		 	}
 		 	else
 		 	Wrong = true;
	   }
	   
	   // ходит Слон
	else if ( figure == fBishop)
	{
			if ( Bishop ( From, To )) {
 		 	Board [ From.Row ] [ From.Col ] = fEmpty;
 		 	Board [ To.Row ] [ To.Col ] = fBishop;
 		 	}
 		 	else
 		 	Wrong = true;
	}
		
		 
	   // ходит Конь
	else if ( figure == fKnight)
	{
			if ( Knight ( From, To )) {
 		 	Board [ From.Row ] [ From.Col ] = fEmpty;
 		 	Board [ To.Row ] [ To.Col ] = fKnight;
 		 	}
 		 	else
 		 	Wrong = true;
	}
	
		 
	   // ходит Король
	else if ( figure == fKing)
	{
			if ( King ( From, To )) {
 		 	Board [ From.Row ] [ From.Col ] = fEmpty;
 		 	Board [ To.Row ] [ To.Col ] = fKing;
 		 	}
 		 	else
 		 	Wrong = true;
	}
	
	 
	   // ходит Ферзь
	else if ( figure == fQueen)
	{
			if ( Queen ( From, To )) {
 		 	Board [ From.Row ] [ From.Col ] = fEmpty;
 		 	Board [ To.Row ] [ To.Col ] = fQueen;
 		 	}
 		 	else
 		 	Wrong = true;
	}

 
	   // ходит Пешка
	else if ( figure == fPawn)
	{
			if ( Pawn ( From, To )) {
 		 	Board [ From.Row ] [ From.Col ] = fEmpty;
 		 	Board [ To.Row ] [ To.Col ] = fPawn;
 		 	}
 		 	else
 		 	Wrong = true;
	}


      }   // нужные
      }
}
/* 
 
 cout << "Программа покажет Вам на какие поля может ходить"<<endl <<"шахматная фигура, в зависимости от заданного Вами поля."<<endl <<"Поля нумеруются с левого нижнего угла от 1 до 8"<< endl<<endl;

while ( true ) {
	EraseBoard (Board, R1, R2);
cout << "Введите номер фигуры:"<<endl<<"1 - Король, 2 - Ферзь, 3 - Ладья,"<<endl<< "4 - Слон, 5 - Конь, 6 - Пешка"<<endl;

int Piece;
cin>> Piece;

SCell From, To, Input;

cout<<"Введите столбец (1..8): ";
cin >> Input.Col;

cout<<"Введите ряд (1..8): ";
cin >> Input.Row;

char F = 'F'; 
char X = 'X';

From.Row = 8 - Input.Row;
From.Col = Input.Col - 1;


switch ( Piece ) {
	
	case 3:  // Ладья 
	{
		for (int c1 = 0; c1 < R1; c1++){
 		 for ( int c2 = 0; c2 < R2; c2++){
 		 	To.Row = c1;
 		 	To.Col = c2;
 		 	if ( Rook ( From, To )) {
 		 	Board [ c1 ] [ c2  ] = X;
 		 	}
 		 }
	}
Board [ From.Row ] [ From.Col ] = F;
break;
	}
	
	case 4:  // Слон
	{
		for (int c1 = 0; c1 < R1; c1++){
 		 for ( int c2 = 0; c2 < R2; c2++){
 		 	To.Row = c1;
 		 	To.Col = c2;
 		 	if ( Bishop ( From, To )) {
 		 	Board [ c1 ] [ c2  ] = X;
 		 	}
 		 }
	}
Board [ From.Row ] [ From.Col ] = F;
break;
	}
		case 5:  // Конь
	{
		for (int c1 = 0; c1 < R1; c1++){
 		 for ( int c2 = 0; c2 < R2; c2++){
 		 	To.Row = c1;
 		 	To.Col = c2;
 		 	if ( Knight ( From, To )) {
 		 	Board [ c1 ] [ c2  ] = X;
 		 	}
 		 }
	}
Board [ From.Row ] [ From.Col ] = F;
break;
	}
	
		case 1:  // Король
	{
		for (int c1 = 0; c1 < R1; c1++){
 		 for ( int c2 = 0; c2 < R2; c2++){
 		 	To.Row = c1;
 		 	To.Col = c2;
 		 	if ( King ( From, To )) {
 		 	Board [ c1 ] [ c2  ] = X;
 		 	}
 		 }
	}
Board [ From.Row ] [ From.Col ] = F;
break;
	}
	
			case 2:  // Ферзь
	{
		for (int c1 = 0; c1 < R1; c1++){
 		 for ( int c2 = 0; c2 < R2; c2++){
 		 	To.Row = c1;
 		 	To.Col = c2;
 		 	if ( Queen ( From, To )) {
 		 	Board [ c1 ] [ c2  ] = X;
 		 	}
 		 }
	}
Board [ From.Row ] [ From.Col ] = F;
break;
	}
	
			case 6:   // Пешка
	{
		for (int c1 = 0; c1 < R1; c1++){
 		 for ( int c2 = 0; c2 < R2; c2++){
 		 	To.Row = c1;
 		 	To.Col = c2;
 		 	if ( Pawn ( From, To )) {
 		 	Board [ c1 ] [ c2  ] = X;
 		 	}
 		 }
	}
Board [ From.Row ] [ From.Col ] = F;
break;
	}
	
	default:
	break;	
};

 DisplayBoard (Board, R1, R2);
 //===== конец цикла while
}
*/

   return 0;
}
// ===== Конец ======

// Пользовательские функции
// Стереть доску
void EraseBoard ( char Board [ ] [ R2 ], int R1, int R2) {
for ( int c1 = 0; c1 < R1; c1++){
 		 for ( int c2 = 0; c2 < R2; c2++){
 		 	Board[ c1 ] [ c2 ] = fEmpty;
 		 }
 }
}


// Расставить фигуры
void BeginBoard ( char Board [ ] [ R2 ], int R1, int R2){
	
	 
 //-----Пешки
for (int c = 0 ; c < R2 ; c++){
	Board [ 6 ] [ c ] = fPawn;
}

//----- Ладьи
Board [ 7 ] [ 0 ] = fRook;
Board [ 7 ] [ 7 ] = fRook;

//----- Кони
Board [ 7 ] [ 1 ] = fKnight;
Board [ 7 ] [ 6 ] = fKnight;

//----- Слоны
Board [ 7 ] [ 2 ] = fBishop;
Board [ 7 ] [ 5 ] = fBishop;

//----- Король
Board [ 7 ] [ 4 ] = fKing;

//------Ферзь
Board [ 7 ] [ 3 ] = fQueen;

}

 // Вывод доски
 void DisplayBoard( char Mass [ ] [ R2 ], int R1, int R2) {
 	for (int c1 = 0; c1 < R1; c1++){
 		 for ( int c2 = 0; c2 < R2; c2++){
 		 	cout<< Mass [ c1 ] [ c2 ]<<" ";
 		 }
 		 cout<<endl;
 	} cout<<endl;
 }

//=== Король

bool King(SCell From, SCell To){
	
if ( abs( To.Row - From.Row) <= 1 & abs ( To.Col - From.Col) <= 1) return true;
else return false;

}

//=== Ферзь
bool Queen(SCell From, SCell To){
	
if ( ( (From.Col == To.Col || From.Row == To.Row ) ) || (abs( To.Row - From.Row) == abs ( To.Col - From.Col) ) )return true;
else return false;

}
//=== Ладья
bool Rook(SCell From, SCell To){
	
if ( From.Col == To.Col || From.Row == To.Row ) return true;
else return false;

}

//=== Слон 

bool Bishop(SCell From, SCell To){
	
if ( abs( To.Row - From.Row) == abs ( To.Col - From.Col) ) return true;
else return false;

}

//=== Конь

bool Knight(SCell From, SCell To){
	
if ( (abs( To.Row - From.Row) == 2 & abs ( To.Col - From.Col) == 1) ||  (abs( To.Row - From.Row) == 1 & abs ( To.Col - From.Col) == 2) ) return true;
else return false;

}

//=== Пешка

bool Pawn (SCell From, SCell To){
	
if ( (( To.Row - From.Row) == -1 &  To.Col == From.Col )|| (  ( To.Row - From.Row) == -2 &  From.Row == 6  & To.Col == From.Col )) return true;
else return false;

}


//=== Вывод сообщения

void DisplayRes( bool Res){
	
if ( Res ) cout << "Так можно ходить"<<endl;
else cout << "Так нельзя ходить"<<endl;

}