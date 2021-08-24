---
description: "Evento InkCollector.MouseWheel: si verifica quando la rotellina del mouse si sposta mentre l'oggetto InkCollector o InkOverlay ha lo stato attivo."
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: Evento InkCollector.MouseWheel (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6c66d5b8698131f3dce422e404f7ce33a25472a0c1e28211f5f90b5616f9f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713021"
---
# <a name="inkcollectormousewheel-event"></a>Evento InkCollector.MouseWheel

Si verifica quando la rotellina del mouse si sposta mentre [**l'oggetto InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) ha lo stato attivo.

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

*Pulsante* \[ Pollici\]
</dt> <dd>

Pulsante del mouse premuto.

</dd> <dt>

*MAIUSC* \[ Pollici\]
</dt> <dd>

Stato del tasto MAIUSC.

</dd> <dt>

*Delta* \[ Pollici\]
</dt> <dd>

Conteggio con segno del numero di deviazioni ruotate dalla rotellina del mouse. Un dentello corrisponde a uno scatto della rotellina del mouse.

</dd> <dt>

*x* \[ in\]
</dt> <dd>

Coordinata x, in pixel, di un clic del mouse.

</dd> <dt>

*y* \[ in\]
</dt> <dd>

Coordinata y, in pixel, di un clic del mouse.

</dd> <dt>

*Annulla* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** per annullare l'evento per il controllo padre. in caso contrario, **VARIANT \_ FALSE.** Il valore predefinito è **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Le proprietà *pX* e *pY* sono in pixel e non le unità HIMETRIC associate allo spazio input penna. Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione che non è in conoscenza della penna e questo tipo di applicazione comprende solo i pixel.

 

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID IPEMouseWheel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Enumerazione InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumerazione InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




