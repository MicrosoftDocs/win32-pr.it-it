---
description: Il metodo OnRenderStart imposta le informazioni per il rendering.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: Metodo CBaseVideoRenderer. OnRenderStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325368"
---
# <a name="cbasevideorendereronrenderstart-method"></a>CBaseVideoRenderer. OnRenderStart, metodo

Il `OnRenderStart` metodo imposta le informazioni per il rendering.

## <a name="syntax"></a>Sintassi


```C++
void OnRenderStart(
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

Questa funzione membro recupera l'ora dell'orologio corrente dal sistema e la archivia in una variabile membro da utilizzare al termine del disegno. La funzione esegue anche la registrazione delle prestazioni. Questa funzione membro deve essere chiamata immediatamente prima dell'inizio del disegno.

Questa funzione membro esegue l'override di [**CBaseRenderer:: OnRenderStart**](cbaserenderer-onrenderstart.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




