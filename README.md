# IMAGE UPLOADER:
Uma simples biblioteca para fazer upload de uma imagens.
## Instalação:
Para instalara esta biblioteca basta digitar o comando
composer require voneka/image-uploader

## Implementação:
```php

require '../vendor/autoload.php';
use Voneka\ImageUploader;

 if ($request->hasFile('nome do campo') && $request->file('nome do campo')->isValid()) {
    $imagem = $request->file('nome do campo');
    $nomeImagem = ImagemUploader::uploadImagem($imagem, $diretorio, ['jpeg', 'png','svg'], $peso, $larguraMaxima, $alturaMaxima, $larguraMinima, $alturaMinima);
    /* Já com o nome da imagem guardada pode fazer a lógima de armazenamento da url da imagem no seu banco de dados.
    Lembrando que a biblioteca só retorna o nome da imagem e não o endereço completo. */
   }     
```
## Requesitos
PHP 7.0 ou Superior

 
