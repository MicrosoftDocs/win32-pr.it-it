---
description: Le colonne archiviate nell'indice di contenuto possono avere più valori e le colonne multivalore possono essere confrontate tramite il predicato di confronto della matrice.
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: Confronti multivalore (matrice)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77710ecdddcf289c9a5c64d0c5f57ca449311097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750375"
---
# <a name="multi-valued-array-comparisons"></a>Confronti multivalore (matrice)

Le colonne archiviate nell'indice di contenuto possono avere più valori e le colonne multivalore possono essere confrontate tramite il predicato di confronto della matrice.

Il predicato di confronto della matrice presenta la sintassi seguente:


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



Se il riferimento alla colonna non è una colonna multivalore, viene restituito un errore. Il tipo di dati della colonna deve essere compatibile con gli elementi dell'elenco di confronto. Se necessario, è possibile [eseguire il cast](-search-sql-castingdatacolumntype.md) del riferimento di colonna come un altro tipo di dati.

L'operatore di confronto (comp \_ op) può essere uno qualsiasi degli operatori di confronto normali. In un confronto multivalore, gli operatori di confronto hanno significati leggermente diversi a seconda che si utilizzi un quantificatore. I quantificatori identificano se è necessario eseguire un confronto in base a tutti o solo alcuni dei valori nell'elenco di confronto. Le funzioni degli operatori di confronto sono fornite nelle tabelle che descrivono ogni quantificatore (tutti e alcuni) più avanti in questo documento.

Il valore dopo l'operatore specifica un singolo valore letterale che viene confrontato con tutti gli elementi della colonna multivalore. Se un elemento corrisponde al valore, il predicato è true.

Nell'elenco di confronto viene specificata una matrice di valori letterali confrontati con la colonna multivalore. Di seguito è riportata la sintassi per l'elenco di confronto:


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> Tenere presente la sintassi dell'elenco di confronto. Il gruppo di valori letterali che costituiscono l'elenco di confronto deve essere racchiuso tra parentesi quadre. Non racchiudere i singoli elementi dell'elenco di confronto tra parentesi quadre. Pertanto, ARRAY \[ 1 \] e Array 1 \[ , 2, 3 \] sono validi, ma \[ la matrice 1 \[ , 2 \] \[ , 3 non lo \] \] è.

 

Il metodo utilizzato per determinare se il confronto multivalore restituisce true o false viene specificato dal quantificatore facoltativo. Le sezioni seguenti descrivono ogni quantificatore e come funziona ogni operatore di confronto quando viene usato il quantificatore.

## <a name="absent-quantifier"></a>Quantificatore assente

Se non viene specificato alcun quantificatore, ogni elemento sul lato sinistro del confronto viene confrontato con l'elemento nella stessa posizione sul lato destro. Il confronto inizia con il primo elemento nelle matrici e avanza nell'ultimo elemento. Se tutti gli elementi sul lato sinistro sono equivalenti agli elementi corrispondenti sul lato destro, il numero di elementi della matrice viene usato per determinare quale matrice è maggiore.

Nella tabella seguente viene illustrato il funzionamento degli operatori di confronto quando non è specificato alcun quantificatore e viene fornita una breve descrizione di ciascuno di essi.



| Operatore       | Descrizione                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | ' Equal to ' restituisce true quando ogni elemento di sinistra ha lo stesso valore dell'elemento a destra corrispondente e entrambe le matrici hanno lo stesso numero di elementi.                                                                                                                                                                                                                     |
| ! = o <> | ' Diverso da' restituisce true quando uno o più elementi di sinistra hanno valori diversi dagli elementi a destra corrispondenti o quando le matrici di sinistra e di destra non hanno lo stesso numero di elementi.                                                                                                                                                              |
| >           | ' Maggiore di ' restituisce true quando il valore di ogni elemento di sinistra è maggiore del valore dell'elemento a destra corrispondente. Se tutti i valori degli elementi a sinistra corrispondono esattamente ai corrispondenti elementi a destra e la matrice di sinistra contiene più elementi rispetto alla matrice di destra,' maggiore di ' restituisce true.                                                     |
| >=          | ' Maggiore o uguale a' restituisce true quando il valore di ogni elemento di sinistra è maggiore o uguale al valore dell'elemento a destra corrispondente. Se tutti i valori degli elementi a sinistra sono uguali o maggiori dei corrispondenti elementi a destra e la matrice di sinistra ha gli stessi o più elementi della matrice di destra,' maggiore di ' restituisce true. |
| <           | ' Less than ' restituisce true quando il valore di ogni elemento di sinistra è minore del valore dell'elemento a destra corrispondente. ' Minor di ' restituisce anche true quando il lato sinistro ha meno elementi del lato destro.                                                                                                                                                  |
| <=          | ' Minore o uguale a' restituisce true quando il valore di ogni elemento di sinistra è minore o uguale al valore dell'elemento a destra corrispondente. Se tutti i valori degli elementi a sinistra sono uguali o minori degli elementi di destra corrispondenti e la matrice di sinistra ha lo stesso o meno elementi della matrice di destra,' maggiore di ' restituisce true.         |



 

