---
description: 'Metodo CTransInPlaceFilter.GetMediaType: il metodo GetMediaType recupera un tipo di supporto preferito per il pin di output.'
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Metodo CTransInPlaceFilter.GetMediaType (Transip.h)
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
ms.openlocfilehash: a714d3dba30b3038d6c04ecedd51db4196a3c4d899d7c607dd12f9a068f8a803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079301"
---
# <a name="ctransinplacefiltergetmediatype-method"></a>Metodo CTransInPlaceFilter.GetMediaType

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

Puntatore a [**un oggetto CMediaType**](cmediatype.md) che riceve il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ UNEXPECTED.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CTransformFilter::GetMediaType.**](ctransformfilter-getmediatype.md) Nella classe **CTransInPlaceFilter** ogni pin chiama il pin connesso opposto per enumerare i tipi di supporti preferiti. Il pin di input chiama il pin di input del filtro downstream e il pin di output chiama il pin di output del filtro upstream. Di conseguenza, il metodo `GetMediaType` del filtro non viene mai chiamato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




