---
description: 'Metodo CBasePin.Inactive: il metodo Inactive notifica al pin che il filtro non è più attivo.'
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Metodo CBasePin.Inactive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c0d9ec403b53c3197c001e966ce7efd5eb8bed2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099339"
---
# <a name="cbasepininactive-method"></a>Metodo CBasePin.Inactive

Il `Inactive` metodo notifica al pin che il filtro non è più attivo.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Quando il filtro si arresta, la [**classe CBaseFilter**](cbasefilter.md) chiama questo metodo su tutti i pin connessi del filtro.

Questo metodo non esegue alcuna operazione nella classe di base. Le classi derivate devono eseguire l'override di questo metodo per liberare tutte le risorse ottenute dal [**metodo CBasePin::Active.**](cbasepin-active.md) ad esempio per decommettere gli allocatori del pin.

Lo stato interno del gestore del grafico filtri non viene aggiornato fino a quando non viene restituito questo metodo, quindi non testare lo stato di questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




