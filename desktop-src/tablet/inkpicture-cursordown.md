---
description: 'Evento InkPicture.CursorDown: si verifica quando la punta del cursore contatta la superficie del tablet di digitalizzazione.'
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: Evento InkPicture.CursorDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a0fd7a6c077093ae7e14ab1d905398e0b75a585cf09c2a87b0da9b843844a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967080"
---
# <a name="inkpicturecursordown-event"></a>Evento InkPicture.CursorDown

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

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento CursorDown.**

</dd> <dt>

*Tratto* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) avviato quando [**l'oggetto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) ha causato l'evento **CursorDown.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questi metodi di evento sono definiti nelle **\_ interfacce IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents.** Le **\_ interfacce IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** implementano l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore DISPID \_ ICECursorDown.

Usare questo evento con attenzione perché potrebbe influire negativamente sulle prestazioni dell'input penna se viene eseguita una quantità troppo grande di codice nei gestori eventi. Per migliorare le prestazioni dell'input penna in tempo reale, nascondere o visualizzare il cursore del mouse nei gestori [**eventi MouseDown**](inkpicture-mousedown.md) e [**MouseUp.**](inkpicture-mouseup.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**Evento CursorButtonUp**](inkpicture-cursorbuttonup.md)
</dt> <dt>

[**Evento CursorButtonDown**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

