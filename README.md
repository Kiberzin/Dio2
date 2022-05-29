package Dio;

public class Ex {

    public class SingletonLazy {

        private static SingletonLazy instancia;

        private SingletonLazy() {
            super();
        }

        public static SingletonLazy getInstancia() {
          if (instancia == null) {
              instancia = new SingletonLazy();
          }
            return instancia;
        }
    }
}

=========================================================================================================================================================================

package Dio;

public class Ex2 {
    public class SingletonEager {

        private static SingletonEager instancia = new SingletonEager();

        private SingletonEager() {
            super();
        }

        public static SingletonEager getInstancia() {

            return instancia;
        }
    }
}

=========================================================================================================================================================================

package Dio;

public class Ex3 {

    public class SingletonLazyHolder {


        private static class Holder {
            private static SingletonLazyHolder instancia = new SingletonLazyHolder();
        }
        private SingletonLazyHolder() {
            super();
        }

        public static SingletonLazyHolder getInstancia() {
            return instancia;
        }
    }
}

=========================================================================================================================================================================

package Dio;

public class Test {
   SingletonLazy lazy = Ex.SingletonLazy.getInstancia();
   System.out.print(lazy);

}

