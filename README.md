public class Test {
    public static void main(String[]args){
        MyThread myThread=new MyThread();
        myThread.start();
        for(int i=0;i<10;i++){
            System.out.println("ok");
            try{
                Thread.sleep(100);

            }catch(InterruptedException e){
                e.printStackTrace();

            }
        }
    }
}
class MyThread extends Thread{
    @Override
    public void run(){
        for(int m=0;m<10;m++){
            System.out.println(m);
            try{
                Thread.sleep(100);

            }catch(InterruptedException e){
                e.printStackTrace();

            }
        }
    }
}
