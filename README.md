# IMAGE UPLOADER:
Esta é uma biblioteca bastante simples para fazer upload de imagens.
Com uma única linha é possivel fazer upload de imagens bastando fornecer os parametros necessários.
## Instalação:
Para instalara esta biblioteca basta digitar o comando na raiz do projecto:

composer require voneka/image-uploader

## Implementação:
```php

require '../vendor/autoload.php';
use Voneka\ImageUploader;
  #Antes de mais fazemos a verificação da existencia da imagem válida ou não.
 if ($request->hasFile('nome do campo') && $request->file('nome do campo')->isValid()) {
    $imagem = $request->file('nome do campo');
    //Se quiser mais extensoes é só adicionar  no array ['jpeg', 'png','svg'].
    $nomeImagem = ImagemUploader::uploadImagem($imagem, $diretorio, ['jpeg', 'png','svg'], $peso, $larguraMaxima, $alturaMaxima, $larguraMinima, $alturaMinima);
    /* Já com o nome da imagem guardada pode fazer a lógima de armazenamento da url da imagem no seu banco de dados.
    Lembrando que a biblioteca só retorna o nome da imagem e não o endereço completo. */
   }     
```
## Requesitos
PHP 7.0 ou Superior

 
