---
description: 'Evento InkCollector.CursorDown: si verifica quando la punta del cursore contatta la superficie del tablet di digitalizzazione.'
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: Evento InkCollector.CursorDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a98a58ce3c6576b45b4c60d47781f8de6ae9f8d5ab0cfea3222ef36890290f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032119"
---
# <a name="inkcollectorcursordown-event"></a>Evento InkCollector.CursorDown

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

Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) avviato quando l'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) ha causato l'evento **CursorDown.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito in \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents. Le interfacce \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents implementano [**l'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ ICECursorDown.

Usare questo evento con attenzione perché potrebbe avere un effetto negativo sulle prestazioni dell'input penna se viene eseguita una quantità troppo grande di codice nei gestori eventi. Per migliorare le prestazioni dell'input penna in tempo reale, nascondere o visualizzare il cursore del mouse nei gestori [**eventi MouseDown**](inkcollector-mousedown.md) e [**MouseUp.**](inkcollector-mouseup.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Evento CursorButtonDown**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Evento CursorButtonUp**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

