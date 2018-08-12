float []x;
float []y;
float []a;
float []b;
float []p;
float []m;
int n=25;
int f=n;
int count=0;
int s;
PImage bg;

void setup()
{
  size(1080,1920);
  frameRate(60);
  background(0); 
  x=new float[n];
  y=new float[n];
  a=new float[n];
  b=new float[n];
  p=new float[n];
  m=new float[n];
  //bg=loadImage("imagebg.png");
  
 for(int i=0;i<n;i++)
  {
    p[i]=150;
    m[i]=150;
    x[i]=random(p[i],1080-p[i]);
    y[i]=random(m[i],1920-m[i]); 
    a[i]=random(-10,10);
    b[i]=random(-10,10);
    
    
  }
}   
 void draw()
{
  background(0);
  fill(20,10,255);
  stroke(0);
  strokeWeight(2);
  println(millis());
  for(int i=0;i<n;i++)
  {
    ellipse(x[i],y[i],p[i],m[i] );
    
    x[i]=x[i]+a[i];
    y[i]=y[i]+b[i];
    
    if(x[i]>width- p[i]/2 || x[i]< p[i]/2)
    {
     
      a[i]=-a[i];
    
    }
    if(y[i]>height- p[i]/2 || y[i]< p[i]/2)
    {
     
      b[i]=-b[i];
    
    }
  }
  textSize(30);
  fill(255,255,255);
 text("Score: "+ count,10,30);
 text("Balls remmaining"+f,10,60);
 s=30-millis()/1000;
 if(s>0 && f>0)
 {
  textSize(30);
  fill(255,255,255);
 text("Time Remmaining:"+s,10,90);
 }
 if(f==0 && s>0)
 {
   textSize(120);
   fill(0,255,0);
   text("You Won",300,700);
 }
 else if(f!=0 && s==0)
 {
   textSize(120);
   fill(225,0,0);
   text("Game Over",400,700);
 }
}
void mousePressed()
{
  for(int i=n-1;i>=0;i--)
  {
  float d = sqrt((x[i]-mouseX)* (x[i]-mouseX)+(y[i]-mouseY)*(y[i]-mouseY));
  if(d<= p[i]/2)
  {
    p[i]=0;
    m[i]=0;
    //int speedbonus= abs(int(a[i]+a[i]));
    //int timebonus=int(20000.0/millis())*2;
    count=count+10;//+speedbonus+timebonus;
    f--;
    break;
  }
  }
}