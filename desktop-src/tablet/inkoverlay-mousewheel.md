---
description: "Evento InkOverlay.MouseWheel: si verifica quando la rotellina del mouse si sposta mentre l'oggetto InkCollector o InkOverlay ha lo stato attivo."
ms.assetid: b7269e07-7001-48ca-8e20-a39cb02f3719
title: Evento InkOverlay.MouseWheel (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468dbdac09fd40144768e8342791d5712a570bcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116889"
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

Indica se l'evento deve essere annullato per il controllo padre. Il valore predefinito è **FALSE,** che specifica che l'evento non deve essere annullato.

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
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC \[ Edition\]<br/>                                                       |
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

 

 




