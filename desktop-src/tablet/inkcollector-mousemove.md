---
description: Si verifica quando il puntatore del mouse viene spostato sull'oggetto InkCollector o InkOverlay.
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: Evento InkCollector. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ad88c35871ed73125be73b66329ede464f0c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306735"
---
# <a name="inkcollectormousemove-event"></a>Evento InkCollector. MouseMove

Si verifica quando il puntatore del mouse viene spostato sull'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) .

## <a name="syntax"></a>Sintassi


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pulsante* \[ in\]
</dt> <dd>

Pulsante del mouse premuto.

</dd> <dt>

*Sposta* \[ in\]
</dt> <dd>

Stato del tasto MAIUSC.

</dd> <dt>

*px* \[ in\]
</dt> <dd>

Coordinata x, in pixel, di un clic del mouse.

</dd> <dt>

*py* \[ in\]
</dt> <dd>

Coordinata y, in pixel, di un clic del mouse.

</dd> <dt>

*Annulla* \[ in uscita\]
</dt> <dd>

**Variante \_ TRUE** per annullare l'evento per il controllo padre; in caso contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Le proprietà *px* e *py* sono in pixel e non le unità HIMETRIC associate allo spazio di input penna. Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione basata su penna e questo tipo di applicazione riconosce solo i pixel.

 

> [!Note]  
> Alcuni controlli si basano su una relazione specifica tra gli eventi [**MouseDown**](inkcollector-mousedown.md), **MouseMove** e [**MouseUp**](inkcollector-mouseup.md) . L'annullamento di alcuni di questi eventi potrebbe avere risultati imprevisti.

 

Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ IPEMouseMove.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Enumerazione InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumerazione InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




