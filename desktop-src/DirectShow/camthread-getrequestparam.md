---
description: Il metodo GetRequestParam recupera la richiesta più recente.
ms.assetid: f5bf4935-29ea-45b9-a57e-9fdcd9cde20a
title: Metodo CAMThread.GetRequestParam (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestParam
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c511fdb68bb6ee9372530d9e19290342a57fbcc5817148613d20fd8afe029b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384921"
---
# <a name="camthreadgetrequestparam-method"></a>Metodo CAMThread.GetRequestParam

Il `GetRequestParam` metodo recupera la richiesta più recente.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore del parametro passato più di recente al [**metodo CAMThread::CallWorker.**](camthread-callworker.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




