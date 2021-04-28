---
description: 'Costruttore CTransformFilter.CTransformFilter : metodo costruttore.'
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: Costruttore CTransformFilter.CTransformFilter (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fce67bbe22361bdbae0cd3e51768e0cf0743d97d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098719"
---
# <a name="ctransformfilterctransformfilter-constructor"></a>Costruttore CTransformFilter.CTransformFilter

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pObjectName* 
</dt> <dd>

Stringa contenente il nome di debug del filtro. Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)

</dd> <dt>

*lpUnk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** aggregatore. In caso contrario, impostare questo parametro su **NULL.**

</dd> <dt>

*Clsid* 
</dt> <dd>

Identificatore di classe del filtro.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il costruttore non crea i segnaposto del filtro. Ciò si verifica durante la prima chiamata al [**metodo GetPin.**](ctransformfilter-getpin.md) Il costruttore inizializza le variabili [**\_ membro m pInput**](ctransformfilter-m-pinput.md) e [**m \_ pOutput**](ctransformfilter-m-poutput.md) su **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




