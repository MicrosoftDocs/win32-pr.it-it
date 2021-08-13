---
description: Blocco per proteggere la creazione di oggetti all'interno del filtro.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: Membro CBaseRenderer::m_ObjectCreationLock (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b0925aab0345d5eed8da19e12f355c417d66c1f36a1384a05950a87d4c95b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429311"
---
# <a name="cbaserendererm_objectcreationlock-member"></a>Membro CBaseRenderer::m \_ ObjectCreationLock

Blocco per proteggere la creazione di oggetti all'interno del filtro. Il filtro mantiene questo blocco quando crea il pin di input ([**CBaseRenderer::m \_ pInputPin**](cbaserenderer-m-pinputpin.md)) o [**l'oggetto CRendererPosPassThru**](crendererpospassthru.md) ([**CBaseRenderer::m \_ pPosition**](cbaserenderer-m-pposition.md)). Questo blocco impedisce a più thread di tentare di creare uno di questi oggetti contemporaneamente.

## <a name="syntax"></a>Sintassi


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




