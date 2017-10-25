/*Koi pond with fish amd lily pads 
 that move differently as they are clicked on */

void setup() {
  size(600, 600);
}

int koiW=80;
int koiH=40;
int KoiTail;
int padH;
int padW;
int eye;
int koiX1=55;
int koiY1=-20;
boolean checkMouse=false;

void draw() {
  background(#7BC4EA);
  eye=5;

  //draws a Koi fish
  fill(255, 0, 0);
  pushMatrix();
  translate(100, 100);
  noStroke();
  ellipse(koiX1, koiY1, koiW, koiH);
  triangle(koiX1-55, koiY1+20, koiX1-55, koiY1-20, koiX1, koiY1);
  fill(0);
  ellipse(koiX1+25, koiY1+10, eye, eye);
  ellipse(koiX1+25, koiY1-10, eye, eye);


  //draws a lily pad
  int padH= 150;
  int padW= 150;
  fill(#378169);
  ellipse(100, 100, padW, padH);

  //lily pad texture
  strokeWeight(5);
  stroke(#7BC4EA);
  line(100, 100, 175, 100);
  popMatrix();

  if ((mouseX<=135)&&(mouseX>=-35)&&(mouseY<=0)&&(mouseY>=-40)&&mousePressed==true)
    {koiX1=koiX1+1;
    checkMouse=true;}
    
  else if (checkMouse==true)
    koiX1=koiX1+1;
}
