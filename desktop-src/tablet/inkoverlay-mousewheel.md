---
description: "Evento InkOverlay.MouseWheel: si verifica quando la rotellina del mouse si sposta mentre l'oggetto InkCollector o InkOverlay ha lo stato attivo."
ms.assetid: b7269e07-7001-48ca-8e20-a39cb02f3719
title: Evento InkOverlay.MouseWheel (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c2563ae898eff2b9541ac52d77626ddebb8259d8bb60a82b18f6460da55f7dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219205"
---
# <a name="inkoverlaymousewheel-event"></a>Evento InkOverlay.MouseWheel

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

Conteggio con segno del numero di detente ruotate dalla rotellina del mouse. Un dentello corrisponde a uno scatto della rotellina del mouse.

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

Indica se l'evento deve essere annullato per il controllo padre. Il valore predefinito è **FALSE,** che specifica che l'evento non deve essere annullato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Le proprietà *pX* e *pY* sono espresse in pixel e non nelle unità HIMETRIC associate allo spazio input penna. Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione inconsapevole e questo tipo di applicazione comprende solo i pixel.

 

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID IPEMouseWheel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Enumerazione InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumerazione InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




