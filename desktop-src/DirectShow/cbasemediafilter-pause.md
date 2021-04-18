---
description: Sospende l'oggetto. Implementa il metodo IMediaFilter::P ause.
ms.assetid: 4f4cbe7e-3004-4731-864f-737c2f51afff
title: Metodo CBaseMediaFilter. pause (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a75cbcf1d629b997584cff35ebd4095094fe8607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325077"
---
# <a name="cbasemediafilterpause-method"></a>CBaseMediaFilter. pause (metodo)

Sospende l'oggetto. Implementa il metodo [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Nella classe di base, questo metodo imposta la variabile membro di [**\_ stato CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) su stato \_ sospeso ma non esegue alcuna operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




