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
ms.openlocfilehash: 59609e09b252e56aded1669264bb98cdbe823e89
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084589"
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
| Intestazione<br/>  | <dl> <dt>Vtrans.h (include Streams.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




