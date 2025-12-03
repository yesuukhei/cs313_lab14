# Calculator - Maven Java Project

Энэхүү төсөл нь Maven-д суурилсан энгийн тооцоолуурын Java аппликейшн юм.

## Төслийн Бүтэц

- **Package**: `lab14.sict.must.edu.mn`
- **Main Source**: `src/main/java/lab14/sict/must/edu/mn/`
- **Test Source**: `src/test/java/lab14/sict/must/edu/mn/`

## Шаардлага

- Java 17
- Maven 3.6+

## Хэрхэн Угсрах

### Бүх тест ажиллуулах
```bash
mvn test
```

### Checkstyle код загварын шалгалт
```bash
mvn checkstyle:check
```

### JaCoCo Code Coverage тайлан үүсгэх
```bash
mvn jacoco:report
```

Coverage тайлан нь `target/site/jacoco/index.html` файлд үүснэ.

### Бүх шалгалт (Checkstyle, Test, Coverage) нэгэн зэрэг
```bash
mvn clean test checkstyle:check jacoco:report
```

## Төсөл Ажиллуулах

Төсөл нь JUnit тестүүд агуулсан бөгөөд `mvn test` командаар ажиллуулна.

## CI/CD

GitHub Actions ашиглан автомат CI процесс тохируулагдсан:
- Checkstyle код загварын шалгалт
- JUnit тестүүд
- JaCoCo 100% branch coverage шалгалт

CI процесс нь `develop` болон `release/*` салбарууд руу хийсэн push болон pull request дээр автоматаар ажиллана.

