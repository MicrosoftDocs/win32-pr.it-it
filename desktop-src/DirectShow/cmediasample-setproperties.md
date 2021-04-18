---
description: "Il metodo seproperties imposta le proprietà dell'esempio. Questo metodo implementa il metodo IMediaSample2:: SetValue."
ms.assetid: 639aedf5-0c21-4578-b336-91859e40f3be
title: Metodo CMediaSample. seproperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5e6ef3c3839825586bf47259cf44783d167f503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324924"
---
# <a name="cmediasamplesetproperties-method"></a>Metodo CMediaSample. seproperties

Il `SetProperties` metodo imposta le proprietà dell'esempio. Questo metodo implementa il metodo [**IMediaSample2::**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) SetValue.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProperties(
         DWORD cbProperties,
   const BYTE  *pbProperties
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cbProperties* 
</dt> <dd>

Lunghezza dei dati della proprietà da impostare, in byte.

</dd> <dt>

*pbProperties* 
</dt> <dd>

Puntatore a un buffer di dimensioni *cbProperties*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argomento non valido<br/>          |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente<br/>       |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Argomento puntatore **null**<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




