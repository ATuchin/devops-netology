# devops-netology
edited file MD

.gitignore внутри terraform позволит игнорировать в общих чертах файлы: ./terraform игнорирует файл terraform в той же директории

*.tfstate игнорирует все файлы по шаблону где 0 или более символов до .tfstate например 1.tfstate .tfstate. игнорирует все файлы по шаблону где 0 или более символов до .tfstate и 0 или более символов после tfstate.

crash.log игнорирует файлы логи crash.*.log в том числе начинающиеся на crash до точки, далее любое количество сиволов до точки и с раширением log

игнорирует различные файлы конфигураций и секретов *.tfvars любые с расширеним .tfvars *.tfvars.json любые с расширеним .tfvars.json

игнорирует файлы с именем override расшиением tf, override.tf.json override.tf override.tf.json *_override.tf игнорирует любые файлы по шаблону любые символы до_override.tf *_override.tf.json игнорирует любые файлы по шаблону любые символы до _override.tf.json .terraformrc игнорирует файл c именем terraformrc и terraform.rc terraform.rc

////Добавлена строка ДЗ 3 задание 3