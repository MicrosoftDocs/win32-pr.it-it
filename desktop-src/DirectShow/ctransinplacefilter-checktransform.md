---
description: Il metodo CheckTransform controlla se un tipo di supporto di input è compatibile con un tipo di supporto di output. Questo metodo esegue l'override del metodo CTransformFilter::CheckTransform.
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: Metodo CTransInPlaceFilter.CheckTransform (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49b7f4aaac21cf6a55360e2e1b970bd9dfa62c0422241f7356871117e138d57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654960"
---
# <a name="ctransinplacefilterchecktransform-method"></a>Metodo CTransInPlaceFilter.CheckTransform

Il `CheckTransform` metodo controlla se un tipo di supporto di input è compatibile con un tipo di supporto di output. Questo metodo esegue l'override [**del metodo CTransformFilter::CheckTransform.**](ctransformfilter-checktransform.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mtIn* 
</dt> <dd>

Puntatore a [**un oggetto CMediaType**](cmediatype.md) che specifica il tipo di input.

</dd> <dt>

*mtOut* 
</dt> <dd>

Puntatore a **un oggetto CMediaType** che specifica il tipo di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il **filtro CTransInPlace** non chiama mai `CheckTransform` . Tutte le connessioni pin usano [**invece CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) per controllare il tipo di supporto, presupponendo che i tipi di input e output corrispondano sempre.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




