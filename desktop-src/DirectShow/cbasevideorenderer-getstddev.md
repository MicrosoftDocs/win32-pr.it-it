---
description: Il metodo GetStdDev stima la deviazione standard in millisecondi tra la scadenza di ogni frame e il momento in cui viene effettivamente eseguito il rendering, per le statistiche per frame.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Metodo CBaseVideoRenderer.GetStdDev (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f7b6ab85000f537179fcc9ae6b979194ae4e975ea2b394d0c58afb8515158aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157083"
---
# <a name="cbasevideorenderergetstddev-method"></a>Metodo CBaseVideoRenderer.GetStdDev

Il `GetStdDev` metodo stima la deviazione standard in millisecondi tra la scadenza di ogni frame e il momento in cui viene effettivamente eseguito il rendering, per le statistiche per frame.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nSamples* 
</dt> <dd>

Valore intero che contiene il numero di campioni video ricevuti dal renderer video.

</dd> <dt>

*piResult* 
</dt> <dd>

Puntatore a un valore intero che conterrà la deviazione standard.

</dd> <dt>

*llSumSq* 
</dt> <dd>

Valore che rappresenta la deviazione standard, in millisecondi, di tutti gli esempi video sottoposti a rendering. Più basso è il valore, maggiore è la coerenza del rendering.

</dd> <dt>

*iTot* 
</dt> <dd>

Valore che rappresenta il valore medio, in millisecondi, tra l'ora stampata e l'ora di rendering per tutti gli esempi di video sottoposti a rendering.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce NOERROR.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




