---
description: "Il metodo SetMediaType imposta il tipo di supporto per l'esempio. Questo metodo implementa il metodo IMediaSample:: SetMediaType."
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: Metodo CMediaSample. SetMediaType (Amfilter. h)
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
ms.openlocfilehash: f46fc4e8c348b1d03d19e815f658e0f637b8f880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325309"
---
# <a name="cmediasamplesetmediatype-method"></a>CMediaSample. SetMediaType, metodo

Il `SetMediaType` metodo imposta il tipo di supporto per l'esempio. Questo metodo implementa il metodo [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) .

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

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione riuscita<br/>             |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo imposta la variabile membro [**CMediaSample:: m \_ pMediaType**](cmediasample-m-pmediatype.md) , che specifica il tipo di supporto e la variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) , che specifica se il tipo di supporto è stato modificato.

Questo metodo crea una copia della struttura del \_ tipo di supporto am \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




