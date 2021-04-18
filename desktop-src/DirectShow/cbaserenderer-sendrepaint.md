---
description: Il metodo SendRepaint Invia un evento Repaint al gestore del grafico dei filtri.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Metodo CBaseRenderer. SendRepaint (Renbase. h)
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
ms.openlocfilehash: b3a88f0c1dae54cb5d9be1e4e9ad3e9677bdd958
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329534"
---
# <a name="cbaserenderersendrepaint-method"></a>CBaseRenderer. SendRepaint, metodo

Il `SendRepaint` metodo invia un evento Repaint al gestore del grafico dei filtri.

## <a name="syntax"></a>Sintassi


```C++
void SendRepaint();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo invia un evento di [**\_ ridisegno EC**](ec-repaint.md) al gestore del grafico del filtro se le condizioni seguenti sono vere:

-   Il pin di input è connesso.
-   Il filtro non Scarica i dati.
-   Non è stata raggiunta la fine del flusso.
-   Il flag [**\_ BAbort di CBaseRenderer:: m**](cbaserenderer-m-babort.md) è **false**.
-   Il flag [**\_ BRepaintStatus di CBaseRenderer:: m**](cbaserenderer-m-brepaintstatus.md) è **true**.

A seconda dello stato del grafico, l' \_ evento di ridisegno EC può causare il reinvio di un campione da parte del filtro upstream, il grafico del filtro per cercare la posizione corrente oppure il gestore del grafico del filtro per sospendere momentaneamente. (Vedere la pagina relativa al [**\_ ridisegno EC**](ec-repaint.md)). Questo evento è potenzialmente inefficiente, quindi deve essere usato in modo sporadico. Tuttavia, i renderer video a volte devono aggiornare la visualizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




