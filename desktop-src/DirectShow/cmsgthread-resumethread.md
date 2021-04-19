---
description: "Usa la funzione ResumeThread di Microsoft Win32 per continuare l'operazione del thread di lavoro dopo una chiamata precedente alla funzione membro CMsgThread:: SuspendThread."
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: Metodo CMsgThread. ResumeThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e0a20bb60f4a10a06ef50f58c449496cae8050d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333318"
---
# <a name="cmsgthreadresumethread-method"></a>CMsgThread. ResumeThread, metodo

Usa la funzione **ResumeThread** di Microsoft Win32 per continuare l'operazione del thread di lavoro dopo una chiamata precedente alla funzione membro [**CMsgThread:: SuspendThread**](cmsgthread-suspendthread.md) .

## <a name="syntax"></a>Sintassi


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se la funzione membro ha esito positivo, il valore restituito è il conteggio di sospensione precedente del thread. Se la funzione membro ha esito negativo, il valore restituito è 0xFFFFFFFF. Per ottenere informazioni estese sull'errore, chiamare la funzione **GetLastError** di Microsoft Win32.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




