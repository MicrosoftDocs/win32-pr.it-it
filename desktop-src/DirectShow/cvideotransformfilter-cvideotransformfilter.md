---
description: Costruttore CVideoTransformFilter.CVideoTransformFilter - Metodo costruttore.
ms.assetid: 4dad635f-4637-4f40-9f02-a91b59d05278
title: Costruttore CVideoTransformFilter.CVideoTransformFilter (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.CVideoTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1db2b665a1525f1352844a2963bd44a761a080a058154419b3320f7113aa3740
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086881"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a>Costruttore CVideoTransformFilter.CVideoTransformFilter

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Stringa contenente il nome di debug del filtro. Per altre informazioni, vedere [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** di aggregazione. In caso contrario, impostare questo parametro su **NULL.**

</dd> <dt>

*Clsid* 
</dt> <dd>

Identificatore di classe del filtro.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




