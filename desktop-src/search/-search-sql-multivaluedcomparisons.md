---
description: Le colonne archiviate nell'indice di contenuto possono avere più valori e tali colonne multivalore possono essere confrontate usando il predicato di confronto ARRAY.
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: Confronti multivalore (ARRAY)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043ed6744717ac3156d9dd64f2f6806f2ffc509107f5bcdc8a66980e5cdd0012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863370"
---
# <a name="multi-valued-array-comparisons"></a>Confronti multivalore (ARRAY)

Le colonne archiviate nell'indice di contenuto possono avere più valori e tali colonne multivalore possono essere confrontate usando il predicato di confronto ARRAY.

Il predicato di confronto ARRAY ha la sintassi seguente:


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



Se il riferimento alla colonna non è una colonna multivalore, viene restituito un errore. Il tipo di dati della colonna deve essere compatibile con gli elementi dell'elenco di confronto. Se necessario, è possibile eseguire il cast del riferimento [alla colonna](-search-sql-castingdatacolumntype.md) come un altro tipo di dati.

L'operatore di confronto (comp \_ op) può essere uno qualsiasi degli operatori di confronto normali. In un confronto multivalore, gli operatori di confronto hanno significati leggermente diversi a seconda che sia usato un quantificatore. I quantificatori identificano se è necessario eseguire un confronto con tutti o alcuni valori nell'elenco di confronto. Le funzioni degli operatori di confronto vengono fornite nelle tabelle che descrivono ogni quantificatore (ALL e SOME) più avanti in questo documento.

Il valore dopo l'operatore specifica un singolo valore letterale che viene confrontato con tutti gli elementi della colonna multivalore. Se un elemento corrisponde al valore, il predicato è true.

L'elenco di confronto specifica una matrice di valori letterali confrontati con la colonna multivalore. La sintassi per l'elenco di confronto è la seguente:


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> Tenere presente la sintassi dell'elenco di confronto. Il gruppo di valori letterali che costituiscono l'elenco di confronto deve essere racchiuso tra parentesi quadre. Non racchiudere i singoli elementi dell'elenco di confronto tra parentesi quadre. Pertanto, ARRAY \[ 1 \] e ARRAY \[ 1,2,3 sono \] validi, mentre ARRAY \[ 1 \[ ,2 \] \[ ,3 \] \] non lo è.

 

Metodo utilizzato per determinare se il confronto multivalore restituisce true o false specificato dal quantificatore facoltativo. Le sezioni seguenti descrivono ogni quantificatore e il funzionamento di ogni operatore di confronto quando viene usato il quantificatore.

## <a name="absent-quantifier"></a>Quantificatore assente

Se non viene specificato alcun quantificatore, ogni elemento a sinistra del confronto viene confrontato con l'elemento nella stessa posizione a destra. Il confronto inizia con il primo elemento nelle matrici e procede fino all'ultimo elemento. Se tutti gli elementi a sinistra sono equivalenti agli elementi corrispondenti a destra, il numero di elementi della matrice viene usato per determinare quale matrice è maggiore.

Nella tabella seguente viene illustrato il funzionamento degli operatori di confronto quando non viene specificato alcun quantificatore e viene fornita una breve descrizione di ognuno.



| Operatore       | Descrizione                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | 'Equal to' restituisce true quando ogni elemento di sinistra ha lo stesso valore dell'elemento di destra corrispondente ed entrambe le matrici hanno lo stesso numero di elementi.                                                                                                                                                                                                                     |
| != o <> | 'Diverso da' restituisce true quando uno o più elementi sul lato sinistro hanno valori diversi dagli elementi di destra corrispondenti o quando le matrici di sinistra e di destra non hanno lo stesso numero di elementi.                                                                                                                                                              |
| >           | 'Greater than' restituisce true quando il valore di ogni elemento a sinistra è maggiore del valore dell'elemento di destra corrispondente. Se tutti i valori degli elementi sul lato sinistro corrispondono esattamente agli elementi di destra corrispondenti e la matrice sul lato sinistro contiene più elementi rispetto alla matrice di destra, "maggiore di" restituisce true.                                                     |
| >=          | 'Maggiore o uguale a' restituisce true quando il valore di ogni elemento a sinistra è maggiore o uguale al valore dell'elemento di destra corrispondente. Se tutti i valori degli elementi a sinistra sono uguali o maggiori degli elementi di destra corrispondenti e la matrice sul lato sinistro ha gli stessi o più elementi della matrice di destra, 'greater than' restituisce true. |
| <           | 'Less than' restituisce true quando il valore di ogni elemento a sinistra è minore del valore dell'elemento di destra corrispondente. 'Minore di' restituisce true anche quando il lato sinistro ha meno elementi rispetto al lato destro.                                                                                                                                                  |
| <=          | 'Minore o uguale a' restituisce true quando il valore di ogni elemento a sinistra è minore o uguale al valore dell'elemento di destra corrispondente. Se tutti i valori degli elementi a sinistra sono uguali o minori degli elementi di destra corrispondenti e la matrice sul lato sinistro ha lo stesso o un numero inferiore di elementi rispetto alla matrice di destra, "maggiore di" restituisce true.         |



 

