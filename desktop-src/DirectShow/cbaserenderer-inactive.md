---
description: Il metodo Inactive viene chiamato quando lo stato passa all'arresto.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: Metodo CBaseRenderer.Inactive (Renbase.h)
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
ms.openlocfilehash: e84afd1d4e4ffb013a2029f7d56a223f0aef2f019bc3beb11bd7bd6c202b88d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652401"
---
# <a name="cbaserendererinactive-method"></a>Metodo CBaseRenderer.Inactive

Il `Inactive` metodo viene chiamato quando lo stato passa all'arresto.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il pin di input chiama questo metodo dal proprio [**metodo CRendererInputPin::Inactive.**](crendererinputpin-inactive.md) Il filtro chiama il [**metodo CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md) per rilasciare l'esempio più recente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




