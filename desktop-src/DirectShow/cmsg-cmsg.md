---
description: Costruisce un oggetto CMsg.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: Costruttore CMsg. CMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg.CMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b26a9572b51d4a476b70c3dd7ddae8c896a4d648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328839"
---
# <a name="cmsgcmsg-constructor"></a>Costruttore CMsg. CMsg

Costruisce un oggetto [**CMsg**](cmsg.md) .

## <a name="syntax"></a>Sintassi


```C++
CMsg(
   UINT     u,
   DWORD    dw,
   LPVOID   lp,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*u* 
</dt> <dd>

Codice della richiesta, definito dal client della classe thread e riconosciuto dalla funzione thread di lavoro sottoposta a override.

</dd> <dt>

*dw* 
</dt> <dd>

Parametro del flag per il codice della richiesta.

</dd> <dt>

*LP* 
</dt> <dd>

Puntatore ai dati richiesti dal thread di lavoro come parametri o valori restituiti. Questi dati non devono essere basati su stack, in quanto verrà fatto riferimento a un po' di tempo dopo il completamento dell'operazione di Accodamento.

</dd> <dt>

*pEvent* 
</dt> <dd>

Puntatore all'oggetto evento che un thread di lavoro può segnalare per indicare il completamento dell'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa funzione membro contiene una richiesta di intervento di un thread di lavoro di [**CMsgThread**](cmsgthread.md) . Tutti i parametri vengono passati alla funzione thread di lavoro come parametri quando il messaggio viene elaborato. I significati dei parametri sono definiti dalla funzione client che chiama il thread di lavoro e la classe derivata che fornisce la funzione di esecuzione del thread di lavoro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




