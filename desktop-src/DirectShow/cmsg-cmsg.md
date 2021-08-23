---
description: Costruisce un oggetto CMsg.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: Costruttore CMsg.CMsg (Msgthrd.h)
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
ms.openlocfilehash: f921c96ae185d8993002c84a09b4efb8bc5977104c274de3a2ffc964a093f1a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831901"
---
# <a name="cmsgcmsg-constructor"></a>Costruttore CMsg.CMsg

Costruisce un [**oggetto CMsg.**](cmsg.md)

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

Codice di richiesta, definito dal client della classe di thread e riconosciuto dalla funzione del thread di lavoro sottoposta a override.

</dd> <dt>

*dw* 
</dt> <dd>

Parametro flag per il codice della richiesta.

</dd> <dt>

*Lp* 
</dt> <dd>

Puntatore ai dati richiesti dal thread di lavoro come parametri o valori restituiti. Questi dati non devono essere basati su stack, in quanto vi verrà fatto riferimento qualche volta dopo aver completato l'operazione di accodamento.

</dd> <dt>

*Pevent* 
</dt> <dd>

Puntatore all'oggetto evento che un thread di lavoro può segnalare per indicare il completamento dell'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa funzione membro contiene una richiesta per un thread di lavoro [**CMsgThread**](cmsgthread.md) su cui agire. Tutti i parametri vengono passati alla funzione del thread di lavoro come parametri quando questo messaggio viene elaborato. I significati dei parametri sono definiti dalla funzione client che chiama il thread di lavoro e dalla classe derivata che fornisce la funzione di esecuzione del thread di lavoro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




