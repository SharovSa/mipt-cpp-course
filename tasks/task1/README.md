# Задача 1. Тайное становится явным
## Формулировка
Вы используете библиотеку `SomeLibrary` в которой есть следующий класс:
```
namespace SomeLibrary {
  class ValueHolder {
  public:
    ValueHolder(const std::string_view name, int value)
      : name_(name), value_(value)
    { }

    std::string GetName() const {
      return name_;
    }

    int GetValue() const {
      return value_;
    }
  private:
    std::string name_;
    int value_;
  };
}
```

Вам необходимо иметь возможность менять значение `value_` в ходе работы с объектами класса `ValueHolder`, при этом изменять исходный код библиотеки запрещено. Реализуйте функцию `SetValue`, которая будет решать поставленную задачу. Ваше решение должно быть кроссплатформенным, использовать `sizeof` запрещено.