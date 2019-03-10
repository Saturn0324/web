import java.util.Vector;

public class Main {

    public static void main(String[] args) {
        Vector<Vector<Integer>> board = new Vector<>();
        for(int i=0;i<10;i++) {
            Vector<Integer> vec=new Vector<>(10);
            for(int j=0;j<10;j++){
                vec.add(j,1);
            }
            board.add(i,vec);
        }
        Vector<Vector<Integer>> new_board = game_of_life(board);
        for (int i = 0; i < new_board.size(); i++) {
            for(int j=0;j<new_board.get(i).size();j++)
            {
                System.out.println(new_board.get(i).get(j)+" ");
            }
            System.out.println("\n");
        }
    }
    public static Vector<Vector<Integer>> game_of_life(Vector<Vector<Integer>> board){
        int a=board.size();
        int b=board.get(0).size();
        int[][] arr = new int[a][b];
        for(int i=0;i<a;i++)
        {
            for(int j=0;j<b;j++)
            {
                int num=0;
                for(int m=i-1;m<=i+1;m++)
                {
                    for(int n=j-1;n<=j+1;n++)
                    {
                        if(m<0||n<0||m>=a||n>=b) continue;;
                        if(board.get(m).get(n)!=0) num++;
                    }
                }
                if(board.get(i).get(j)!=0) num--;
                switch (num){
                    case 0:
                    case 1:
                    case 4:
                    case 5:
                    case 6:
                    case 7:
                    case 8:
                        arr[i][j]=0;
                    case 3:
                        arr[i][j]=1;
                    case 2:
                        arr[i][j]=board.get(i).get(j);break;
                }
            }
        }
        for(int i=0;i<a;i++)
        {
            Vector<Integer> temp=new Vector<>(b);
            for(int j=0;j<b;j++)
            {
                temp.add(j,arr[i][j]);
            }
            board.add(i,temp);
        }
        return board;

    }
}
