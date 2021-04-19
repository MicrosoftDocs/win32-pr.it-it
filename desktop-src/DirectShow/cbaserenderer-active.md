---
description: Il metodo attivo viene chiamato quando lo stato viene impostato su in pausa o in esecuzione.
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: Metodo CBaseRenderer. Active (Renbase. h)
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
ms.openlocfilehash: 11593ffb25a953f4269d84ee2b9c9d884a23e5fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329407"
---
# <a name="cbaserendereractive-method"></a>Metodo CBaseRenderer. Active

Il `Active` metodo viene chiamato quando lo stato viene impostato su in pausa o in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Il pin di input chiama questo metodo dal proprio metodo [**CRendererInputPin:: Active**](crendererinputpin-active.md) . Questo metodo non esegue alcuna operazione nella classe di base.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




