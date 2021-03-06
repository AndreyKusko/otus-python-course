# Репозиторий домашних заданий для OTUS
## Homework 1 - Log analyzer

#### Запуск  
```bash
python3 log_analyzer.py [--config path_to_config]  
```
Ожидается файл конфигурации в формате JSON, содержащий все или некоторые из следующих полей.  
```python
{
"REPORT_SIZE": INT,  
"LOG_DIR": PATH,  
"REPORT_DIR": PATH,  
"APP_LOG": PATH,  
"ERROR_LEVEL": FLOAT,  
}  
```
**REPORT_DIR** - Если не задан, то создается  
Если параметр **config** не передан будут использоваться встроенные конфигурации по умолчанию:  
```python
{
"REPORT_SIZE": 1000,  
"LOG_DIR": "/var/log/nginx",  
"REPORT_DIR": "./reports",  
"APP_LOG": None,  
"ERROR_LEVEL": 0.2,  
}  
```

#### Тестирование
Для программы написаны два юнит теста _test_functions.py_ и _test_app.py_. При их запуске  на основе сэмплов в ./test_sources будут проводится тесты. Первый тест проверяет правильность работы отдельно взятых функций, а второй по сути запускает приложение и проверяет, что все необходимые файлы и папки созданы.  
Чтобы добавить тест, необходимо вручную вносить его в код. Тестирование по фиду не реализовано.
