---
description: Passa un messaggio EC \_ VIDEO SIZE CHANGED al gestore del grafico del \_ \_ filtro.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Metodo CBaseControlVideo.OnVideoSizeChange (Ctlutil.h)
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
ms.openlocfilehash: 689f6f14426d88270136d6cc3687f9e214b72d6e42e2af44f3d189510d61f327
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076691"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a>Metodo CBaseControlVideo.OnVideoSizeChange

Passa un messaggio EC \_ VIDEO SIZE CHANGED al gestore del grafico del \_ \_ filtro.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT** che dipende dall'implementazione. può essere uno dei valori seguenti o altri valori non elencati.



| Codice restituito                                                                                   | Descrizione               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Esito negativo.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/> |



 

## <a name="remarks"></a>Commenti

Un renderer video deve chiamare questa funzione membro ogni volta che le dimensioni del video vengono modificate. questa operazione viene in genere chiamata una volta dopo la connessione iniziale. Se il renderer può supportare modifiche di formato dinamico (da 320 x 240 a 160 x 120), deve anche chiamarlo dopo ogni modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




