---
description: Il metodo OnRenderEnd esegue una smussatura per i casi in cui il tempo di rendering varia a causa di interruzioni.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Metodo CBaseVideoRenderer. OnRenderEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f37b4d03f77090f4cac40a218fd3ac27c0c349d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324489"
---
# <a name="cbasevideorendereronrenderend-method"></a>CBaseVideoRenderer. OnRenderEnd, metodo

Il `OnRenderEnd` metodo esegue la smussatura per i casi in cui il tempo di rendering varia a causa di interruzioni.

## <a name="syntax"></a>Sintassi


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'esempio di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione membro deve essere chiamata subito dopo il disegno di un'immagine.

Questa funzione membro esegue l'override di [**CBaseRenderer:: OnRenderEnd**](cbaserenderer-onrenderend.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




