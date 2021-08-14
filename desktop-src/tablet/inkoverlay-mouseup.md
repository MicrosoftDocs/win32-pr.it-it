---
description: "Evento InkOverlay.MouseUp: si verifica quando il puntatore del mouse si trova sull'oggetto InkCollector o InkOverlay e viene rilasciato un pulsante del mouse."
ms.assetid: 049e1560-d4b2-4d34-9d54-2b45217001b2
title: Evento InkOverlay.MouseUp (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 675c588d12976a506afec02e1bec58d97a99fd13ec897250f0e472dfbc519490
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219787"
---
# <a name="inkoverlaymouseup-event"></a>Evento InkOverlay.MouseUp

Si verifica quando il puntatore del mouse si trova [**sull'oggetto InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) e viene rilasciato un pulsante del mouse.

## <a name="syntax"></a>Sintassi


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pulsante* \[ Pollici\]
</dt> <dd>

Pulsante del mouse rilasciato.

</dd> <dt>

*MAIUSC* \[ Pollici\]
</dt> <dd>

Stato del tasto MAIUSC.

</dd> <dt>

*pX* \[ Pollici\]
</dt> <dd>

Coordinata x, in pixel, di un clic del mouse.

</dd> <dt>

*pY* \[ Pollici\]
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

Per migliorare le prestazioni dell'input penna in tempo reale, nascondere o visualizzare il cursore del mouse nei gestori [**eventi MouseDown**](inkcollector-mousedown.md) e [**MouseUp.**](inkcollector-mouseup.md)

> [!Note]  
> Le proprietà *pX* e *pY* sono espresse in pixel e non nelle unità HIMETRIC associate allo spazio input penna. Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione inconsapevole e questo tipo di applicazione comprende solo i pixel.

 

> [!Note]  
> Alcuni controlli si basano su una relazione specifica tra gli eventi [**MouseDown,**](inkcollector-mousedown.md) [**MouseMove**](inkcollector-mousemove.md) [**e MouseUp.**](inkcollector-mouseup.md) L'annullamento di alcuni di questi eventi può avere risultati imprevisti.

 

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID IPEMouseUp.

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

 

 




