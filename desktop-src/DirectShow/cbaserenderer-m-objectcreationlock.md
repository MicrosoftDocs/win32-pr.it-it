---
description: Blocco per proteggere la creazione di oggetti all'interno del filtro.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: 'Membro CBaseRenderer:: m_ObjectCreationLock (Renbase. h)'
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
ms.openlocfilehash: e344b20b4924ac26ebe6253f5388136b350abefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332212"
---
# <a name="cbaserendererm_objectcreationlock-member"></a>Membro ObjectCreationLock di CBaseRenderer:: m \_

Blocco per proteggere la creazione di oggetti all'interno del filtro. Il filtro utilizza questo blocco quando crea il pin di input ([**CBaseRenderer:: m \_ pInputPin**](cbaserenderer-m-pinputpin.md)) o l'oggetto [**CRendererPosPassThru**](crendererpospassthru.md) ([**CBaseRenderer:: m \_ pPosition**](cbaserenderer-m-pposition.md)). Questo blocco impedisce a più thread di tentare di creare uno di questi oggetti nello stesso momento.

## <a name="syntax"></a>Sintassi


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




