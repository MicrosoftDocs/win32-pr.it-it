---
description: Si verifica quando viene riconosciuto un movimento del sistema.
ms.assetid: 6f82b234-2088-4207-a6b4-6c6919623d6a
title: Evento InkOverlay.SystemGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b1e6ac7c02bc308856a89043bc0b1824b0fab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313457"
---
# <a name="inkoverlaysystemgesture-event"></a>Evento temGesture InkOverlay.Sys

Si verifica quando viene riconosciuto un movimento del sistema.

## <a name="syntax"></a>Sintassi


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cursore* \[ in\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento [**SystemGesture**](inkcollector-systemgesture.md) .

</dd> <dt>

*ID* \[ in\]
</dt> <dd>

Valore del movimento del sistema.

</dd> <dt>

*X* \[ in\]
</dt> <dd>

Coordinata x della posizione del movimento.

</dd> <dt>

*Y* \[ in\]
</dt> <dd>

Coordinata y della posizione del movimento.

</dd> <dt>

*Modificatore* \[ in\]
</dt> <dd>

Riservato.

</dd> <dt>

*Carattere* \[ in\]
</dt> <dd>

Riservato.

</dd> <dt>

*CursorMode* \[ in\]
</dt> <dd>

Valore che indica se l'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) è in modalità normale o in modalità gomma. 1 è per la modalità normale e 2 sono per la modalità gomma.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

I movimenti di sistema sono utili perché forniscono informazioni sull'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) usato per creare il movimento. Forniscono anche collegamenti alle combinazioni di eventi del mouse e sono metodi "più economici" per rilevare gli eventi del mouse.

Ad esempio, invece di cercare una [](inkcollector-mouseup.md)  /  coppia di eventi di evento [**MouseDown**](inkcollector-mousedown.md) di un evento MouseUp senza che si verifichino altri eventi del mouse, è possibile cercare i movimenti del sistema [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) o **RightTap** .

Come altro esempio, anziché ascoltare gli eventi dell'evento MouseMove di [**evento MouseDown**](inkcollector-mousedown.md)  /  [](inkcollector-mousemove.md) e ottenere numerosi messaggi di **evento MouseMove** , è possibile osservare i movimenti del sistema di [**trascinamento**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) o **RightDrag se** , purché non si sia interessati alle coordinate (x, y) di ogni posizione del mouse. In questo modo è possibile ricevere un solo messaggio anziché molti messaggi di **evento MouseMove** .

Per un elenco di movimenti di sistema specifici, vedere il tipo di enumerazione [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) . Per ulteriori informazioni sui movimenti di sistema, vedere [utilizzo di movimenti](using-gestures.md) e [input del comando sul Tablet PC](/previous-versions//dd314533(v=vs.85)).

Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICESystemGesture.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**InkOverlay (classe)**](inkoverlay-class.md)
</dt> <dt>

[**Enumerazione InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[Uso di movimenti](using-gestures.md)
</dt> <dt>

[Input penna, input penna e riconoscimento](pen-input--ink--and-recognition.md)
</dt> <dt>

[Input del comando sul Tablet PC](/previous-versions//dd314533(v=vs.85))
</dt> </dl>

 

