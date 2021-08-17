---
description: La classe CRefTime è una classe helper per la gestione dei tempi di riferimento.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: Classe CRefTime (Reftime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d8f9d30b057c1c011dcbff1b7d8c88e9183d50ca1fc2b7dd046b79fe8279d37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953956"
---
# <a name="creftime-class"></a>Classe CRefTime

![gerarchia di classi creftime](images/cutil05.png)

La `CRefTime` classe è una classe helper per la gestione dei tempi di riferimento.

Un *tempo di riferimento* è un'unità di tempo rappresentata in unità di 100 nanosecondi. Questa classe condivide lo stesso layout di dati del tipo di dati [**REFERENCE \_ TIME,**](reference-time.md) ma aggiunge alcuni metodi e operatori che forniscono funzioni di confronto, conversione e aritmetica. Per altre informazioni sui tempi di riferimento, [vedere Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).



| Variabili membro pubbliche                                                 | Descrizione                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [**m \_ time**](creftime-m-time.md)                                      | Specifica il valore **REFERENCE \_ TIME.**              |
| Metodi pubblici                                                          | Descrizione                                           |
| [**CRefTime**](creftime-creftime.md)                                   | Metodo del costruttore.                                   |
| [**GetUnits**](creftime-getunits.md)                                   | Recupera l'ora di riferimento in unità di 100 nanosecondi. |
| [**Millisecs**](creftime-millisecs.md)                                 | Converte il tempo di riferimento in millisecondi.          |
| Operatori                                                               | Descrizione                                           |
| [**operatore REFERENCE \_ TIME()**](creftime-operator-reference-time-.md) | Esegue il cast dell'oggetto a un **tipo di dati REFERENCE \_ TIME.**  |
| [**operator=**](creftime-operator-assign.md)                           | Assegna una nuova ora di riferimento.                         |
| [**operator+=**](creftime-operator-plus-assign.md)                     | Aggiunge due tempi di riferimento.                             |
| [**operator =**](creftime-operator-minus-assign.md)                    | Sottrae un'ora di riferimento da un'altra.            |



 

## <a name="remarks"></a>Commenti

L'uso di questa classe può insidie. Se si applica l'operatore += con un oggetto **CRefTime** come operando sinistro e una variabile di tipo **LONG** come operando destro, il compilatore forza in modo implicito l'operando destro in un **oggetto CRefTime.** Questa coercizione usa il costruttore **CRefTime** che converte i millisecondi in unità REFERENCE TIME. Di conseguenza, l'operando destro viene moltiplicato per \_ 10.000:


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



Tuttavia, la stessa cosa non avviene usando l'operatore +:


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Reftime.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




