---
description: Si verifica quando l'oggetto InkCollector rileva un pulsante del cursore.
ms.assetid: f07daad7-e0d1-45cf-a708-5486a5dfda8b
title: Evento InkCollector. CursorButtonUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932d768c13da953d1926b28fb651c63dc26be572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306055"
---
# <a name="inkcollectorcursorbuttonup-event"></a>Evento InkCollector. CursorButtonUp

Si verifica quando l'oggetto [**InkCollector**](inkcollector-class.md) rileva un pulsante del cursore.

## <a name="syntax"></a>Sintassi


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cursore* \[ in\]
</dt> <dd>

Oggetto [**interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **CursorButtonUp** .

</dd> <dt>

*Pulsante* \[ in\]
</dt> <dd>

Pulsante rilasciato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Quando l'utente completa un tratto e solleva la penna dal digitalizzatore, viene applicato un pulsante su una penna. Quando il pulsante non è premuto, viene attivato un pulsante su un barino.

Quando si rilascia il pulsante destro del mouse, si ricevono effettivamente due eventi **CursorButtonUp** , uno per il pulsante destro e uno per il pulsante sinistro.

Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICECursorButtonUp.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Evento CursorButtonDown**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Evento CursorDown**](inkcollector-cursordown.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaccia IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




