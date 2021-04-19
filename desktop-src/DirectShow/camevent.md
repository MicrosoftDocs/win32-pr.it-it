---
description: La classe CAMEvent è un wrapper per gli eventi di reimpostazione manuale e ripristino automatico.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: Classe CAMEvent (Wxutil. h)
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
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326578"
---
# <a name="camevent-class"></a>Classe CAMEvent

![gerarchia di classi CamEvent](images/util06.png)

La classe **CAMEvent** è un wrapper per gli eventi di reimpostazione manuale e ripristino automatico.

Questa classe fornisce un modo pratico per gestire gli eventi, anziché chiamare funzioni quali [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)e [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).



| Variabili membro protette                          | Descrizione                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [**\_hEvent m**](camevent-m-hevent.md)              | Handle di evento.                                                   |
| Metodi pubblici                                      | Descrizione                                                     |
| [**CAMEvent**](camevent-camevent.md)               | Metodo del costruttore.                                             |
| [**~ CAMEvent**](camevent--camevent.md)             | Metodo del distruttore.                                              |
| [**Controllo**](camevent-check.md)                     | Verifica se l'evento è impostato, senza bloccarsi.              |
| [**Reset**](camevent-reset.md)                     | Imposta lo stato dell'evento su non segnalato.                     |
| [**Set**](camevent-set.md)                         | Segnala l'evento.                                              |
| [**Attesa**](camevent-wait.md)                       | Si blocca fino a quando l'evento non viene segnalato o fino a quando non si verifica un timeout. |
| Operatori                                           | Descrizione                                                     |
| [**HANDLE operatore**](camevent-operator-handle.md) | Recupera l'handle dell'evento.                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

