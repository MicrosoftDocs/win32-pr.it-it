---
description: 'Metodo CTransformOutputPin.QueryId: il metodo QueryId recupera un identificatore per il pin. Questo metodo implementa il metodo IPin::QueryId.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: Metodo CTransformOutputPin.QueryId (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56da848f3829f56d93d7d0383dc7fdc1ec6d5bfd995c2c74507d05eb13801fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584811"
---
# <a name="ctransformoutputpinqueryid-method"></a>Metodo CTransformOutputPin.QueryId

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

L'identificatore pin viene usato per la persistenza del grafico. L'identificatore pin per questa classe è Out. Questa classe esegue l'override del comportamento della [**classe CBasePin.**](cbasepin.md) Nella classe **CBasePin** l'identificatore pin corrisponde al nome del pin, specificato nel costruttore della classe. Nella classe **CTransformInputPin** l'identificatore del pin e il nome del pin non sono uguali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




