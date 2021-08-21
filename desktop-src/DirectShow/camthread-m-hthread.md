---
description: Handle per il thread.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: Membro CAMThread::m_hThread (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7293a97373a53d102887e5958c4296aff3dcfe3d392c80492ed773af62a8f11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158912"
---
# <a name="camthreadm_hthread-member"></a>Membro CAMThread::m \_ hThread

Handle per il thread.

## <a name="syntax"></a>Sintassi


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a>Osservazioni

Questa variabile viene inizializzata come **NULL.** Il [**metodo CAMThread::Create**](camthread-create.md) imposta questa variabile sull'handle del thread. Per determinare se il thread esiste, chiamare il [**metodo CAMThread::ThreadExists.**](camthread-threadexists.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




