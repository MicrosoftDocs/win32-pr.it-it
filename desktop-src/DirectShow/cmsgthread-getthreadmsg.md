---
description: Recupera un oggetto CMsg in coda contenente una richiesta.
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: Metodo CMsgThread. GetThreadMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1851ac36590992aca6fa4413119be1df7427bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328829"
---
# <a name="cmsgthreadgetthreadmsg-method"></a>CMsgThread. GetThreadMsg, metodo

Recupera un oggetto [**CMsg**](cmsg.md) in coda contenente una richiesta.

## <a name="syntax"></a>Sintassi


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*msg* 
</dt> <dd>

Puntatore a un oggetto [**CMsg**](cmsg.md) allocato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione membro viene chiamata dalla funzione [**ThreadProc**](camthread-threadproc.md) privata del thread di lavoro per recuperare la funzione membro successiva. Il parametro *msg* deve puntare a un oggetto [**CMsg**](cmsg.md) allocato che verrà compilato con i parametri della richiesta successiva nella coda. Se non sono presenti richieste in coda, questa funzione membro si blocca fino a quando la richiesta successiva non viene accodata (tramite una chiamata alla funzione membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




