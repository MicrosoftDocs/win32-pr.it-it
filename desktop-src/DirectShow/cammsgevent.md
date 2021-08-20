---
description: La classe CAMMsgEvent è un wrapper per gli oggetti evento che eseguono l'elaborazione dei messaggi.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: Classe CAMMsgEvent (Wxutil.h)
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
ms.openlocfilehash: c7c4d3c8268f06e81d1bd1a5285f7e4785459889397ccf249bbde7f0dd627f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955436"
---
# <a name="cammsgevent-class"></a>Classe CAMMsgEvent

![Gerarchia di classi cammsgevent](images/util06.png)

La `CAMMsgEvent` classe è un wrapper per gli oggetti evento che eseguono l'elaborazione dei messaggi.

Questa classe deriva [**dall'oggetto CAMEvent.**](camevent.md) Aggiunge un metodo, [**CAMMsgEvent::WaitMsg,**](cammsgevent-waitmsg.md)che invia i messaggi in ingresso durante l'attesa.



| Metodi pubblici                                 | Descrizione                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [**CAMMsgEvent**](cammsgevent-cammsgevent.md) | Costruttore.                                                         |
| [**WaitMsg**](cammsgevent-waitmsg.md)         | Attende che l'evento sia segnalato durante l'invio dei messaggi inviati. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




