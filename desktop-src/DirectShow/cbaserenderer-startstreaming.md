---
description: Il metodo StartStreaming avvia il flusso quando il filtro passa a uno stato di esecuzione.
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: Metodo CBaseRenderer. StartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf1fcb1cbfb651221296054493688b2d9f33bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332997"
---
# <a name="cbaserendererstartstreaming-method"></a>CBaseRenderer. StartStreaming, metodo

Il `StartStreaming` metodo avvia lo streaming quando il filtro passa a uno stato di esecuzione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT** .

## <a name="remarks"></a>Commenti

Se il filtro include un esempio, pianifica l'esempio per il rendering. In caso contrario, se è presente una notifica di fine del flusso in sospeso, il filtro Invia un evento [**EC \_ complete**](ec-complete.md) al gestore del grafico dei filtri.

Questo metodo chiama il metodo [**CBaseRenderer:: OnStartStreaming**](cbaserenderer-onstartstreaming.md) . Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




