---
description: 'Metodo CTransformInputPin.QueryId: il metodo QueryId recupera un identificatore per il pin. Questo metodo implementa il metodo IPin::QueryId.'
ms.assetid: 91fde383-0288-4307-9ca8-e117b6111769
title: Metodo CTransformInputPin.QueryId (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8407e649814fcb12f699c2362f0f89137e941d19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095009"
---
# <a name="ctransforminputpinqueryid-method"></a>Metodo CTransformInputPin.QueryId

Il `QueryId` metodo recupera un identificatore per il pin. Questo metodo implementa il [**metodo IPin::QueryId.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)

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
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | **Argomento puntatore NULL**<br/> |



 

## <a name="remarks"></a>Commenti

L'identificatore pin viene usato per la persistenza del grafico. L'identificatore pin per questa classe è In. Questa classe esegue l'override del comportamento della [**classe CBasePin.**](cbasepin.md) Nella classe **CBasePin** l'identificatore pin corrisponde al nome del pin, specificato nel costruttore della classe. Nella classe **CTransformInputPin** l'identificatore del pin e il nome del pin non sono uguali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




