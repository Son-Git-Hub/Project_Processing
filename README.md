# Project_Processing
int x=240, y=240, z=240; //가속도, 마찰, 일반 속도를 위해 변수 3개지정

 

float velocity_x=1, velocity_y=15, velocity_z=5;  // 발사하는 속도

float accel_x= 2; //가속도

float friction = 0.98; //마찰율

 

void setup() {

  size(900, 900);

  background(255);

}

 

void draw() {

 

//가속도 공룡 코드 (핑크색)

fill(255,0,255);

beginShape();

vertex(50,200);

vertex(100,150);

vertex(120,100);

vertex(60,20);

vertex(250,80);

vertex(210,110);

vertex(250,150);

vertex(170,170);

vertex(150,200);

vertex(50,200);

endShape();

 

//가속도 공룡 눈 추가

fill(200,0,150);

ellipse(210,85,20,20);

 

//가속도가 붙는 불 추가

fill(255,0,0);

ellipse(x,110,30,30);

velocity_x += accel_x;

x +=velocity_x;

 

//마찰 공룡 추가 (노란색)

fill(255,255,0);

beginShape();

vertex(50,500);

vertex(100,450);

vertex(120,400);

vertex(60,320);

vertex(250,380);

vertex(210,410);

vertex(250,450);

vertex(170,470);

vertex(150,500);

vertex(50,500);

endShape();

 

//마찰 공룡 눈 추가

fill(0,200,255);

ellipse(210,385,20,20);

 

//마찰 하는 불 추가

fill(255,0,0);

ellipse(y,410,30,30);

velocity_y *=friction;

y+= velocity_y;

 

//일반 속도 공룡 추가 (파란색)

fill(0,255,255);

beginShape();

vertex(50,800);

vertex(100,750);

vertex(120,700);

vertex(60,620);

vertex(250,680);

vertex(210,710);

vertex(250,750);

vertex(170,770);

vertex(150,800);

vertex(50,800);

endShape();

 

// 일반 공룡 눈 추가

fill(0,0,255);

ellipse(210,685,20,20);

 

//일반적인 불 추가

fill(255,0,0);

ellipse(z,710,30,30);

z+=velocity_z;

 

//문구 출력

 

fill(255,0,0); //글자 색상 조정

textSize(100); //글자 크기 조정

text("FIRE!!",400,850); //500,900 좌표에 문자 출력

}
