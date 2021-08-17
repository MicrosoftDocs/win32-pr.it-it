---
description: Il metodo SetRepaintStatus abilita o disabilita gli eventi di ridisegno.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Metodo CBaseRenderer.SetRepaintStatus (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 748d0091bd3d2eae11773a9f94b62ceeb92b2d3ca64049f1a1981e38bf222e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016849"
---
# <a name="cbaserenderersetrepaintstatus-method"></a>Metodo CBaseRenderer.SetRepaintStatus

Il `SetRepaintStatus` metodo abilita o disabilita gli eventi di ridisegno.

## <a name="syntax"></a>Sintassi


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bRepaint* 
</dt> <dd>

Valore booleano che indica se gli eventi di ridisegno sono abilitati. Se **TRUE,** il filtro invierà [**gli eventi EC \_ REPAINT**](ec-repaint.md) al gestore del grafico filtri. In caso contrario, non invierà eventi \_ REPAINT EC.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo garantisce che il gestore del grafico filtri non sia inondato da eventi EC \_ REPAINT ridondanti. Dopo l'invio di [**un evento EC \_ REPAINT,**](ec-repaint.md) il filtro chiama questo metodo con il valore **TRUE.** Il filtro non invia altri eventi EC \_ REPAINT finché non riceve più dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