## <a name="all-quantifier"></a>Quantificatore ALL

Il quantificatore ALL specifica che ogni elemento a sinistra viene confrontato con ogni elemento a destra. Per restituire true, il confronto deve essere true per ogni elemento a sinistra rispetto a ogni elemento a destra. Il numero di elementi nei lati sinistro e destro della matrice non ha alcun effetto sul risultato.

Nella tabella seguente viene illustrato il funzionamento di ogni operatore di confronto con il quantificatore ALL.



| Operatore       | Descrizione                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | 'Equal to' restituisce true quando ogni valore di elemento a sinistra corrisponde a ogni valore di elemento a destra.                              |
| != o <> | 'Diverso da' restituisce true quando almeno uno dei valori dell'elemento a sinistra è diverso da uno dei valori degli elementi di destra. |
| >           | 'Greater than' restituisce true quando ogni valore di elemento a sinistra è maggiore di ogni valore di elemento a destra.                         |
| >=          | 'Maggiore o uguale a' restituisce true quando ogni valore di elemento a sinistra è maggiore o uguale a ogni valore di elemento a destra. |
| <           | 'Less than' restituisce true quando ogni valore di elemento a sinistra è minore di ogni valore di elemento a destra.                               |
| <=          | 'Minore o uguale a' restituisce true quando ogni valore di elemento a sinistra è minore o uguale a ogni valore di elemento a destra.       |



 

## <a name="some-or-any-quantifier"></a>Quantificatore SOME (o ANY)

Il quantificatore SOME e il quantificatore ANY possono essere usati in modo intercambiabile. Analogamente al quantificatore ALL, il quantificatore SOME specifica che ogni elemento a sinistra viene confrontato con ogni elemento a destra. Per restituire true, il confronto deve essere true per almeno uno degli elementi a sinistra rispetto a qualsiasi elemento a destra. Il numero di elementi nelle matrici a sinistra e a destra non ha alcun effetto sul risultato.

La tabella seguente illustra il funzionamento di ogni operatore di confronto con il quantificatore SOME.



| Operatore       | Descrizione                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | 'Equal to' restituisce true quando almeno uno dei valori dell'elemento a sinistra corrisponde a uno qualsiasi dei valori degli elementi di destra.                                  |
| != o <> | 'Diverso da' restituisce true quando nessuno dei valori degli elementi a sinistra corrisponde a uno dei valori degli elementi di destra.                                      |
| >           | 'Greater than' restituisce true quando almeno uno dei valori dell'elemento a sinistra è maggiore di uno qualsiasi dei valori degli elementi di destra.                         |
| >=          | 'Greater than or equal to' restituisce true quando almeno uno dei valori dell'elemento a sinistra è maggiore o uguale a uno dei valori degli elementi di destra. |
| <           | 'Less than' restituisce true quando almeno uno dei valori dell'elemento a sinistra è minore di uno dei valori degli elementi di destra.                               |
| <=          | 'Minore o uguale a' restituisce true quando almeno uno dei valori dell'elemento a sinistra è minore o uguale a uno dei valori degli elementi di destra.       |



 

## <a name="examples"></a>Esempio

L'esempio seguente controlla se i documenti sono nelle categorie "Finance" o "Planning":


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



Tutti i confronti seguenti restituiscono true. Tenere presente che nell'uso effettivo la sintassi della query di ricerca richiede che il lato sinistro sia una proprietà, non un valore letterale.


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

[Confronto tra valori letterali](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Predicato NULL](-search-sql-null.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



