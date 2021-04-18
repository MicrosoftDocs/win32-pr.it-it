---
description: Il metodo CheckRequest controlla se è presente una richiesta, senza blocco.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Metodo CAMThread. CheckRequest (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a004e0f5303cf6702c03e78c292a6a2d832a489
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328273"
---
# <a name="camthreadcheckrequest-method"></a>CAMThread. CheckRequest, metodo

Il `CheckRequest` metodo verifica se è presente una richiesta, senza blocco.

## <a name="syntax"></a>Sintassi


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pParam* 
</dt> <dd>

Puntatore a una variabile che riceve il valore passato nell'ultima chiamata al metodo [**CAMThread:: CallWorker**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se è presente una richiesta in sospeso; in caso contrario, **false** .

## <a name="remarks"></a>Commenti

Questo metodo è una versione non di blocco del metodo [**CAMThread:: GetRequest**](camthread-getrequest.md) .

Se un altro thread è in attesa di una chiamata a CallWorker, questo metodo recupera il parametro request e restituisce **true**. In caso contrario, restituisce **false**. Se il metodo restituisce **true**, chiamare il metodo [**CAMThread:: Reply**](camthread-reply.md) per rilasciare il thread richiedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




