---
description: La classe CRefTime è una classe helper che consente di gestire i tempi di riferimento.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: Classe CRefTime (Reftime. h)
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
ms.openlocfilehash: 01e83520943abafd814425b6ff3fb53f48775627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327926"
---
# <a name="creftime-class"></a>Classe CRefTime

![gerarchia di classi creftime](images/cutil05.png)

La `CRefTime` classe è una classe helper per la gestione dei tempi di riferimento.

Un' *ora di riferimento* è un'unità di tempo rappresentata in unità di 100 nanosecondi. Questa classe condivide lo stesso layout di dati del tipo di dati [**\_ time di riferimento**](reference-time.md) , ma aggiunge alcuni metodi e operatori che forniscono funzioni di confronto, conversione e aritmetica. Per altre informazioni sui tempi di riferimento, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).



| Variabili membro pubblico                                                 | Descrizione                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [**\_ora m**](creftime-m-time.md)                                      | Specifica il valore dell' **\_ ora di riferimento** .              |
| Metodi pubblici                                                          | Descrizione                                           |
| [**CRefTime**](creftime-creftime.md)                                   | Metodo del costruttore.                                   |
| [**Getunits**](creftime-getunits.md)                                   | Recupera l'ora di riferimento in unità 100-nanosecondi. |
| [**Millisecondi**](creftime-millisecs.md)                                 | Converte l'ora di riferimento in millisecondi.          |
| Operatori                                                               | Descrizione                                           |
| [**tempo riferimento operatore \_ ()**](creftime-operator-reference-time-.md) | Esegue il cast dell'oggetto a un tipo di dati **\_ time di riferimento** .  |
| [**operatore =**](creftime-operator-assign.md)                           | Assegna una nuova ora di riferimento.                         |
| [**operatore + =**](creftime-operator-plus-assign.md)                     | Aggiunge due tempi di riferimento.                             |
| [**operatore =**](creftime-operator-minus-assign.md)                    | Sottrae un'ora di riferimento da un'altra.            |



 

## <a name="remarks"></a>Commenti

È possibile che si verifichi un problema con l'utilizzo di questa classe. Se si applica l'operatore + = con un oggetto **CRefTime** come operando sinistro e una variabile di tipo **Long** come operando destro, il compilatore forza l'operando di destra in modo implicito in un oggetto **CRefTime** . Questa coercizione usa il costruttore **CRefTime** che converte i millisecondi in \_ unità di tempo di riferimento. di conseguenza, l'operando destro viene moltiplicato per 10.000:


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



Tuttavia, la stessa operazione non viene eseguita utilizzando l'operatore +:


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Reftime. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




