---
description: Il metodo Remove rimuove l'oggetto CDeferredCommand dalla coda.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Metodo CCmdQueue.Remove (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6d0b0a4b416c5adb97b1a9efba1fbd5f6142b0e0fb761c6d4c0b277ac0cda7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954580"
---
# <a name="ccmdqueueremove-method"></a>Metodo CCmdQueue.Remove

Il `Remove` metodo rimuove [**l'oggetto CDeferredCommand**](cdeferredcommand.md) dalla coda.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCmd* 
</dt> <dd>

Puntatore **all'oggetto CDeferredCommand** da rimuovere dalla coda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce VFW \_ E NOT FOUND se \_ \_ l'oggetto non viene trovato nella coda. In caso contrario, restituisce S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




