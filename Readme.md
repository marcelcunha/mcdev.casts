# Casts 

Esse pacote trás uma coleção de Casts customizados para serem usados com Laravel 7 ou superior.

## Instalação

```composer require mcdev/casts```

## Uso

No arquivo da model, importe o cast desejado, em seguida adicione-o no array de casts junto ao atributo escolhido. Exemplo:

```php
<?php

namespace App\Models;

use MCDev\Casts\CPFCast;

class User 
{

    protected $casts = [
        'cpf' => CPFCast::class,
    ];
}

```

## Casts

Todos casts salvam tipos primitivos (string, integer, double) no banco de dados.

Atualmente existem os seguintes casts no pacote com um exemplo do formato do accessor: 

```
CPFCast             111.222.333-44
DateCast            24/05/2008
DateTimeCast        22/08/2005 14:26
MoneyRealCast       R$ 14.589,23
PhoneCast           (88) 5555-6666 ou (88) 95555-66666
```
