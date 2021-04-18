---
description: Deprecato. L'oggetto PenInputPanel è stato sostituito dal pannello di input di testo (TIP). Si verifica quando l'oggetto PenInputPanel è stato visualizzato o nascosto.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: Evento PenInputPanel. VisibleChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c739f3517ad9739f1d1ba95af9e5001dfbe659a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319156"
---
# <a name="peninputpanelvisiblechanged-event"></a>PenInputPanel. VisibleChanged, evento

Deprecato. L'oggetto [**PenInputPanel**](peninputpanel-class.md) è stato sostituito dal [Pannello di input di testo (tip)](text-input-panel-reference.md).

Si verifica quando l'oggetto [**PenInputPanel**](peninputpanel-class.md) è stato visualizzato o nascosto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewVisibility* \[ in\]
</dt> <dd>

**Variante \_ TRUE** per fare in modo che l'oggetto [**PenInputPanel**](peninputpanel-class.md) diventi visibile. in caso contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'evento ha esito positivo, viene restituito **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

L'evento **VisibleChanged** si applica alla destinazione del passaggio del mouse sul pannello di input di Tablet PC. Tuttavia, non viene generato quando la destinazione del passaggio del mouse si espande per visualizzare il pannello di input completo di Tablet PC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




