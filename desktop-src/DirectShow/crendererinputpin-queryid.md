---
description: Il metodo QueryId recupera l'identificatore pin. Questo metodo esegue l'override del metodo CBasePin::QueryId.
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: Metodo CRendererInputPin.QueryId (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 732bf7aa6d0d247c93c0334db48b86bccd2ac15715dd2da9a4d60a0d315966bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054573"
---
# <a name="crendererinputpinqueryid-method"></a>Metodo CRendererInputPin.QueryId

Il `QueryId` metodo recupera l'identificatore pin. Questo metodo esegue l'override [**del metodo CBasePin::QueryId.**](cbasepin-queryid.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Id* 
</dt> <dd>

Riceve una stringa contenente l'identificatore pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente<br/>       |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | **Argomento puntatore NULL**<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo alloca la stringa di caratteri wide "In" e la assegna al *parametro Id.* Il chiamante deve liberare la memoria allocata usando la **funzione CoTaskMemFree.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 




