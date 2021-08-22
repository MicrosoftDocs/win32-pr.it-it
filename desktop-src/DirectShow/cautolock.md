---
description: La classe CAutoLock contiene una sezione critica per l'ambito di un blocco di codice.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: Classe CAutoLock (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b046111e3a7e22fcf9e380fae09bb2d2007a583e49c0507b8e214142505fe02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661703"
---
# <a name="cautolock-class"></a>Classe CAutoLock

La `CAutoLock` classe contiene una sezione critica per l'ambito di un blocco di codice.

Questa classe funziona in combinazione con la [**classe CCritSec,**](ccritsec.md) che è un wrapper per gli oggetti sezione critica. Il `CAutoLock` costruttore blocca la sezione critica e il distruttore la sblocca. Usando un oggetto come variabile locale, è possibile bloccare una sezione critica con la garanzia che tutti i percorsi di codice `CAutoLock` sbloccheranno la sezione critica.

L'esempio di codice seguente illustra come usare questa classe:


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



I metodi in questa classe non sono progettati per l'override.



| Variabili membro protette                 | Descrizione                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [**m \_ pLock**](cautolock-m-plock.md)      | Sezione critica per questo blocco.                                  |
| Metodi pubblici                             | Descrizione                                                      |
| [**CAutoLock**](cautolock-cautolock.md)   | Metodo del costruttore. Blocca l'oggetto sezione critica specificato. |
| [**~CAutoLock**](cautolock--cautolock.md) | Metodo del distruttore. Sblocca l'oggetto sezione critica.          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




