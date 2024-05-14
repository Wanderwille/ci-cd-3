# Домашнее задание к занятию 9 «Процессы CI/CD» - Подус Сергей

## Знакомоство с SonarQube

### Основная часть

1. Создайте новый проект, название произвольное.
2. Скачайте пакет sonar-scanner, который вам предлагает скачать SonarQube.
3. Сделайте так, чтобы binary был доступен через вызов в shell (или поменяйте переменную PATH, или любой другой, удобный вам способ).
4. Проверьте `sonar-scanner --version`.
5. Запустите анализатор против кода из директории [example](./example) с дополнительным ключом `-Dsonar.coverage.exclusions=fail.py`.
6. Посмотрите результат в интерфейсе.
7. Исправьте ошибки, которые он выявил, включая warnings.
8. Запустите анализатор повторно — проверьте, что QG пройдены успешно.
9. Сделайте скриншот успешного прохождения анализа, приложите к решению ДЗ.

## Знакомство с Nexus

### Основная часть

1. В репозиторий `maven-public` загрузите артефакт с GAV-параметрами:

 *    groupId: netology;
 *    artifactId: java;
 *    version: 8_282;
 *    classifier: distrib;
 *    type: tar.gz.
   
2. В него же загрузите такой же артефакт, но с version: 8_102.
3. Проверьте, что все файлы загрузились успешно.
4. В ответе пришлите файл `maven-metadata.xml` для этого артефекта.


### Знакомство с Maven

### Подготовка к выполнению

1. Скачайте дистрибутив с [maven](https://maven.apache.org/download.cgi).
2. Разархивируйте, сделайте так, чтобы binary был доступен через вызов в shell (или поменяйте переменную PATH, или любой другой, удобный вам способ).
3. Удалите из `apache-maven-<version>/conf/settings.xml` упоминание о правиле, отвергающем HTTP- соединение — раздел mirrors —> id: my-repository-http-unblocker.
4. Проверьте `mvn --version`.
5. Заберите директорию [mvn](./mvn) с pom.

### Основная часть

1. Поменяйте в `pom.xml` блок с зависимостями под ваш артефакт из первого пункта задания для Nexus (java с версией 8_282).
2. Запустите команду `mvn package` в директории с `pom.xml`, ожидайте успешного окончания.
3. Проверьте директорию `~/.m2/repository/`, найдите ваш артефакт.
4. В ответе пришлите исправленный файл `pom.xml`.


## Ответ:

## Знакомоство с SonarQube

1. Создал проект с названием Test-project

![Скриншот 1](https://github.com/Wanderwille/scrinshot/blob/main/Project.png)

4. 

![Скриншот 2](https://github.com/Wanderwille/scrinshot/blob/main/scaner.png)

6. Результат: 2 ошибки BUG и 1 Code Smell

![Скриншот 3](https://github.com/Wanderwille/scrinshot/blob/main/test%20code.png)

9. Скриншот исправленных 3-ех ошибок

![Скриншот 4](https://github.com/Wanderwille/scrinshot/blob/main/clear.png)

## Знакомство с Nexus

3. 

![Скриншот 5](https://github.com/Wanderwille/scrinshot/blob/main/arts%20meven.png)

4. Файл xml

Ссылка: https://github.com/Wanderwille/file/blob/main/maven-metadata.xml


### Знакомство с Maven

4. Версия meven

![Скриншот 6](https://github.com/Wanderwille/scrinshot/blob/main/meven.png)

### Основная часть

3. Скачанный артефакт

![Скриншот 7](https://github.com/Wanderwille/scrinshot/blob/main/repo.png)

4. Файл pom.xml: https://github.com/Wanderwille/file/blob/main/pom.xml


