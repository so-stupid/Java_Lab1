# Лабораторная работа №1 

## План
## 1) Создать структуру:
```
mkdir src
mkdir classes
cd src
mkdir mypackage
cd ..
```
## 2) Создать main класс
```
package mypackage;

    public class HelloWorld{
    
        public static void main(String args[]){
            System.out.println("Hello, World!");
        }
    }	
```

## 3) Скомпилировать классы
```
javac -classpath ./classes -d ./classes src/mypackage/HelloWorld.java
```

4) Выполнить программу
```
 java -classpath ./classes mypackage.HelloWorld

```
5) Упаковка в Jar
Сознание манифеста:
```
    Manifest-Version: 1.0
    Created-By: 1.6.0_19 (Sun Microsystems Inc.)
    Main-Class: mypackage.HelloWorld
```

Упаковка:
```
 jar cvmf manifest.mf helloWorld.jar -C ./classes mypackage
```

Выполнение: 
```
java -jar helloWorld.jar
```
