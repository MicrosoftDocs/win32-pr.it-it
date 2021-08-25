---
description: Il metodo ForceRefresh è obsoleto.
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: Metodo CPosPassThru.ForceRefresh (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 738a528562afd04e27105691b001958f130e353ec52aa60da86bec47c81b5ba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915521"
---
# <a name="cpospassthruforcerefresh-method"></a>Metodo CPosPassThru.ForceRefresh

Il `ForceRefresh` metodo è obsoleto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

In origine questa classe è stata progettata per memorizzare nella cache i puntatori alle interfacce [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del pin connesso. Il `ForceRefresh` metodo ha rilasciato tali interfacce.

Come attualmente implementato, questa classe non memorizza nella cache tali interfacce. Per motivi di `ForceRefresh` compatibilità, il metodo è ancora incluso, ma restituisce S \_ OK senza eseguire alcuna operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




