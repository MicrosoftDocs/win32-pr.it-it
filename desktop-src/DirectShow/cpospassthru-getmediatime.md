---
description: Il metodo GetMediaTime recupera i timestamp nell'esempio corrente.
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Metodo CPosPassThru. GetMediaTime (Ctlutil. h)
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
ms.openlocfilehash: b2748d986f121a38041155dcd43f13a647916486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325514"
---
# <a name="cpospassthrugetmediatime-method"></a>CPosPassThru. GetMediaTime, metodo

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

Puntatore a una variabile che riceve l'ora di inizio, in unità del formato dell'ora corrente.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di fine, in unità del formato dell'ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E ha \_ esito negativo.

## <a name="remarks"></a>Commenti

Eseguire l'override di questo metodo se il filtro memorizza nella cache i timestamp sugli esempi ricevuti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




