---
description: Il confronto dei valori letterali usa operatori di confronto standard per la corrispondenza tra una colonna a valore singolo e un valore letterale.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Confronto tra valori letterali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1e311c6f98c1114b63a1bf650d6e7be004e1e8e4cf5848b962a7cbf8049bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227176"
---
# <a name="literal-value-comparison"></a>Confronto tra valori letterali

Il confronto dei valori letterali usa operatori di confronto standard per la corrispondenza tra una colonna a valore singolo e un [valore letterale.](-search-sql-literals.md) Per informazioni sul confronto tra colonne multivalore, vedere Confronti multivalore [(ARRAY).](-search-sql-multivaluedcomparisons.md)

Il predicato di confronto dei valori letterali ha la sintassi seguente:


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> Il lato destro del confronto deve essere un valore letterale. Non è possibile confrontare una colonna con un valore calcolato e non è possibile confrontare una colonna con un'altra colonna.

 

La parte della colonna è qualsiasi colonna di proprietà valida e può essere eseguito il cast a un altro tipo, se necessario. Facoltativamente, è possibile racchiudere il nome della colonna tra virgolette doppie per una leggibilità senza influire sulla funzionalità. Per altre informazioni, vedere [Cast del tipo di dati di una colonna](-search-sql-castingdatacolumntype.md).

Il valore letterale può essere qualsiasi valore letterale stringa, numerico, esadecimale, booleano o di data, racchiuso tra virgolette singole. Vengono riconosciute solo le corrispondenze esatte e i caratteri jolly vengono ignorati. È anche possibile eseguire il cast del valore letterale a un altro tipo.

## <a name="comparison-operators"></a>Operatori di confronto

Nella tabella seguente vengono descritti gli operatori di confronto supportati.



| Operatore di confronto | Descrizione              |
|---------------------|--------------------------|
| =                   | Uguale a                 |
| != o <>      | Diverso da             |
| >                | Maggiore di             |
| >=               | Maggiore o uguale a |
| <                | Minore di                |
| <=               | Minore o uguale a    |



 

 

In combinazione con l'operatore "=", Windows Search Structured Query Language (SQL) supporta l'uso delle parole chiave BEFORE e AFTER, che specificano se la query deve confrontare i valori di colonna prima o dopo un valore specificato, nell'ordinamento del dizionario.


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

[Funzione DATEADD](-search-sql-dateadd.md)
</dt> <dt>

[Confronti multivalore (ARRAY)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[Predicato NULL](-search-sql-null.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



