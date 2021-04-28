---
description: 'Metodo CBaseFilter.Pause: il metodo Pause sospende il filtro. Questo metodo implementa il metodo IMediaFilter::P ause.'
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: Metodo CBaseFilter.Pause (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee91393a574d0135e66e5a9c1e1e6b0325a0b4de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120089"
---
# <a name="cbasefilterpause-method"></a>Metodo CBaseFilter.Pause

Il `Pause` metodo sospende il filtro. Questo metodo implementa il [**metodo IMediaFilter::P ause.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo chiama [**il metodo CBasePin::Active**](cbasepin-active.md) su ogni segnaposto connesso del filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




