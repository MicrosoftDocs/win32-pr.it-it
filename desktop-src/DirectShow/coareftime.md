---
description: La classe COARefTime converte i tempi di riferimento tra i secondi e le unità 100-nanosecondi.
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: Classe COARefTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851495d69a1e34bd1723c20f88dc4bb86b7a8025
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324471"
---
# <a name="coareftime-class"></a>Classe COARefTime

![gerarchia di classi coareftime](images/cutil05.png)

La `COARefTime` classe converte i tempi di riferimento tra i secondi e le unità di 100 nanosecondi.

Questa classe esegue la conversione tra tempi di riferimento compatibili con l'automazione e i tempi di riferimento compatibili con C/C++. Le interfacce compatibili con l'automazione usano valori **doppi** per rappresentare il tempo in secondi. Altre interfacce usano valori **LONGLONG** a 64 bit per rappresentare l'ora in unità 100-nanosecondi. Per questi valori sono definiti i tipi seguenti:

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

I filtri possono utilizzare la `COARefTime` classe per eseguire la conversione tra i due formati. Questa classe è derivata dalla classe [**CRefTime**](creftime.md) .



| Metodi pubblici                                          | Descrizione                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [**COARefTime**](coareftime-coareftime.md)             | Metodo del costruttore.                                                   |
| Operatori                                               | Descrizione                                                           |
| [**doppio**](coareftime-double.md)                     | Converte l'ora di riferimento in un valore **Double** .                    |
| [**\_ora riferimento**](coareftime-reference-time.md)    | Esegue il cast dell'oggetto a un valore di **\_ ora di riferimento** .                      |
| [**operatore =**](coareftime-operator-assign.md)        | Assegna una nuova ora di riferimento.                                         |
| [**operatore = =**](coareftime-operator-eq.md)           | Verifica l'uguaglianza tra due tempi di riferimento.                       |
| [**operatore! =**](cmediatype-operator-neq.md)          | Verifica la disuguaglianza tra due tempi di riferimento.                     |
| [**operatore <**](coareftime-operator-lt.md)         | Verifica se un tempo di riferimento è minore di un altro.                     |
| [**operatore >**](coareftime-operator-gt.md)         | Verifica se un tempo di riferimento è maggiore di un altro.                  |
| [**operatore <=**](coareftime-operator-lteq.md)      | Verifica se un'ora di riferimento è minore o uguale a un'altra.         |
| [**operatore >=**](coareftime-operator-gteq.md)      | Verifica se un'ora di riferimento è maggiore o uguale a un'altra.      |
| [**operatore +**](coareftime-operator-plus.md)          | Aggiunge due tempi di riferimento.                                             |
| [* * operatore * *](coareftime-operator-minus.md)         | Sottrae un'ora di riferimento da un'altra.                            |
| [**operatore + =**](coareftime-operator-plus-assign.md)  | Aggiunge due tempi di riferimento e assegna il risultato a questo oggetto.      |
| [**operatore =**](coareftime-operator-minus-assign.md) | Sottrae due tempi di riferimento e assegna il risultato a questo oggetto. |
| [**operatore \***](coareftime-operator-mult.md)         | Moltiplica un'ora di riferimento per un valore.                               |
| [**operatore**](coareftime-operator-div.md)           | Divide un'ora di riferimento per un valore.                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




