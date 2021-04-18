---
description: Il metodo GetEvent recupera un handle di evento, che viene usato per segnalare una modifica nel tempo di notifica successivo.
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: Metodo CAMSchedule. GetEvent (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 360a4b88c8c03d2f04ad55bc65eebf6be3797c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328360"
---
# <a name="camschedulegetevent-method"></a>Metodo CAMSchedule. GetEvent

Il `GetEvent` metodo recupera un handle di evento, che viene usato per segnalare una modifica nel tempo di notifica successivo.

## <a name="syntax"></a>Sintassi


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un handle a un evento.

## <a name="remarks"></a>Commenti

Se il successivo avviso cambia in altre parole, se viene aggiunta una nuova richiesta di notifica all'inizio dell'elenco, l'utilità di pianificazione segnala l'evento. L'orologio deve chiamare il metodo [**CAMSchedule:: Advise**](camschedule-advise.md) per determinare il tempo di notifica successivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dsschedule. h (include Streams. h)</dt> </dl>                                                                                |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




