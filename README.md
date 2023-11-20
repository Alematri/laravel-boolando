* Laravel Boolando 
===
Create un nuovo progetto Laravel. Concentratevi sul layout: create un file di layout in cui inserire la struttura comune di tutte le pagine del sito web (tag head, tag body, ...) eventualmente includendo header e footer tramite due partials.
Create poi una rotta per visualizzare la lista di tutti i prodotti recuperati da un file inserito nella cartella config e abbellite il tutto sfruttando SASS.
Bonus:
Create più pagine istituzionali che condividono lo stesso layout (ad es. about, oppure la pagina di dettaglio di un prodotto)
Buon lavoro!
PS create il progetto con laravel 9
composer create-project --prefer-dist laravel/laravel:^9.2 your_project_name_here
poi, entrate nella cartella e intallate il paccheto di Fabio Pacifici
composer require pacificdev/laravel_9_preset
poi installate ui di boostrap
php artisan preset:ui bootstrap
e poi npm install e npm run dev su un teminale e nell’altro php artisan serve
products.php
 
<?php
​
return [
  [
    "id" => 1,
    "frontImage" => "1.webp",
    "backImage" => "1b.webp",
    "brand" => "Levi's",
    "name" => "Relaxed Fit",
    "price" => 29.99,
    "isInFavorites" => true,
    "badges" => [
      [
        "type" => "tag",
        "value" => "Sostenibilità"
      ],
      [
        "type" => "discount",
        "value" => "-50%"
      ]
    ]
  ],
  [
    "id" => 2,
    "frontImage" => "2.webp",
    "backImage" => "2b.webp",
    "brand" => "Guess",
    "name" => "Roses Tee",
    "price" => 20.99,
    "isInFavorites" => true,
    "badges" => [
      [
        "type" => "discount",
        "value" => "-30%"
      ]
    ]
  ],
  [
    "id" => 3,
    "frontImage" => "3.webp",
    "backImage" => "3b.webp",
    "brand" => "Come Zucchero Filato",
    "name" => "Voglia di colori pastello",
    "price" => 129.99,
    "isInFavorites" => false,
    "badges" => [
      [
        "type" => "discount",
        "value" => "-30%"
      ]
    ]
  ],
  [
    "id" => 4,
    "frontImage" => "4.webp",
    "backImage" => "4b.webp",
    "brand" => "Levi's",
    "name" => "Tee Unisex",
    "price" => 14.99,
    "isInFavorites" => false,
    "badges" => [
      [
        "type" => "tag",
        "value" => "Sostenibilità"
      ],
      [
        "type" => "discount",
        "value" => "-50%"
      ]
    ]
  ],
  [
    "id" => 5,
    "frontImage" => "5.webp",
    "backImage" => "5b.webp",
    "brand" => "Maya Deluxe",
    "name" => "Stripe Bodice",
    "price" => 99.99,
    "isInFavorites" => true,
    "badges" => [
      [
        "type" => "tag",
        "value" => "Sostenibilità"
      ],
      [
        "type" => "discount",
        "value" => "-50%"
      ]
    ]
  ],
  [
    "id" => 6,
    "frontImage" => "6.webp",
    "backImage" => "6b.webp",
    "brand" => "Esprit",
    "name" => "Maglione - Black",
    "price" => 29.99,
    "isInFavorites" => true,
    "badges" => [
      [
        "type" => "tag",
        "value" => "Sostenibilità"
      ]
    ]
  ]
]
​
?>
