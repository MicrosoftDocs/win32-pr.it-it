---
description: "Evento InkCollector.CursorInRange: si verifica quando un cursore entra nell'intervallo di rilevamento fisico (prossimità) del contesto della tablet."
ms.assetid: d05b240c-ba64-4008-b25d-e06c052eb5b0
title: Evento InkCollector.CursorInRange (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9b7cd6204b2dbb29f9a46e48ecb12569e1301f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110289"
---
# <a name="inkcollectorcursorinrange-event"></a>Evento InkCollector.CursorInRange

Si verifica quando un cursore entra nell'intervallo di rilevamento fisico (prossimità) del contesto della tablet.

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

**VARIANT \_ TRUE** per indicare che questa è la prima volta che l'agente di raccolta input penna viene contattato con [**l'oggetto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento CursorInRange.** in caso contrario, **VARIANT \_ FALSE.**

</dd> <dt>

*ButtonsState* \[ Pollici\]
</dt> <dd>

Stato dei pulsanti per il cursore che ha generato **l'evento CursorInRange.**

Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM.](using-the-com-library.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICECursorInRange.

**L'evento CursorInRange** viene generato anche in modalità di selezione o cancellazione, non solo in modalità input penna. A questo scopo, è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento. Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Evento CursorOutOfRange**](inkcollector-cursoroutofrange.md)
</dt> <dt>

[**Enumerazione InkCursorButtonState**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




