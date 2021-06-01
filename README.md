<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>


## Basement LMS

A criação da LMS vai dar ênfase em uma facilidade maior para que outros desenvolvedores Laravel entendam como é a modelagem de tudo.


Essa aplicação ainda está em desenvolvimento, caso você queira integrar ao time, mande um e-mail para os mantenedores!

```
danielhe4rt: hey@danielheart.dev
```

### Projeto
1. [] Base do Projeto
    * Tecnologias:
        * Bootstrap 4/5
        * Websockets (chat)
        * Azure Stream (streaming de video)
        * Docker
        * Larastan
        * Psalm ?
2. [] Autenticação
    * [] Métodos base: Sessão
    * [] Métodos custom: Discord e Twitch
3. [] Cursos
    1. [] Modelagem base:
4. [] Subscrição
    1. [] Método de pagamento: Stripe, GerenciaNet, Pagarme, Picpay
    2. [] Vinculação com Twitch: Subzada do Daniel é na faixa
    3. [] Formulário não pagante: Se não houver condições de comprar, deixa o salve que a gente libera!
5. Gameficação
6. Fórum
7. Chat

### Installation
* Run `git clone https://github.com/DanielHe4rt/basement-lms`
* `cd basement-lms`
* Run `composer install` (install composer beforehand)
* From the projects root run `cp .env.example .env`
* Configure your `.env` file, with:

Database settings
```
DB_DATABASE=lms_laravel
DB_USERNAME=root
DB_PASSWORD=root
```

Execute this comand for install Laravel Sail
`php artisan sail:install`

Select `mysql` for database

Create alias for this commando in your `~/.bashrc`

`alias sail='bash vendor/bin/sail'`

Now, utilize 
`sail up -d` for up your application.

Email settings (using a provider like Mailgun, Amazon SES, etc)

* Run `sail artisan key:generate`
* Run `sail artisan migrate`
* For Auth API (to configure Laravel Passport), run: `sail artisan passport:install`
* Run `sail npm install`
* Run `sail artisan db:seed`

* Start the Websocket server (for chat functionality) `sail artisan websockets:serve`



The application is running on `localhost:80`