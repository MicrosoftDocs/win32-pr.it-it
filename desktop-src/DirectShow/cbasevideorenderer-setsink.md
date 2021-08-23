---
description: Il metodo SetSink imposta l'oggetto IQualityControl che riceverà messaggi di qualità.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: Metodo CBaseVideoRenderer.SetSink (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b5fef3eb6bd1b959c6c7246e4aeebf5b42a01ddcecd211f3e1d7860102a6381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697901"
---
# <a name="cbasevideorenderersetsink-method"></a>Metodo CBaseVideoRenderer.SetSink

Il `SetSink` metodo imposta [**l'oggetto IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) che riceverà messaggi di qualità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*piqc* 
</dt> <dd>

Puntatore [**all'oggetto IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) a cui devono essere inviate le notifiche.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) nel renderer video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




