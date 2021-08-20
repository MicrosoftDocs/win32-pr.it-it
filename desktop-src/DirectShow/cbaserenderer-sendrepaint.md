---
description: Il metodo SendRepaint invia un evento repaint al gestore del grafico dei filtri.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Metodo CBaseRenderer.SendRepaint (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendRepaint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9057d1ff733c30da3b3b0d7e960607eadd033dcee0b26994478c6da9156a183e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954790"
---
# <a name="cbaserenderersendrepaint-method"></a>Metodo CBaseRenderer.SendRepaint

Il `SendRepaint` metodo invia un evento repaint al gestore del grafico del filtro.

## <a name="syntax"></a>Sintassi


```C++
void SendRepaint();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo invia un [**evento EC \_ REPAINT**](ec-repaint.md) al gestore del grafico del filtro se si verificano le condizioni seguenti:

-   Il pin di input è connesso.
-   Il filtro non scarica i dati.
-   La fine del flusso non è stata raggiunta.
-   Il flag [**\_ bAbort CBaseRenderer::m**](cbaserenderer-m-babort.md) è **FALSE.**
-   Il flag [**CBaseRenderer::m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md) è **TRUE.**

A seconda dello stato del grafico, l'evento EC REPAINT può inviare nuovamente un campione al filtro upstream, il grafico dei filtri per la ricerca nella posizione corrente oppure la sospensione momentanea del gestore del grafico \_ del filtro. Vedere [**EC \_ REPAINT.**](ec-repaint.md) Questo evento è potenzialmente inefficiente, quindi deve essere usato con parsimonio. Tuttavia, i renderer video talvolta devono aggiornare la visualizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




