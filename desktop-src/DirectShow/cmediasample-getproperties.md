---
description: "Il metodo GetProperties recupera le proprietà dell'esempio. Questo metodo implementa il metodo IMediaSample2:: GetProperties."
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: Metodo CMediaSample. GetProperties (Amfilter. h)
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
ms.openlocfilehash: 06ee1022f298e2f5167d348777b33fc2f1703eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324963"
---
# <a name="cmediasamplegetproperties-method"></a>Metodo CMediaSample. GetProperties

Il `GetProperties` metodo recupera le proprietà dell'esempio. Questo metodo implementa il metodo [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) .

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

Lunghezza dei dati della proprietà da recuperare, in byte.

</dd> <dt>

*pbProperties* 
</dt> <dd>

Puntatore a un buffer di dimensioni *cbProperties*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Esito positivo.<br/>                   |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Argomento puntatore **null** .<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




