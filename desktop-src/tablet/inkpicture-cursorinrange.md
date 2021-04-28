---
description: "Evento InkPicture.CursorInRange: si verifica quando un cursore entra nell'intervallo di rilevamento fisico (prossimità) del contesto del tablet."
ms.assetid: e921e175-a2cf-45e6-bb81-dc82e384d3b1
title: Evento InkPicture.CursorInRange (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05d703022e8d97df0d8d74a73e20af3d91b8531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086579"
---
# <a name="inkpicturecursorinrange-event"></a>Evento InkPicture.CursorInRange

Si verifica quando un cursore entra nell'intervallo di rilevamento fisico (prossimità) del contesto del tablet.

## <a name="syntax"></a>Sintassi


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cursore* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento CursorInRange.**

</dd> <dt>

*NewCursor* \[ Pollici\]
</dt> <dd>

**VARIANT \_ TRUE** se questa è la prima volta che l'agente di raccolta input penna viene contattato con [**l'oggetto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **CursorInRange.** in caso contrario, **VARIANT \_ FALSE.**

</dd> <dt>

*ButtonsState* \[ Pollici\]
</dt> <dd>

Stato dei pulsanti per il cursore che ha generato **l'evento CursorInRange.**

Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nell'interfaccia di solo invio **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID \_ ICECursorInRange DISPID.

**L'evento CursorInRange** viene generato anche in modalità selezione o cancellazione, non solo in modalità input penna. A questo scopo, è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento. Il vantaggio di questo requisito è una maggiore libertà di innovare sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**Evento CursorOutOfRange**](inkpicture-cursoroutofrange.md)
</dt> <dt>

[**Enumerazione InkCursorButtonState**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




