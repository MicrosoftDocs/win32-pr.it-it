---
description: Deprecato. PenInputPanel è stato sostituito dal pannello di input di testo (TIP). Si verifica quando l'oggetto PenInputPanel viene visualizzato o nascosto.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: Evento PenInputPanel.VisibleChanged (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc917f34c09ef0d4f079fd55e476bbbc4cea266e1b1c436a62b20d6c08ed1b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596610"
---
# <a name="peninputpanelvisiblechanged-event"></a>Evento PenInputPanel.VisibleChanged

Deprecato. [**PenInputPanel**](peninputpanel-class.md) è stato sostituito dal pannello [di input di testo (TIP).](text-input-panel-reference.md)

Si verifica quando [**l'oggetto PenInputPanel**](peninputpanel-class.md) viene visualizzato o nascosto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewVisibility* \[ Pollici\]
</dt> <dd>

**VARIANT \_ TRUE** per fare in modo che [**l'oggetto PenInputPanel**](peninputpanel-class.md) diventi visibile; in caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo evento ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

**L'evento VisibleChanged si** applica alla destinazione del passaggio del mouse del Pannello input penna di Tablet PC. Tuttavia, non viene generato quando la destinazione del passaggio del mouse si espande per visualizzare il Pannello input penna di Tablet PC completo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Peninputpanel**](peninputpanel-class.md)
</dt> </dl>

 

 




