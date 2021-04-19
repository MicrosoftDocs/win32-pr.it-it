---
description: La classe CAutoLock include una sezione critica per l'ambito di un blocco di codice.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: Classe CAutoLock (Wxutil. h)
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
ms.openlocfilehash: 866ca7164fdaef5a93679da000779c51fb4ddb24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327974"
---
# <a name="cautolock-class"></a>Classe CAutoLock

La `CAutoLock` classe include una sezione critica per l'ambito di un blocco di codice.

Questa classe funziona insieme alla classe [**CCritSec**](ccritsec.md) , che è un wrapper per gli oggetti della sezione critica. Il `CAutoLock` Costruttore blocca la sezione critica e il distruttore lo sblocca. Utilizzando un `CAutoLock` oggetto come variabile locale, è possibile bloccare una sezione critica con la garanzia che tutti i percorsi del codice possano sbloccare la sezione critica.

Nell'esempio di codice seguente viene illustrato come utilizzare questa classe:


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



I metodi di questa classe non sono progettati per essere sottoposti a override.



| Variabili membro protette                 | Descrizione                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [**\_pLock m**](cautolock-m-plock.md)      | Sezione critica per questo blocco.                                  |
| Metodi pubblici                             | Descrizione                                                      |
| [**CAutoLock**](cautolock-cautolock.md)   | Metodo del costruttore. Blocca l'oggetto sezione critica specificato. |
| [**~ CAutoLock**](cautolock--cautolock.md) | Metodo del distruttore. Sblocca l'oggetto sezione critica.          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




