# ArrayPesos
Le damos un numero y el nos devuelve un array con multiplos de 3
package PackOne;

import java.util.ArrayList;
import java.util.List;

public class GetPesos {

    public static void main(String[] args) {
        List output = getRequire(1000);
        System.out.println(output);
    }

    private static List<Integer> getRequire(int max) {
        List<Integer> lista = new ArrayList<>();
        int sum = 0, i, k = 0, j = 0;
        if(max == 0){lista = null; return lista;}
        
        para:
        for (i = 1; i <= max; j = i *= 3) {
            if ((j * 3) > max && (max - (j + k)) < 0) {
                break para;
            }
            if (i < max) {
                lista.add(i);
                k += i;
            }
        }
        sum = max - k;
        if (sum == 0) {
        } else {
            lista.add(sum);
        }

        return lista;
    }
}

