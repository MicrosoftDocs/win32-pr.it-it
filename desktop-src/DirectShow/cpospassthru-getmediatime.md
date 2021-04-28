---
description: "Metodo CPosPassThru.GetMediaTime: il metodo GetMediaTime recupera i timestamp nell'esempio corrente."
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Metodo CPosPassThru.GetMediaTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 328a0ae09c80a687863cfedb994f5a80cebebf14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095259"
---
# <a name="cpospassthrugetmediatime-method"></a>Metodo CPosPassThru.GetMediaTime

Il `GetMediaTime` metodo recupera i timestamp nell'esempio corrente.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStartTime* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di inizio, in unità del formato di ora corrente.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di fine, in unità del formato di ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ FAIL.

## <a name="remarks"></a>Commenti

Eseguire l'override di questo metodo se il filtro memorizza nella cache i timestamp nei campioni ricevuti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




