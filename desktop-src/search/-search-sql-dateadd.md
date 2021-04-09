---
description: La funzione DATEADD esegue calcoli di data e ora per le proprietà corrispondenti con tipi di dati. Utilizzare la funzione DATEADD per ottenere le date e le ore in un intervallo di tempo specificato prima del presente.
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: Funzione DATEADD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0b193e75ec644eb3312a61c723edeac43ee264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128550"
---
# <a name="dateadd-function"></a>Funzione DATEADD

La funzione DATEADD esegue calcoli di data e ora per le proprietà corrispondenti con tipi di dati. Utilizzare la funzione DATEADD per ottenere le date e le ore in un intervallo di tempo specificato prima del presente.

## <a name="syntax"></a>Sintassi


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a>Argomenti

*DateTimeUnits*

Specifica le unità del parametro *DateTime* : anno, trimestre, mese, settimana, giorno, ora, minuto o secondo. Questo valore fa distinzione tra maiuscole e minuscole e le virgolette non sono necessarie intorno al parametro.

*OffsetValue*

Specifica l'offset dell'ora, nelle unità specificate dal parametro *DateTimeUnits* . **OffsetValue** deve essere un numero intero negativo. I valori positivi non sono supportati.

*DateTime*

Specifica un timestamp da cui calcolare l'offset. Non può essere un valore letterale di data. Deve essere GETGMTDATE o il risultato di un'altra funzione DATEADD.

## <a name="remarks"></a>Commenti

La funzione DATEADD può essere utilizzata solo nei confronti di valori letterali e solo sul lato destro dell'operatore di confronto.

La funzione GETGMTDATE restituisce la data e l'ora correnti nell'ora di Greenwich (GMT). Tenere presente che questo valore potrebbe non corrispondere all'ora locale del computer.

Non usare l'operatore di confronto uguale a (=) perché la rappresentazione temporale interna può produrre errori di arrotondamento che generano risultati di corrispondenza imprevisti.

È possibile utilizzare più funzioni DATEADD per combinare unità di offset.

### <a name="examples"></a>Esempio

La clausola WHERE di esempio seguente corrisponde ai documenti modificati negli ultimi cinque giorni:


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



La clausola WHERE di esempio seguente corrisponde ai documenti modificati negli ultimi due giorni e quattro ore:


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Confronto di valori letterali](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Confronti multivalore (matrice)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



