---
description: Il metodo Stop arresta il filtro. Questo metodo implementa il metodo IMediaFilter::Stop.
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: Metodo CBaseFilter.Stop (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 659ad34c01ca6c74a24f6bbf5f5bef42df46f94f06b7e03541f9caf3398b39e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768191"
---
# <a name="cbasefilterstop-method"></a>Metodo CBaseFilter.Stop

Il `Stop` metodo arresta il filtro. Questo metodo implementa il [**metodo IMediaFilter::Stop.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo chiama il [**metodo CBasePin::Inactive**](cbasepin-inactive.md) su ognuno dei pin connessi del filtro. Imposta anche lo stato del filtro su Stato \_ arrestato.

Quando il filtro si arresta, deve rifiutare gli esempi da upstream, interrompere la distribuzione degli esempi a valle, arrestare i thread di lavoro e liberare le risorse usate per lo streaming.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




