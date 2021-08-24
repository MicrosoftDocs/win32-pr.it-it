---
description: Il metodo SetActualDataLength imposta la lunghezza dei dati validi nel buffer. Questo metodo implementa il metodo IMediaSample::SetActualDataLength.
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Metodo CMediaSample.SetActualDataLength (Amfilter.h)
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
ms.openlocfilehash: db090ad96f6c53f725aef7864e729b8083bfd1a02b30f0d699d30b5c6f8f71aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634377"
---
# <a name="cmediasamplesetactualdatalength-method"></a>Metodo CMediaSample.SetActualDataLength

Il `SetActualDataLength` metodo imposta la lunghezza dei dati validi nel buffer. Questo metodo implementa il [**metodo IMediaSample::SetActualDataLength.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength)

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

Lunghezza in byte dei dati validi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                             | Descrizione                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Operazione completata.<br/>                                         |
| <dl> <dt>**OVERFLOW DEL \_ \_ BUFFER VFW E \_**</dt> </dl> | *lLen* è maggiore delle dimensioni del buffer allocato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo imposta la [**variabile membro CMediaSample::m \_ lActual.**](cmediasample-m-lactual.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




