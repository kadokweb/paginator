# Paginator @KadokWeb

[![Maintainer](http://img.shields.io/badge/maintainer-@kadokweb-blue.svg?style=flat-square)](https://twitter.com/kadokweb)
[![Source Code](http://img.shields.io/badge/source-kadokweb/paginator-blue.svg?style=flat-square)](https://github.com/kadokweb/paginator)
[![PHP from Packagist](https://img.shields.io/packagist/php-v/kadokweb/paginator.svg?style=flat-square)](https://packagist.org/packages/kadokweb/paginator)
[![Latest Version](https://img.shields.io/github/release/kadokweb/paginator.svg?style=flat-square)](https://github.com/kadokweb/paginator/releases)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Build](https://img.shields.io/scrutinizer/build/g/kadokweb/paginator.svg?style=flat-square)](https://scrutinizer-ci.com/g/kadokweb/paginator)
[![Quality Score](https://img.shields.io/scrutinizer/g/kadokweb/paginator.svg?style=flat-square)](https://scrutinizer-ci.com/g/kadokweb/paginator)
[![Total Downloads](https://img.shields.io/packagist/dt/kadokweb/paginator.svg?style=flat-square)](https://packagist.org/packages/kadokweb/paginator)

###### Paginator is an extremely compact and easy to use component. You only have to configure its behavior once by the counter, and then use the render method to create a nav with all the navigation links. Easy with having a coffee to use and interacting with your database.

Paginator é um componente extremamente compacto e fácil de usar. Você só precisa configurar seu comportamento uma vez pelo construtor, e depois usar o método render para criar uma nav com todos os links de navegação. Fácil com tomar um café para usar e interagir com seu banco de dados.

## About KadokWeb

###### KadokWeb is a set of small and optimized PHP components for common tasks.With them you perform routine tasks with fewer lines, writing less and doing much more.

KadokWeb é um conjunto de componentes PHP pequenos e otimizados para tarefas comuns. Com eles, você executa tarefas rotineiras com menos linhas, escreve menos e faz muito mais.

### Highlights


- Easy to configure and customize via ***constructor*** class (Fácil para configurar e personalizar via ***construtor*** da classe)
- Simple to generate paging with only five arguments (Simples de gerar paginação com apenas cinco argumentos)
- ***pager*** method to assemble results pagination (Método ***pager*** para montar a paginação de resultados)
- ***render*** method to mount html ready to navigate (Método ***render*** para montar o html pronto para navegar)
- Navigation structure with custom classes in elemenos ***nav***, ***a*** and ***span*** (Estrutura de navegação com classes personalizadas em elemenos ***nav***, ***a*** e ***span***)
- Methods ***limit*** and ***offset*** to retrieve values ​​and integrate your ***SQL query*** (Método ***limit*** e ***offset*** para resgatar valores e integrar a sua ***consulta SQL***)
- Composer ready and PSR-2 compliant (Pronto para o composer e compatível com PSR-2)

## Installation

Paginator is available via Composer:

```bash
"kadokweb/paginator": "^1.0"
```

or run

```bash
composer require kadokweb/paginator
```

## Documentation

###### For details on how to use the paginator, see the sample folder with details in the component directory

Para mais detalhes sobre como usar o paginator, veja a pasta de exemplo com detalhes no diretório do componente

```php
<?php
require __DIR__ . "/../vendor/autoload.php";

$page = filter_input(INPUT_GET, "page", FILTER_VALIDATE_INT);
$pager = new \KadokWeb\Paginator\Paginator();
$pager->pager($page, 100, 10);

echo $pager->render();
```

##### Result

````html
<nav class="paginator">
    <a class='paginator_item' title="Primeira página" href="?page=1"><<</a>
    <span class="paginator_item paginator_active">1</span>
    <a class='paginator_item' title="Página 2" href="?page=2">2</a>
    <a class='paginator_item' title="Página 3" href="?page=3">3</a>
    <a class='paginator_item' title="Página 4" href="?page=4">4</a>
    <a class='paginator_item' title="Última página" href="?page=10">>></a>
</nav>
````

## Contributing

Please see [CONTRIBUTING](https://github.com/kadokweb/paginator/blob/master/CONTRIBUTING.md) for details.

## Support

###### Security: If you discover any security related issues, please email cursos@upinside.com.br instead of using the issue tracker.

Se você descobrir algum problema relacionado à segurança, envie um e-mail para cursos@upinside.com.br em vez de usar o rastreador de problemas.

Thank you

## Credits

- [Robson V. Leite](https://github.com/kadokweb) (Developer)
- [UpInside Treinamentos](https://github.com/upinside) (Team)
- [All Contributors](https://github.com/kadokweb/paginator/contributors)

## License

The MIT License (MIT). Please see [License File](https://github.com/kadokweb/paginator/blob/master/LICENSE) for more information.