---
description: Usa la funzione SuspendThread di Microsoft Win32 per sospendere l'operazione di un thread in esecuzione.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: Metodo CMsgThread. SuspendThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69190015104d712864965e757d82afbdcc852884
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333312"
---
# <a name="cmsgthreadsuspendthread-method"></a>CMsgThread. SuspendThread, metodo

Usa la funzione **SuspendThread** di Microsoft Win32 per sospendere l'operazione di un thread in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se la funzione membro ha esito positivo, il valore restituito è il conteggio di sospensione precedente del thread. Se la funzione membro ha esito negativo, il valore restituito è 0xFFFFFFFF. Per ottenere informazioni estese sull'errore, chiamare la funzione **GetLastError** di Microsoft Win32.

## <a name="remarks"></a>Commenti

Il thread client chiama questa funzione membro per sospendere l'operazione del thread di lavoro. Il thread di lavoro rimane sospeso e non verrà eseguito fino a quando non viene effettuata una chiamata aggiuntiva alla funzione membro [**CMsgThread:: ResumeThread**](cmsgthread-resumethread.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




