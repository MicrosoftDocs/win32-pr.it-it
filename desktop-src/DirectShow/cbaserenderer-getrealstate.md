---
description: Il metodo GetRealState recupera lo stato del filtro.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Metodo CBaseRenderer. GetRealState (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40f2e49137a4324b14f25e4abb9b14cb919efbb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325934"
---
# <a name="cbaserenderergetrealstate-method"></a>CBaseRenderer. GetRealState, metodo

Il `GetRealState` metodo recupera lo stato del filtro.

## <a name="syntax"></a>Sintassi


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore dello [**\_ stato CBaseFilter:: m**](cbasefilter-m-state.md). Il valore è un membro del tipo enumerato [**\_ stato filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) .

## <a name="remarks"></a>Commenti

Questo metodo fornisce un'alternativa più semplice al metodo [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) , per uso interno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




