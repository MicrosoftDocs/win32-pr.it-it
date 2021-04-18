---
description: Il metodo GetTypeInfoCount Recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto.
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Metodo CBaseDispatch. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39c5b78181f5f26fb5f57831345bb6345a26da85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327966"
---
# <a name="cbasedispatchgettypeinfocount-method"></a>CBaseDispatch. GetTypeInfoCount, metodo

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

Puntatore a una variabile che riceve il numero di interfacce di informazioni sul tipo fornite dall'oggetto. Quando il metodo restituisce, il valore è 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                               | Descrizione                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Esito positivo.<br/>                   |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Argomento puntatore **null** .<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseDispatch**](cbasedispatch.md)
</dt> </dl>

 

 




