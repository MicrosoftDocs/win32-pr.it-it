---
description: Si verifica quando il cursore esce dall'intervallo di rilevamento fisico (prossimità) del contesto della tavoletta.
ms.assetid: 0c71a4ad-3c09-4134-b0e7-82f29e8913ed
title: Evento InkPicture. CursorOutOfRange (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6a3eb09ca54fcfc4df3135896ea14f9bf56570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316834"
---
# <a name="inkpicturecursoroutofrange-event"></a>Evento InkPicture. CursorOutOfRange

Si verifica quando il cursore esce dall'intervallo di rilevamento fisico (prossimità) del contesto della tavoletta.

## <a name="syntax"></a>Sintassi


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cursore* \[ in\]
</dt> <dd>

Oggetto [**interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **CursorOutOfRange** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch (dispinterfaces) con ID DISPID \_ ICECursorOutOfRange.

L'evento **CursorOutOfRange** viene generato anche in modalità selezione o cancellazione, non solo in modalità input penna. A tale scopo, è necessario monitorare la modalità di modifica (che è responsabile dell'impostazione) e tenere presente la modalità prima di interpretare l'evento. Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma grazie a una maggiore consapevolezza degli eventi della piattaforma.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Evento CursorInRange**](inkpicture-cursorinrange.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




