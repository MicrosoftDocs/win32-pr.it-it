---
description: 'Evento InkOverlay.CursorDown: si verifica quando la punta del cursore contatta la superficie del tablet di digitalizzazione.'
ms.assetid: 753aa733-8d62-4983-b76d-d58844b79c35
title: Evento InkOverlay.CursorDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ed26c672aadc9fa19f6a6426fed7339752448d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117059"
---
# <a name="inkoverlaycursordown-event"></a>Evento InkOverlay.CursorDown

Si verifica quando la punta del cursore contatta la superficie del tablet di digitalizzazione.

## <a name="syntax"></a>Sintassi


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cursore* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato [**l'evento CursorDown.**](inkcollector-cursordown.md)

</dd> <dt>

*Tratto* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) avviato quando l'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) ha causato l'evento [**CursorDown.**](inkcollector-cursordown.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito in \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents. Le interfacce \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents implementano [**l'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ ICECursorDown.

Usare questo evento con attenzione perché potrebbe avere un effetto negativo sulle prestazioni dell'input penna se viene eseguita una quantità troppo grande di codice nei gestori eventi. Per migliorare le prestazioni dell'input penna in tempo reale, nascondere o visualizzare il cursore del mouse nei gestori [**eventi MouseDown**](inkcollector-mousedown.md) e [**MouseUp.**](inkcollector-mouseup.md)

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

[**Evento CursorButtonDown**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Evento CursorButtonUp**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

