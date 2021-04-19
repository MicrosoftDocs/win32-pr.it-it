---
description: La funzione WaitDispatchingMessages attende che un oggetto venga segnalato, durante l'invio dei messaggi della finestra.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: Funzione WaitDispatchingMessages (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e509a081243f28293dc2d8abf8311f69eaf9a44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326776"
---
# <a name="waitdispatchingmessages-function"></a>WaitDispatchingMessages (funzione)

La `WaitDispatchingMessages` funzione attende la segnalazione di un oggetto, durante l'invio dei messaggi della finestra.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hObject* 
</dt> <dd>

Handle dell'oggetto da attendere.

</dd> <dt>

*dwWait* 
</dt> <dd>

Intervallo di timeout, in millisecondi.

</dd> <dt>

*HWND* 
</dt> <dd>

Handle facoltativo per una finestra.

</dd> <dt>

*uMsg* 
</dt> <dd>

Messaggio finestra facoltativo che specifica un messaggio da inviare.

</dd> <dt>

*hEvent* 
</dt> <dd>

Handle facoltativo per un evento da attendere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore dalla funzione **WaitForMultipleObjects** .

## <a name="remarks"></a>Commenti

Se un oggetto è proprietario di una finestra, deve inviare messaggi della finestra durante l'attesa. Questa funzione consente all'oggetto di attendere un evento, un semaforo o un altro oggetto di esclusione reciproca durante l'invio dei messaggi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper varie](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




