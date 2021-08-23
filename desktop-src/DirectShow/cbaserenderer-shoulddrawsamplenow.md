---
description: Il metodo ShouldDrawSampleNow determina come è pianificato il rendering di un esempio.
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: Metodo CBaseRenderer.ShouldDrawSampleNow (Renbase.h)
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
ms.openlocfilehash: 818a7682fed504028ebee1c3a5ff5d35a268e1daad8756b110bcfcb2ca8d9f80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016869"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a>Metodo CBaseRenderer.ShouldDrawSampleNow

Il `ShouldDrawSampleNow` metodo determina la modalità di pianificazione del rendering di un esempio.

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

Restituisce S \_ FALSE. Se la classe derivata esegue l'override di questo metodo, restituire uno dei valori illustrati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Il rendering dell'esempio deve essere eseguito immediatamente.<br/>                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | L'esempio deve essere pianificato per il rendering, in base ai timestamp.<br/> |
| <dl> <dt>**Codice errore**</dt> </dl> | Non eseguire il rendering di questo esempio.<br/>                                              |



 

## <a name="remarks"></a>Commenti

Il [**metodo CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) chiama questo metodo. Per impostazione predefinita, gli esempi sono sempre pianificati per il rendering in base ai relativi timestamp. La classe derivata può eseguire l'override di questo metodo. ad esempio per implementare il controllo di qualità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




