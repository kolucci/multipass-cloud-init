# multipass-cloud-init
multipass + cloud-init repository for local cloud deployments

## Установка Multipass в Ubuntu Linux
```sh
$ sudo snap install multipass
```

## Запуск LTS нод

- Запуск ноды (по умолчанию, вы получите текущий Ubuntu LTS)
  `multipass launch --name foo`
- Запуск комманд на ноде, пробует запустить bash (`logout` или `ctrl-d` для выхода)
  `multipass exec foo -- lsb_release -a`
- Передать мета-данные *cloud-init* из файла при запуске. ([Подробности](https://cloudinit.readthedocs.io/en/latest/topics/examples.html "Примеры для cloud-config.yaml"))
  `multipass launch -n bar --cloud-init cloud-config.yaml`
- Просмотр существующих нод
  `multipass list`
- Останов и запуск нод
  ```sh
  multipass stop foo bar
  multipass start foo
  ```
- Удаление и очистка ненужных нод
  ```sh
  multipass delete bar
  multipass purge
  ```
- Найти альтернативные образы для запуска с помощью *multipass*
  `multipass find`
- Дополнительная помощь
  ```sh
  multipass help
  multipass help <command>
  ```
