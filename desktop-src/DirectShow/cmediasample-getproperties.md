---
description: Il metodo GetProperties recupera le proprietà dell'esempio. Questo metodo implementa il metodo IMediaSample2::GetProperties.
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: Metodo CMediaSample.GetProperties (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 856da0c73f3dd93d0c660f55aa0a9de35d87ab1b270df2179d7ad0b520e6d0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074025"
---
# <a name="cmediasamplegetproperties-method"></a>Metodo CMediaSample.GetProperties

Il `GetProperties` metodo recupera le proprietà dell'esempio. Questo metodo implementa il [**metodo IMediaSample2::GetProperties.**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cbProperties* 
</dt> <dd>

Lunghezza in byte dei dati della proprietà da recuperare.

</dd> <dt>

*proprietà pb* 
</dt> <dd>

Puntatore a un buffer di dimensioni *cbProperties*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Operazione completata.<br/>                   |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | Argomento del puntatore **NULL.**<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




