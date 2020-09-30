# Ansible
Esse repositório foi criado como forma de armazenar configurações bases para ferramentas que utilizo em meu dia a dia, mas está aberto a qualquer pessoa que queira fazer uso.

Essas configurações foram criadas para execução remota utilizando escalação de privilégios com usuario SUDO.

Para executar os playbooks com escalação de privilégio é utilizado o seguinte comando:

ansible-playbook update.yaml --ask-become-pass -k -e "host=teste.xtz" -t update

-e                      Variavel de host, se quiser executar apenas em um host, se quiser executar em todo o ambiente, basta tirar esse Parâmetro.
--ask-become-pass       Esse Parâmetro solicita senha para o usuario SUDO
-k                      Esse Parâmetro solicita senha para o login do usuário no servidor (Usuario pessoal e não o root)
-t                      Esse Parâmetro é utilizado quando se defini tags para uma task