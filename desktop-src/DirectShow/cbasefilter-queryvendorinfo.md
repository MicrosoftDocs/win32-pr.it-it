---
description: 'Il metodo QueryVendorInfo recupera una stringa contenente informazioni sul fornitore. Questo metodo implementa il metodo IBaseFilter:: QueryVendorInfo.'
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: Metodo CBaseFilter. QueryVendorInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1786477c042bb1d9ecc6340056a771141d0a3c74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333491"
---
# <a name="cbasefilterqueryvendorinfo-method"></a>CBaseFilter. QueryVendorInfo, metodo

Il `QueryVendorInfo` metodo recupera una stringa contenente le informazioni sul fornitore. Questo metodo implementa il metodo [**IBaseFilter:: QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVendorInfo* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore a una stringa di caratteri wide contenente le informazioni sul fornitore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ NOTIMPL.

## <a name="remarks"></a>Commenti

Per fornire informazioni sul fornitore per un filtro, eseguire l'override di questo metodo. Se si implementa questo metodo, utilizzare la funzione **CoTaskMemAlloc** per allocare memoria per la stringa. Il chiamante è responsabile della chiamata della funzione **CoTaskMemFree** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




