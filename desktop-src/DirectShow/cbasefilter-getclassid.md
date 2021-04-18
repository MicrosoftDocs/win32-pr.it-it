---
description: "Il metodo GetClassID recupera l'identificatore di classe del filtro. Questo metodo implementa il metodo IPersist:: GetClassID."
ms.assetid: c3a8b6ab-b36f-493e-9436-6784e25e2511
title: Metodo CBaseFilter. GetClassID (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02dfe8452da6366454dcc1cfeeed93c379c89bd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328949"
---
# <a name="cbasefiltergetclassid-method"></a>CBaseFilter. GetClassID, metodo

Il `GetClassID` metodo recupera l'identificatore di classe del filtro. Questo metodo implementa il metodo **IPersist:: GetClassID** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pClsID* 
</dt> <dd>

Puntatore a una variabile che riceve l'identificatore di classe.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un \_ puntatore S OK o e \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




