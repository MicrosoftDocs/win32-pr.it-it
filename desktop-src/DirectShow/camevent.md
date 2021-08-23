---
description: La classe CAMEvent è un wrapper per gli eventi di reimpostazione manuale e reimpostazione automatica.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: Classe CAMEvent (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea87239628f001feaa82f84ca8c50941b56d3eb99f486934b551e832d1f588c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955530"
---
# <a name="camevent-class"></a>Classe CAMEvent

![Gerarchia di classi camevent](images/util06.png)

La **classe CAMEvent** è un wrapper per gli eventi di reimpostazione manuale e reimpostazione automatica.

Questa classe offre un modo pratico per gestire gli eventi, anziché chiamare funzioni come [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)e [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).



| Variabili membro protette                          | Descrizione                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [**m \_ hEvent**](camevent-m-hevent.md)              | Handle dell'evento.                                                   |
| Metodi pubblici                                      | Descrizione                                                     |
| [**CAMEvent**](camevent-camevent.md)               | Metodo del costruttore.                                             |
| [**~CAMEvent**](camevent--camevent.md)             | Metodo del distruttore.                                              |
| [**Verifica**](camevent-check.md)                     | Controlla se l'evento è impostato, senza blocco.              |
| [**Reset**](camevent-reset.md)                     | Imposta lo stato dell'evento su non associato.                     |
| [**Impostare**](camevent-set.md)                         | Segnala l'evento.                                              |
| [**Attesa**](camevent-wait.md)                       | Si blocca fino a quando l'evento non viene segnalato o fino a quando non si verifica un timeout. |
| Operatori                                           | Descrizione                                                     |
| [**operator HANDLE**](camevent-operator-handle.md) | Recupera l'handle dell'evento.                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

