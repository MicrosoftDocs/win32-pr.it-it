---
description: Passa un \_ \_ \_ messaggio di modifica delle dimensioni del video EC al gestore del grafico dei filtri.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Metodo CBaseControlVideo. OnVideoSizeChange (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37caa05d164c23484c749730796d6a5f10d67d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324493"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a>CBaseControlVideo. OnVideoSizeChange, metodo

Passa un \_ \_ \_ messaggio di modifica delle dimensioni del video EC al gestore del grafico dei filtri.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.



| Codice restituito                                                                                   | Descrizione               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Esito negativo.<br/>       |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/> |



 

## <a name="remarks"></a>Commenti

Un renderer video deve chiamare questa funzione membro ogni volta che viene modificata la dimensione del video; Questa operazione viene in genere chiamata una volta dopo la connessione iniziale. Se il renderer è in grado di supportare le modifiche del formato dinamico (da 320 x 240 a 160 x 120), dovrebbe chiamarlo anche dopo ogni modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




