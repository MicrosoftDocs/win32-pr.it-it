---
description: "Metodo CMediaPosition.GetTypeInfoCount: il metodo GetTypeInfoCount recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto."
ms.assetid: c98368f2-ae0c-4301-be30-7332b19f53ee
title: Metodo CMediaPosition.GetTypeInfoCount (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 032584025d91d6e21b02ed74b26b2e59d55e3a6e044c215d586913d8417a412e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157009"
---
# <a name="cmediapositiongettypeinfocount-method"></a>Metodo CMediaPosition.GetTypeInfoCount

Il `GetTypeInfoCount` metodo recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pctinfo* 
</dt> <dd>

Puntatore a una variabile che riceve il numero di interfacce di informazioni sul tipo fornite dall'oggetto . Quando il metodo viene restituito, il valore è 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                               | Descrizione                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Operazione completata.<br/>                   |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl> | Argomento del puntatore **NULL.**<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




