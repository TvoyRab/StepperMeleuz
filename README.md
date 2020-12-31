# Stepper-Mel
The programm to stepper motor.
## Данный проект реализован для управления ходом шагового двигателя 
***Создатели проекта***: Zabirov Robert and Ismagilov Azamat
***Город***: Республика Башкортостан , город Мелеуз
***Дата***:31.12.2020
 
### Инструкция по применению библиотеки :
// установка шага
void setStep(int stepLength); 
stepLength-длина шага 
//   линейное перемещение и управление вращением
	void  moveStep(float dir,int pause,int moveCount); 
   dir-направления движения 
   pause-пауза
   moveCount-шаг
   
   
  // Управление ускорением движения мотора
	void moveAccStep(float dir,int pause,int moveCount);
      dir-направления движения 
   pause-пауза
   moveCount-шаг
   
   
  //Управление углом поворота вала шагового двигателя
	void  moveAngle(float speed,float angle, bool acc); 
   speed-скорость 
   angle-угол в грудусах
   acc-ускорение
   
   // Управление линейным перемещением в относительной и абсолютной системе координат
	void  moveVector(float speed,int _length, bool acc); 
    speed-скорость 
    _length-длина перемещения 
    acc-ускорение
    
    
   
   // Установка текущей позиции мотора
	void  movePosition(float speed,int newPos, bool acc); 
   speed-скорость 
   newPos-указание новой позиции 
   acc-ускорение
   // Возвращение домой 
	  void   moveHome();
   
   
   
  int PIN_STEP=3; // пин для генерации импульсов для движения двигателей (каждый импульс – шаг), можно регулировать скорость двигателя
  int PIN_DIR=2; // пин  для установка направления  вращения
  int PIN_MS1=4; // контакты для установки микрошага
  int PIN_MS2=5; // контакты для установки микрошага
  int PIN_MS3=6; // контакты для установки микрошага
  int pos=0;  // начальная позиция 
  int currentStep=0; // дробление
  int a=20; //ускорение 
  const int MS[5][3]={{0,0,0}, // дробление шага 
                      {1,0,0},
                      {0,0,1},
                      {1,0,1},
                      {1,1,1}};	
};	

#### GIT history
* v1.0
* v1.1 добавлена возможность управления движением и вращением 
* v1.2 добавлена возможность управлением углом поворота вала шагового двигателя
* v1.3 оптимизация выбора дробления шага
* v1.4 реализовано Управление линейным перемещением в относительной и абсолютной системе координат
* v1.5 добавлена возможность установки текущей позиции мотора 
* v1.6 исправлены ошибки и оптимизированы пункты , ранее описанные в `GIT history`
* v1.7 добавлена возможность управления ускорением движения мотора 


