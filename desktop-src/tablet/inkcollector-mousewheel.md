---
description: Si verifica quando viene spostata la rotellina del mouse mentre l'oggetto InkCollector o InkOverlay dispone dello stato attivo.
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: Evento InkCollector. MouseWheel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e6a6728bfcbe058ff5eab56499f6c8e885351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306733"
---
# <a name="inkcollectormousewheel-event"></a>Evento InkCollector. MouseWheel

Si verifica quando viene spostata la rotellina del mouse mentre l'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) dispone dello stato attivo.

## <a name="syntax"></a>Sintassi


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
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

*Delta* \[ in\]
</dt> <dd>

Conteggio con segno del numero di arresti ruotati della rotellina del mouse. Un dentello corrisponde a uno scatto della rotellina del mouse.

</dd> <dt>

*x* \[ in\]
</dt> <dd>

Coordinata x, in pixel, di un clic del mouse.

</dd> <dt>

*y* \[ in\]
</dt> <dd>

Coordinata y, in pixel, di un clic del mouse.

</dd> <dt>

*Annulla* \[ in uscita\]
</dt> <dd>

**Variante \_ TRUE** per annullare l'evento per il controllo padre; in caso contrario, **Variant \_ false**. Il valore predefinito è **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Le proprietà *px* e *py* sono in pixel e non le unità HIMETRIC associate allo spazio di input penna. Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione basata su penna e questo tipo di applicazione riconosce solo i pixel.

 

Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ IPEMouseWheel.

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

 

 




