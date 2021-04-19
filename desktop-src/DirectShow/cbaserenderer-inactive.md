---
description: Il metodo inattivo viene chiamato quando lo stato viene impostato su arrestato.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: Metodo CBaseRenderer. Inactive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac328c772b740a0d7ab05be4c6ea9f2a24f852e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326282"
---
# <a name="cbaserendererinactive-method"></a>Metodo CBaseRenderer. Inactive

Il `Inactive` metodo viene chiamato quando lo stato viene impostato come arrestato.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Il pin di input chiama questo metodo dal proprio metodo [**CRendererInputPin:: inactive**](crendererinputpin-inactive.md) . Il filtro chiama il metodo [**CBaseRenderer:: ClearPendingSample**](cbaserenderer-clearpendingsample.md) per rilasciare l'esempio più recente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




