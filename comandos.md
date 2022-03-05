# Estegonagrafia


## Comando CAT

### Para Criptografar

cat skyfall_cat_in.jpg segredo.txt > skyfall_cat_out.jpg

### Para vizualizar ou extrari o conteudo

strings skyfall_cat_out.jpg 

Note que o segredo.txt é inserido no final do arquivo.

split -b 150871 skyfall_cat_out.jpg


## Comando STEGHIDE

### Para Criptografar 

steghide embed -cf skyfall_steghide.jpg -ef segredo.txt 

senha: 123456

### Para Extrair

steghide extract -sf skyfall_steghide.jpg

senha: 123456


## Comando Outguess

## Para Criptografar

outguess -k 123456 -d segredo.txt skyfall_original.jpg skyfall_outguess.jpg 

senha: 123456


## Para extrair

outguess -k 123456 -r skyfall_original_outguess.jpg segredo.txt

senha: 12346


## Criptoanalise


### Verificação de MD5

md5sum skyfall*

xxd skyfall_cat_out.jpg >> skyfall_cat_out.hex

ghex skayfall_cat_out.jpg &

### Ferramenta Stegdetect




