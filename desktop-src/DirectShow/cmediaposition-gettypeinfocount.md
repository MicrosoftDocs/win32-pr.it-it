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
ms.openlocfilehash: 8cfc54f414a6722f7f69a0330fad2d1a0cfab425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095479"
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
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




