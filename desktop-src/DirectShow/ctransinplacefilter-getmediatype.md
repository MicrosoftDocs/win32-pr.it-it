---
description: Il metodo GetMediaType recupera un tipo di supporto preferito per il pin di output.
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Metodo CTransInPlaceFilter. GetMediaType (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2347e0466a7df848e0f0b2bccec325eedfefc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326393"
---
# <a name="ctransinplacefiltergetmediatype-method"></a>CTransInPlaceFilter. GetMediaType, metodo

Il `GetMediaType` metodo recupera un tipo di supporto preferito per il pin di output.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iPosition* 
</dt> <dd>

Valore di indice in base zero.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che riceve il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ imprevisto.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) . Nella classe **CTransInPlaceFilter** ogni pin chiama il pin connesso opposto per enumerare i tipi di supporto preferiti. Il pin di input chiama il pin di input del filtro downstream e il pin di output chiama il pin di output del filtro upstream. Pertanto, il metodo del filtro `GetMediaType` non viene mai chiamato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




