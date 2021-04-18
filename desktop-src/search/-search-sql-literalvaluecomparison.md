---
description: Il confronto dei valori letterali usa gli operatori di confronto standard per la corrispondenza di una colonna a valore singolo con un valore letterale.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Confronto di valori letterali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8577e5a97dcc92131658c325f175efa1d0c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306120"
---
# <a name="literal-value-comparison"></a>Confronto di valori letterali

Il confronto dei valori letterali usa gli operatori di confronto standard per la corrispondenza di una colonna a valore singolo con un valore [letterale](-search-sql-literals.md) . Per informazioni sul confronto tra colonne multivalore, vedere [confronti con più valori (Array)](-search-sql-multivaluedcomparisons.md).

Il predicato di confronto dei valori letterali presenta la sintassi seguente:


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> Il lato destro del confronto deve essere un valore letterale. Non è possibile confrontare una colonna con un valore calcolato e non è possibile confrontare una colonna con un'altra colonna.

 

La parte colonna è qualsiasi colonna di proprietà valida ed è possibile eseguirne il cast a un altro tipo, se necessario. Facoltativamente, è possibile racchiudere il nome della colonna tra virgolette doppie per migliorare la leggibilità senza influire sulle funzionalità. Per ulteriori informazioni, vedere [cast del tipo di dati di una colonna](-search-sql-castingdatacolumntype.md).

Il valore letterale può essere qualsiasi valore letterale stringa, numerico, esadecimale, booleano o data, racchiuso tra virgolette singole. Vengono riconosciute solo le corrispondenze esatte e i caratteri jolly vengono ignorati. È anche possibile eseguire il cast del valore letterale a un altro tipo.

## <a name="comparison-operators"></a>Operatori di confronto

Nella tabella seguente vengono descritti gli operatori di confronto supportati.



| Operatore di confronto | Descrizione              |
|---------------------|--------------------------|
| =                   | Uguale a                 |
| ! = o <>      | Diverso da             |
| >                | Maggiore di             |
| >=               | Maggiore o uguale a |
| <                | Minore di                |
| <=               | Minore o uguale a    |



 

 

In combinazione con l'operatore "=", Windows Search Structured Query Language (SQL) supporta l'utilizzo delle parole chiave BEFORe e AFTER, che specificano se la query deve confrontare i valori di colonna prima o dopo un valore specificato, nell'ordinamento del dizionario.


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a>Esempio

Di seguito sono riportati esempi del predicato di confronto dei valori letterali.


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Predicato LIKE](-search-sql-like.md)
</dt> <dt>

[DATEADD (funzione)](-search-sql-dateadd.md)
</dt> <dt>

[Confronti multivalore (matrice)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[Predicato NULL](-search-sql-null.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



