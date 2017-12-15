/* analog clock by Rabita chhantyal */

int xendsecond,yendsecond,xendminute,yendminute,xendhour,yendhour;

float theta;

void setup(){
 
 size(500,500);
 
 background(255,189,193);
 
 xendsecond=90;
 
  yendsecond=0;
  
  xendminute=70;
 
 yendminute=0;
  
  xendhour=40;
  
  yendhour=0;
  
  frameRate(1);
}

void draw(){
  
  background(255,189,193);
  
  translate(width/2,height/2);
  
  stroke(255,177,158);
  
  fill(color(#9FC3E6));
  
  strokeWeight(15);
  
  ellipse(0,0,200,200);
  
  strokeWeight(1.5);
  
  stroke(color(255,0,0));
  
  line(0,0,xendsecond,yendsecond);
  
  stroke(255,177,158);
  
  strokeWeight(2.5);
 
 stroke(color(#A86FBA));
 
 line(0,0,xendminute,yendminute);
 
 strokeWeight(4);
 
 stroke(color(#F76804));
 
 line(0,0,xendhour,yendhour);
 
  ellipse(0,0,10,10);
  
  fill(color(25,0,0));
 
 text("12",0,-100);
  
  text("6",0,100);
 
 text("9",-100,0);
  
  text("3",100,0);
 
 theta+=TWO_PI/60;
 
 xendsecond=int(90*cos(theta));
 
 yendsecond=int(90*sin(theta));
  
  xendminute=int(70*cos(theta/60));
  
  yendminute=int(70*sin(theta/60));
 
 xendhour=int(40*cos(theta/60/60-PI/2));

yendhour=int(40*sin(theta/60/60-PI/2));

}
