---
description: Il metodo SetMediaType imposta il tipo di supporto per l'esempio. Questo metodo implementa il metodo IMediaSample::SetMediaType.
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: Metodo CMediaSample.SetMediaType (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e7059e0d9b2d91b6a938c67445f185a2c9be0daf5831c30b235918ab7820b1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832171"
---
# <a name="cmediasamplesetmediatype-method"></a>Metodo CMediaSample.SetMediaType

Il `SetMediaType` metodo imposta il tipo di supporto per l'esempio. Questo metodo implementa il [**metodo IMediaSample::SetMediaType.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMediaType(
   AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaType* 
</dt> <dd>

Puntatore a una [**struttura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione riuscita<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo imposta la variabile membro [**CMediaSample::m \_ pMediaType,**](cmediasample-m-pmediatype.md) che specifica il tipo di supporto, e la variabile membro [**CMediaSample::m \_ dwFlags,**](cmediasample-m-dwflags.md) che specifica se il tipo di supporto è stato modificato.

Questo metodo crea una copia della struttura AM \_ MEDIA \_ TYPE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




