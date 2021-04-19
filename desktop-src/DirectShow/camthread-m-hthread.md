---
description: Handle per il thread.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'Membro CAMThread:: m_hThread (Wxutil. h)'
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
ms.openlocfilehash: e83dd225da0c3673f9c7f423e0bf56da7431b097
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333380"
---
# <a name="camthreadm_hthread-member"></a>Membro hThread di CAMThread:: m \_

Handle per il thread.

## <a name="syntax"></a>Sintassi


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a>Osservazioni

Questa variabile è inizializzata come **null**. Il metodo [**CAMThread:: create**](camthread-create.md) imposta questa variabile sull'handle del thread. Per determinare se il thread esiste, chiamare il metodo [**CAMThread:: ThreadExists**](camthread-threadexists.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




