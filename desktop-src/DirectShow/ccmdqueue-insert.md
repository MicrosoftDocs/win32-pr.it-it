---
description: Il metodo Insert aggiunge un oggetto CDeferredCommand alla coda.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: Metodo CCmdQueue.Insert (Winutil.h)
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
ms.openlocfilehash: 90e2bab4a3545e8a02315155ad4a477511ecf961c93a511ccba268b7fde7dd0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757321"
---
# <a name="ccmdqueueinsert-method"></a>Metodo CCmdQueue.Insert

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

Puntatore **all'oggetto CDeferredCommand** da aggiungere alla coda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK nell'implementazione predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




