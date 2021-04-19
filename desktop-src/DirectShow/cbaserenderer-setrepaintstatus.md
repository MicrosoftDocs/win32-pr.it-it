---
description: Il metodo SetRepaintStatus Abilita o Disabilita gli eventi di ridisegno.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Metodo CBaseRenderer. SetRepaintStatus (Renbase. h)
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
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333002"
---
# <a name="cbaserenderersetrepaintstatus-method"></a>CBaseRenderer. SetRepaintStatus, metodo

Il `SetRepaintStatus` metodo consente di abilitare o disabilitare gli eventi di ridisegno.

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

Valore booleano che indica se gli eventi di Repaint sono abilitati. Se **true**, il filtro invierà gli eventi di [**\_ ridisegno EC**](ec-repaint.md) al gestore del grafico dei filtri. In caso contrario, non verrà inviato alcun \_ evento di ridisegno EC.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo garantisce che il gestore del grafo del filtro non venga invaso da eventi di ridisegno EC ridondanti \_ . Dopo che il filtro ha inviato un evento di [**\_ ridisegno EC**](ec-repaint.md) , chiama questo metodo con il valore **true**. Il filtro non invia più eventi di \_ ridisegno EC fino a quando non riceve più dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




