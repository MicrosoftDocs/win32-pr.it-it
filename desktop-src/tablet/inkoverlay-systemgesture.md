---
description: 'InkOverlay.Sysevento temGesture: si verifica quando viene riconosciuto un movimento di sistema.'
ms.assetid: 6f82b234-2088-4207-a6b4-6c6919623d6a
title: InkOverlay.SystemGesture (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3498d6b5fa779f6a15866ac93d53be8348f3d1a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086669"
---
# <a name="inkoverlaysystemgesture-event"></a>InkOverlay.Sysevento temGesture

Si verifica quando viene riconosciuto un movimento di sistema.

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

*Cursore* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato [**l'evento SystemGesture.**](inkcollector-systemgesture.md)

</dd> <dt>

*ID* \[ in\]
</dt> <dd>

Valore del movimento di sistema.

</dd> <dt>

*X* \[ in\]
</dt> <dd>

Coordinata x della posizione del movimento.

</dd> <dt>

*Y* \[ in\]
</dt> <dd>

Coordinata y della posizione del movimento.

</dd> <dt>

*Modificatore* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> <dt>

*Carattere* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> <dt>

*CursorMode* \[ Pollici\]
</dt> <dd>

Valore che indica se l'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) è in modalità normale o in modalità gomma. 1 è per la modalità normale e 2 per la modalità di cancellazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

I movimenti di sistema sono utili perché forniscono informazioni sull'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) usato per creare il movimento. Forniscono inoltre collegamenti a combinazioni di eventi del mouse e sono modi "più economici" per rilevare gli eventi del mouse.

Ad esempio, anziché cercare una coppia di eventi [**MouseUp Event**](inkcollector-mouseup.md)MouseDown Event senza altri eventi del mouse che si verificano tra di loro, è possibile cercare i movimenti di sistema Tap o  /  [](inkcollector-mousedown.md) **RightTap.** [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)

Come altro esempio, invece di ascoltare gli eventi evento [](inkcollector-mousedown.md)  /  [**MouseMove**](inkcollector-mousemove.md) dell'evento MouseDown e ricevere numerosi messaggi di evento **MouseMove,** è possibile controllare i movimenti di sistema [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) o **RightDrag** purché non si sia interessati alle coordinate (x, y) di ogni posizione del mouse. In questo modo è possibile ricevere un solo messaggio anziché numerosi **messaggi di evento MouseMove.**

Per un elenco di movimenti di sistema specifici, vedere il tipo di enumerazione [**InkSystemGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) Per altre informazioni sui movimenti di sistema, vedere [Uso di movimenti e](using-gestures.md) input dei comandi nel Tablet [PC.](/previous-versions//dd314533(v=vs.85))

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ ICESystemGesture DISPID.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Enumerazione InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[Uso dei movimenti](using-gestures.md)
</dt> <dt>

[Input penna, input penna e riconoscimento](pen-input--ink--and-recognition.md)
</dt> <dt>

[Input dei comandi nel Tablet PC](/previous-versions//dd314533(v=vs.85))
</dt> </dl>

 

