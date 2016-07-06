# Twig loader for flysystem filesystems

[Flysystem](http://flysystem.thephpleague.com/) loader for the [Twig](http://twig.sensiolabs.org/) templating engine.

## Installation

The library is installable through composer:

```bash
composer require cedricziel/twig-loader-flysystem
```

## Usage

Adapted from the [official Twig documentation](http://twig.sensiolabs.org/doc/api.html#basics)

```php
$localAdapter = new League\Flysystem\Adapter\Local(__DIR__);
$filesystem = League\Flysystem\Filesystem($localAdapter);

$loader = new CedricZiel\TwigLoaderFlysystem\FlysystemLoader($filesystem);
$twig = new \Twig_Environment($loader);

$template = $twig->loadTemplate('index.html');
$content = $template->render(array('the' => 'variables', 'go' => 'here'));
```

## License

MIT
