
# Estruturas de controle - loops

## Apresentação
[Loops](/introprog2024/pdf/aula07.pdf) 

## Exemplos

### Exemplo01

```
#!/usr/bin/perl 

# calcular a media de tamanho das sequencias em um array

@seqs = ("ATGGCGTAGATCG", "TAAGCCCCGGTATATTTGACCCCGAT", "GATAGAG");

# Passo 1: acessar elementos do array, calcular e armazenar comprimentos

$tamanho = # completar com os comandos;

# Passo 2: calcular a media

$media = # completar com os comandos;

# Passo 3: Imprimir resultado

print "\nExemplo 01:\n";

print "Media de tamanho = $media\n";

exit;
```

========

### Exemplo03 

```

# for() para imprimir conteudo de arrays

@seqs = ("ATGGCGTAGATCG", "TAAGCCCCGGTATATTTGACCCCGAT", "GATAGAG");

$seqs = @seqs; #numero de elementos do array

print "\nExemplo 03:\n";

print "Numero de sequencias = $seqs\n";

for ( $i = 0; $i < $seqs; $i++ ) {

    print ">Gene$i\n$seqs[$i]\n\n" ; 

}  
exit;
```

========

### Exemplo05

```
# foreach() para imprimir conteudo de arrays

print "\nExemplo 05:\n";

foreach $seq (@seqs) {

    print "$seq\n\n" ; 

}
```

========

### Exemplo07

```
# foreach() para imprimir conteudo de hashes

%seqs = ("Gene25", "ATGGCGTAGATCG",            
         "Gene49", "TAAGCCCCGGTATATTTGACCCCGAT", 
         "Gene03", "GATAGAG");
         
print "\nExemplo 07:\n";

#comandos         

exit;
```

========

### Exemplo 09

```
# foreach() para encontrar um valor especifico em hashes

print "\nExemplo 09:\n";

$seq_alvo = "GATAGAG"; # esta presente?

foreach $gene (keys(%seqs)) {

    if ($seqs{$gene} eq $seq_alvo) {
        print "Sequencia encontrada: $gene.\n\n"; 
    }
}
```

========

### Exemplo 10

```

#usando while

print "\nExemplo 10:\n";

$contagem = 10;

while($contagem > 0){
   print("$contagem\n");

   # contagem regressiva
   $contagem--;

   # pausar o script por 1s
   sleep(1);

   if($contagem == 0){
      print("Feliz Ano Novo!\n");
   }
}

exit;

```

========

### Exemplo 11

```
#usando until

print "\nExemplo 11:\n";

$n_secreto = 9;
$palpite;

# Loop 'until' ate adivinhar o numero secreto
until ($palpite == $n_secreto) {
   print "Digite o seu palpite: ";
   $palpite = <STDIN>;  # Ler a entrada 
   chomp($palpite);     # Remover newline
    
   # Verificar se o palpite está correto
   if ($palpite == $n_secreto) {
      print "Parabéns! Você adivinhou o número secreto.\n";
   } else {
      print "Errado! Tente novamente.\n";
   }
}

exit;

```

========

### Exemplo13 

```
# formas de imprimir arrays

@seqs = ("ATGGCGTAGATCG","TAAGCCCCGGTATATTTGACCCT", "GATAGAG");

# for
$seqs = @seqs;

print "\nExemplo 13 (for):\n";

for ( $i = 0; $i < $seqs; $i++ ) {
    print "$seqs[$i]\n" ; 
}
```
========

### Exemplo14

```
# formas de imprimir arrays

# foreach 

print "\nExemplo 14 (foreach):\n";

foreach $seq (@seqs) {
    print "$seq\n" ; 
}

```

========

### Exemplo15

```
# formas de imprimir arrays

# while
$n_seqs = @seqs;

$i = 0;

print "\nExemplo 15 (while):\n";

while ( $i < $n_seqs ) {
    print "$seqs[$i]\n"; 
}
```

========

Testing newfile
