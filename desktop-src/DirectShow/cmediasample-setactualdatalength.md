---
description: 'Il metodo SetActualDataLength imposta la lunghezza dei dati validi nel buffer. Questo metodo implementa il metodo IMediaSample:: SetActualDataLength.'
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Metodo CMediaSample. SetActualDataLength (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325321"
---
# <a name="cmediasamplesetactualdatalength-method"></a>CMediaSample. SetActualDataLength, metodo

Il `SetActualDataLength` metodo imposta la lunghezza dei dati validi nel buffer. Questo metodo implementa il metodo [**IMediaSample:: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lLen* 
</dt> <dd>

Lunghezza dei dati validi, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                             | Descrizione                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Esito positivo.<br/>                                         |
| <dl> <dt>**\_overflow del \_ buffer \_ E VFW**</dt> </dl> | *lLen* è maggiore della dimensione del buffer allocata.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo imposta la variabile membro [**CMediaSample:: m \_ lActual**](cmediasample-m-lactual.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




