---
description: Il metodo Notify riceve una notifica che indica che è richiesta una modifica della qualità.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: Metodo CBaseVideoRenderer.Notify (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8674ecbf7951ca0c208f9ffb50c0e5d9591b16552fda266c7d641905edd09a4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052191"
---
# <a name="cbasevideorenderernotify-method"></a>Metodo CBaseVideoRenderer.Notify

Il `Notify` metodo riceve una notifica che indica che è richiesta una modifica di qualità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSelf* \[ Pollici\]
</dt> <dd>

Puntatore al filtro che invia la notifica sulla qualità.

</dd> <dt>

*q* \[ in\]
</dt> <dd>

Struttura di notifica della qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) nel renderer video. Questa operazione viene chiamata, in genere dal gestore del grafico dei filtri, quando è necessario ridurre la qualità. Ciò può verificarsi quando la qualità della riproduzione audio è stata aumentata fino a ridurre la qualità di riproduzione del video.

`Notify`imposta il **membro \_ dati m trThrottle** su un valore di ritardo che deve essere inserito tra i frame da [**ThrottleWait.**](cbasevideorenderer-throttlewait.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




