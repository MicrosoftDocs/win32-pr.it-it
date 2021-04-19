---
description: Il metodo ShouldDrawSampleNow determina il modo in cui un campione viene pianificato per il rendering.
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: Metodo CBaseRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27fbf603fd670cac2a39831114a7f141b17ffd2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333000"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a>CBaseRenderer. ShouldDrawSampleNow, metodo

Il `ShouldDrawSampleNow` metodo determina il modo in cui un campione viene pianificato per il rendering.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Puntatore a una variabile che contiene l'ora di inizio dell'esempio.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntatore a una variabile che contiene l'ora di fine dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore \_ false. Se la classe derivata esegue l'override di questo metodo, restituire uno dei valori mostrati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Il rendering dell'esempio deve essere eseguito immediatamente.<br/>                              |
| <dl> <dt>**S \_ false**</dt> </dl>   | L'esempio deve essere pianificato per il rendering, in base agli indicatori temporali.<br/> |
| <dl> <dt>**Codice di errore**</dt> </dl> | Non eseguire il rendering di questo esempio.<br/>                                              |



 

## <a name="remarks"></a>Commenti

Il metodo [**CBaseRenderer:: GetSampleTimes**](cbaserenderer-getsampletimes.md) chiama questo metodo. Per impostazione predefinita, gli esempi sono sempre pianificati per il rendering in base ai relativi timestamp. La classe derivata può eseguire l'override di questo metodo. ad esempio, per implementare il controllo qualità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




