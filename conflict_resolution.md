# Conflict Шийдвэрлэлт

## Conflict-ийн Дэлгэрэнгүй

`feature/add-multiply-validation`-ийг `develop` руу нэгтгэхэд `src/main/java/lab14/sict/must/edu/mn/Multiplication.java` дээр merge conflict гарсан. Conflict нь `multiply` функцын Javadoc коммент дээр байсан.

## Шийдвэрлэлтийн Алхмууд

1. Онцлогын салбарт `git merge develop` ажиллуулсан.
2. `Multiplication.java` дээрх conflict-ийг тодорхойлсон.
3. Файлыг засварлаж, хоёр салбарын Javadoc комментийг нэгтгэсэн.
4. `git add src/main/java/lab14/sict/must/edu/mn/Multiplication.java` ажиллуулсан.
5. `git commit` ажиллуулж merge-ийг дуусгасан.
6. Салбарыг push хийж, PR үүсгэсэн.

## Хэрэглэсэн Git Командууд

```bash
# Develop салбарыг feature салбарт merge хийх
git checkout feature/add-multiply-validation
git merge develop

# Conflict-ийг засварласны дараа
git add src/main/java/lab14/sict/must/edu/mn/Multiplication.java
git commit -m "Merge conflict шийдвэрлэх: Multiplication.java дээрх Javadoc нэгтгэх"

# Remote руу push хийх
git push origin feature/add-multiply-validation
```

## Шийдэгдсэн Өөрчлөлт

Хоёр салбарын Javadoc комментийг нэгтгэж, хоёр талын мэдээллийг агуулсан шинэ Javadoc коммент үүсгэсэн. CI шалгалт (Checkstyle, 100% coverage) амжилттай болж, PR merge хийгдсэн.
