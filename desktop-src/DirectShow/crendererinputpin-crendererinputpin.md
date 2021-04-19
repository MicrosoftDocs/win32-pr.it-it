---
description: Il metodo CRendererInputPin è un metodo del costruttore.
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: Costruttore CRendererInputPin. CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6888b234b87a48fc89f70c0db36122cbf7289ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333188"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a>Costruttore CRendererInputPin. CRendererInputPin

Il `CRendererInputPin` metodo è un metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CRendererInputPin(
   CBaseRenderer *pRenderer,
   HRESULT       *phr,
   LPCWSTR       Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRenderer* 
</dt> <dd>

Puntatore all'oggetto [**CBaseRenderer**](cbaserenderer.md) che implementa il filtro.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a una variabile che riceve un valore **HRESULT** .

</dd> <dt>

*Nome* 
</dt> <dd>

Puntatore a una stringa di caratteri wide contenente l'identificatore del PIN.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 




