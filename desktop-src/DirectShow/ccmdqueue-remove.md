---
description: Il metodo Remove rimuove l'oggetto CDeferredCommand dalla coda.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Metodo CCmdQueue. Remove (Winutil. h)
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
ms.openlocfilehash: ef9f45c8176645c5937b5ad74045130ff8cd8c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332767"
---
# <a name="ccmdqueueremove-method"></a>Metodo CCmdQueue. Remove

Il `Remove` metodo rimuove l'oggetto [**CDeferredCommand**](cdeferredcommand.md) dalla coda.

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

Puntatore all'oggetto **CDeferredCommand** da rimuovere dalla coda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce VFW \_ E \_ non \_ trovato se l'oggetto non viene trovato nella coda. In caso contrario, restituisce S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




