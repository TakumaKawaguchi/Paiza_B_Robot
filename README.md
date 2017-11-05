import java.util.*;


public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int sx= sc.nextInt();
        int sy= sc.nextInt();
        
        int mf= sc.nextInt();
        int mr= sc.nextInt();
        int mb= sc.nextInt();
        int ml= sc.nextInt();
        int mno= sc.nextInt();
        int d=4;
        
        for(int i=0;i<=mno;i++){
            String temp=sc.nextLine();
            String t[]= temp.split(" ");
            if(i!=0){
                //System.out.println(t[0]);
        
            String mt= t[0];
            String md= t[1];
                    
            if(mt.equals("m")){
                if(d==0 || d==4){
                    if(md.equals("F")){
                        sy=sy+mf;
                    }
                    if(md.equals("B")){
                        sy=sy-mb;
                    }
                    if(md.equals("L")){
                        sx=sx-ml;
                    }                
                    if(md.equals("R")){
                        sx=sx+mr;
                    }
                }
                if(d==1){
                    if(md.equals("F")){
                        sx=sx+mf;
                    }
                    if(md.equals("B")){
                        sx=sx-mb;
                    }
                    if(md.equals("L")){
                        sy=sy+ml;
                    }                
                    if(md.equals("R")){
                        sy=sy-mr;
                    }
                }                
                if(d==2){
                    if(md.equals("F")){
                        sy=sy-mf;
                    }
                    if(md.equals("B")){
                        sy=sy+mb;
                    }
                    if(md.equals("L")){
                        sx=sx+ml;
                    }                
                    if(md.equals("R")){
                        sx=sx-mr;
                    }
                }                
                if(d==3){
                    if(md.equals("F")){
                        sx=sx-mf;
                    }
                    if(md.equals("B")){
                        sx=sx+mb;
                    }
                    if(md.equals("L")){
                        sy=sy-ml;
                    }                
                    if(md.equals("R")){
                        sy=sy+mr;
                    }
                }         
             
      
            }
            else{
                if(md.equals("B")){
                    d=d+2;
                  
                }
                if(md.equals("L")){
                    d--;
                }                
                if(md.equals("R")){
                    d++;
                }    
          
                d=d%4;
            }
            }
         
        }
        System.out.println(sx+" "+sy);
    
    }
}
