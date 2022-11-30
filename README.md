# devops-netology
Будут проигнорированы следующие файлы:

**/.terraform/* - игнорировать все файлы из директорий которые имеют в пути последней папку .terraform

# .tfstate files
*.tfstate - все файлы с расширением .tfstate
*.tfstate.* - все файлы содержащие в середине названия .tfstate.

# Crash log files
crash.log - файлы с именем crash.log
crash.*.log - файлы содержащие в имени любые символы между crash. и .log

# Exclude all .tfvars files, which are likely to contain sensitive data, such as
# password, private keys, and other secrets. These should not be part of version 
# control as they are data points which are potentially sensitive and subject 
# to change depending on the environment.
*.tfvars - файлы с расширением .tfvars
*.tfvars.json - файлы начинающиеся с любых символов и заканчивающиеся как .tfvars.json

# Ignore override files as they are usually used to override resources locally and so
# are not checked in
override.tf - файлы с именем override.tf
override.tf.json - файлы с именем override.tf.json
*_override.tf - файлы с именем начинающимся на любые символы и заканчивающимся как _override.tf
*_override.tf.json -файлы с именем начинающимся на любые символы и заканчивающимся как _override.tf.json

# Include override files you do wish to add to version control using negated pattern
# !example_override.tf

# Include tfplan files to ignore the plan output of command: terraform plan -out=tfplan
# example: *tfplan*

# Ignore CLI configuration files
.terraformrc - файлы с именем .terraformrc
terraform.rc - файлы с именем terraform.rc
