---
description: 'Il metodo Stop arresta il filtro. Questo metodo implementa il metodo IMediaFilter:: stop.'
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: Metodo CBaseFilter. Stop (Amfilter. h)
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
ms.openlocfilehash: b4c4893edcf02fa18da3dc207a49f87c91b2a9ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328172"
---
# <a name="cbasefilterstop-method"></a>Metodo CBaseFilter. Stop

Il `Stop` metodo interrompe il filtro. Questo metodo implementa il metodo [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CBasePin:: inactive**](cbasepin-inactive.md) su ognuno dei pin connessi del filtro. Imposta anche lo stato del filtro sullo stato \_ arrestato.

Quando il filtro si interrompe, deve rifiutare esempi da upstream, interrompere la distribuzione di campioni a valle, arrestare i thread di lavoro e liberare le risorse usate per lo streaming.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