## <a name="all-quantifier"></a>TUTTI i quantificatori

Il quantificatore ALL specifica che ogni elemento sul lato sinistro viene confrontato con ogni elemento sul lato destro. Per restituire true, il confronto deve essere true per ogni elemento sul lato sinistro rispetto a ogni elemento sul lato destro. Il numero di elementi nei lati della matrice sinistra e destra non ha alcun effetto sul risultato.

Nella tabella seguente viene illustrato il funzionamento di ogni operatore di confronto con il quantificatore ALL.



| Operatore       | Descrizione                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | ' Equal to ' restituisce true quando ogni valore dell'elemento di sinistra è uguale a ogni valore di elemento a destra.                              |
| ! = o <> | ' Diverso da' restituisce true quando almeno uno dei valori degli elementi a sinistra è diverso da uno qualsiasi dei valori degli elementi a destra. |
| >           | ' Maggiore di ' restituisce true quando ogni valore dell'elemento di sinistra è maggiore di ogni valore di elemento a destra.                         |
| >=          | ' Maggiore o uguale a' restituisce true quando ogni valore dell'elemento di sinistra è maggiore o uguale a ogni valore di elemento a destra. |
| <           | ' Less than ' restituisce true quando ogni valore dell'elemento di sinistra è minore di ogni valore di elemento a destra.                               |
| <=          | ' Minore o uguale a' restituisce true quando ogni valore dell'elemento di sinistra è minore o uguale a ogni valore di elemento a destra.       |



 

## <a name="some-or-any-quantifier"></a>UN quantificatore (o qualsiasi)

Il quantificatore SOME e il quantificatore ANY possono essere usati in modo interscambiabile. Come il quantificatore ALL, il quantificatore SOME specifica che ogni elemento sul lato sinistro viene confrontato con ogni elemento sul lato destro. Per restituire true, il confronto deve essere true per almeno uno degli elementi sul lato sinistro rispetto a qualsiasi elemento a destra. Il numero di elementi nelle matrici di sinistra e di destra non ha alcun effetto sul risultato.

Nella tabella seguente viene illustrato il funzionamento di ogni operatore di confronto con il quantificatore SOME.



| Operatore       | Descrizione                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | ' Equal to ' restituisce true quando almeno uno dei valori degli elementi a sinistra è uguale a uno dei valori degli elementi a destra.                                  |
| ! = o <> | ' Diverso da' restituisce true se nessuno dei valori degli elementi a sinistra è uguale a uno dei valori degli elementi a destra.                                      |
| >           | ' Maggiore di ' restituisce true quando almeno uno dei valori degli elementi a sinistra è maggiore di uno dei valori degli elementi a destra.                         |
| >=          | ' Maggiore o uguale a' restituisce true quando almeno uno dei valori degli elementi di sinistra è maggiore o uguale a uno dei valori degli elementi a destra. |
| <           | ' Less of ' restituisce true quando almeno uno dei valori degli elementi a sinistra è minore di uno dei valori degli elementi a destra.                               |
| <=          | ' Minore o uguale a' restituisce true quando almeno uno dei valori degli elementi di sinistra è minore o uguale a uno dei valori degli elementi a destra.       |



 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene verificato se i documenti sono inclusi nelle categorie "Finance" o "Planning":


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



Tutti i confronti seguenti restituiscono true. Tenere presente che, nell'uso effettivo, la sintassi della query di ricerca richiede che il lato sinistro sia una proprietà, non un valore letterale.


```
ARRAY [1,2] > ARRAY [1,1]
ARRAY [1,2] > ARRAY [1,1,2]
ARRAY [1,2] < ARRAY [1,2,3]
ARRAY [1,2] = SOME ARRAY [1,12,27,35,2]
ARRAY [1,1] != ALL ARRAY [1,2]
ARRAY [1,20,21,22] < SOME ARRAY [0,40]
ARRAY [1,20,21,22] < ANY ARRAY [0,40]
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Predicato LIKE](-search-sql-like.md)
</dt> <dt>

[Confronto di valori letterali](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Predicato NULL](-search-sql-null.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



