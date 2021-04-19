---
description: "Il metodo CheckTransform controlla se un tipo di supporto di input è compatibile con un tipo di supporto di output. Questo metodo esegue l'override del metodo CTransformFilter:: CheckTransform."
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: Metodo CTransInPlaceFilter. CheckTransform (Transip. h)
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
ms.openlocfilehash: 6a80132723be0b70f2c4afe93306d7f581b7734c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332980"
---
# <a name="ctransinplacefilterchecktransform-method"></a>CTransInPlaceFilter. CheckTransform, metodo

Il `CheckTransform` metodo verifica se un tipo di supporto di input è compatibile con un tipo di supporto di output. Questo metodo esegue l'override del metodo [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) .

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

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di input.

</dd> <dt>

*mtOut* 
</dt> <dd>

Puntatore a un oggetto **CMediaType** che specifica il tipo di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Il filtro **CTransInPlace** non chiama mai `CheckTransform` . Al contrario, tutte le connessioni pin utilizzano [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) per verificare il tipo di supporto, supponendo che i tipi di input e di output corrispondano sempre.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




