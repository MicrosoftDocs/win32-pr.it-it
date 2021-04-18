---
description: La classe CAMMsgEvent è un wrapper per oggetti evento che eseguono l'elaborazione dei messaggi.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: Classe CAMMsgEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ebac7aae11f7a7b7d6b846e262e93b5759210b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329268"
---
# <a name="cammsgevent-class"></a>Classe CAMMsgEvent

![gerarchia di classi cammsgevent](images/util06.png)

La `CAMMsgEvent` classe è un wrapper per gli oggetti evento che eseguono l'elaborazione dei messaggi.

Questa classe deriva dall'oggetto [**CAMEvent**](camevent.md) . Viene aggiunto un metodo, [**CAMMsgEvent:: WaitMsg**](cammsgevent-waitmsg.md), che invia i messaggi in ingresso in attesa.



| Metodi pubblici                                 | Descrizione                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [**CAMMsgEvent**](cammsgevent-cammsgevent.md) | Costruttore.                                                         |
| [**WaitMsg**](cammsgevent-waitmsg.md)         | Attende la segnalazione dell'evento, durante l'invio dei messaggi inviati. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




