---
description: Il metodo GetMediaType recupera il tipo di supporto, se il tipo di supporto è diverso dall'esempio precedente. Questo metodo implementa il metodo IMediaSample::GetMediaType.
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Metodo CMediaSample.GetMediaType (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee7b5464ff2620dbc0247b006dc323232131de3936d2c5e56f2232b67c00ba5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832301"
---
# <a name="cmediasamplegetmediatype-method"></a>Metodo CMediaSample.GetMediaType

Il `GetMediaType` metodo recupera il tipo di supporto, se il tipo di supporto è diverso dall'esempio precedente. Questo metodo implementa il [**metodo IMediaSample::GetMediaType.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppMediaType* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore a una [**struttura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Se il tipo di supporto non è stato modificato rispetto all'esempio precedente, *\* ppMediaType* viene impostato su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Il tipo di supporto non è stato modificato rispetto all'esempio precedente.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                                     |



 

## <a name="remarks"></a>Commenti

Al termine del tipo di supporto, liberare il blocco di memoria chiamando la [**funzione dell'utilità DeleteMediaType.**](deletemediatype.md)

La [**variabile membro CMediaSample::m \_ pMediaType**](cmediasample-m-pmediatype.md) specifica il tipo di supporto. La variabile membro [**CMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) specifica se il tipo di supporto è stato modificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




