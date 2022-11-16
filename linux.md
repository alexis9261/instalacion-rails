```bash
sudo apt install curl
curl -sL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

sudo apt-get update
sudo apt-get install git-core zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev software-properties-common libffi-dev nodejs yarn

```

Instalación rbenv - Entorno para poder ejecutar distintas versiones de Ruby en Linux


```bash

cd
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(rbenv init -)"' >> ~/.bashrc
exec $SHELL

git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc
exec $SHELL

```

Instalación ruby 3

```bash
rbenv install 3.1.2
rbenv global 3.1.2
```

Para ver todas las versiones de Ruby que se tienen instaladas

```bash
rbenv versions
```

Para cambiar a una version de Ruby en particular

```bash
rbenv global particular_version
rbenv global 2.7.0
```

Instalación bundler, manejador de paquetes de Ruby

```bash
gem install bundler
```

Instalación rails, instala el framework en el S.O. NO crea un proyecto, solo el instalador

```bash
gem install rails -v 7.0.2.4
```

Paso final, para refresacar configuraciones de rbenv, necesario si se realizo un cambio de version de Ruby

```bash
rbenv rehash
```

Comando final, verificamos que esta corriendo la version correcta de Ruby

```bash
ruby -v
```

Ahora creamos un proyecto Ruby on Rails, En cualquier directorio
```bash
cd path/
rails new app_name
```


