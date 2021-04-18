---
description: Il metodo Insert aggiunge un oggetto CDeferredCommand alla coda.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: Metodo CCmdQueue. Insert (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bad004641258e29ed42d7142a5b0ab2c0ceb78d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324478"
---
# <a name="ccmdqueueinsert-method"></a>CCmdQueue. Insert (metodo)

Il `Insert` metodo aggiunge un oggetto [**CDeferredCommand**](cdeferredcommand.md) alla coda.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCmd* 
</dt> <dd>

Puntatore all'oggetto **CDeferredCommand** da aggiungere alla coda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK nell'implementazione predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




