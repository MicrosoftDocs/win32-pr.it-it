---
description: "Il metodo GetMediaType Recupera il tipo di supporto, se il tipo di supporto è diverso rispetto all'esempio precedente. Questo metodo implementa il metodo IMediaSample:: GetMediaType."
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Metodo CMediaSample. GetMediaType (Amfilter. h)
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
ms.openlocfilehash: 9a067494d6236b824ef8fbbcb583ad50503297b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326405"
---
# <a name="cmediasamplegetmediatype-method"></a>CMediaSample. GetMediaType, metodo

Il `GetMediaType` metodo recupera il tipo di supporto, se il tipo di supporto è diverso rispetto all'esempio precedente. Questo metodo implementa il metodo [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .

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

Indirizzo di una variabile che riceve un puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Se il tipo di supporto non è stato modificato rispetto all'esempio precedente, *\* ppMediaType* è impostato su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | Il tipo di supporto non è stato modificato rispetto all'esempio precedente.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                                                 |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                                     |



 

## <a name="remarks"></a>Commenti

Al termine del tipo di supporto, liberare il blocco di memoria chiamando la funzione di utilità [**DeleteMediaType**](deletemediatype.md) .

La variabile membro [**CMediaSample:: m \_ pMediaType**](cmediasample-m-pmediatype.md) specifica il tipo di supporto. La variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) specifica se il tipo di supporto è stato modificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




