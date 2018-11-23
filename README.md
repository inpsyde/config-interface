# Inpsyde Config Interface [![Latest Stable Version](https://poser.pugx.org/inpsyde/config-interface/v/stable?format=flat-square)](https://packagist.org/packages/inpsyde/config-interface) [![Build Status](https://img.shields.io/travis-ci/inpsyde/config-interface.svg?style=flat-square)](https://travis-ci.org/inpsyde/config-interface) [![License](https://poser.pugx.org/inpsyde/config-interface/license?format=flat-square)](https://packagist.org/packages/inpsyde/config-interface)

The package provides a standard interface for a common configuration value container.

## Why

When it comes to more complex plugins you want to have a reliable and uniform way to access your configuration. Instead of coupling your business logic to details about configuration you can depend on an abstract configuration interface.


## The Config interface

    <?php
    
    namespace Inpsyde\Config;
    
    use Inpsyde\Config\Exception\Exception;
    
    interface Config
    {
        /**
         * @throws Exception
         * @return mixed
         */
        public function get(string $key);
    
        public function has(string $key) : bool;
    }

This interface reminds of PSR-11 and we considered to extend or simply use PRS-11 as interface but the documentation says that it is explicitly meant as common interface for [_dependency injection containers_](https://www.php-fig.org/psr/psr-11/).

Also mixing up DI-Containers with config containers is not a good thing as both targeting different purposes.


## License

Copyright (c) 2018 David Naber, Inpsyde GmbH

Good news, this plugin is free for everyone! Since it's released under the [MIT License](LICENSE) you can use it free of charge on your personal or commercial website.

## Contributing

All feedback, bug reports and pull requests are welcome.
