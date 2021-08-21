---
description: Il metodo Active viene chiamato quando lo stato passa alla sospensione o all'esecuzione.
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: Metodo CBaseRenderer.Active (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df5ec659b5e76940ebf279e3feb8995d34380db0543d9eebcf42c1f3bff8c0e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954970"
---
# <a name="cbaserendereractive-method"></a>Metodo CBaseRenderer.Active

Il `Active` metodo viene chiamato quando lo stato passa alla sospensione o all'esecuzione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il pin di input chiama questo metodo dal proprio [**metodo CRendererInputPin::Active.**](crendererinputpin-active.md) Questo metodo non esegue alcuna operazione nella classe di base.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




