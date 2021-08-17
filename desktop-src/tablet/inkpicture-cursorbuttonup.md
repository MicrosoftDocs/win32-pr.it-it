---
description: "Evento InkPicture.CursorButtonUp: si verifica quando InkCollector rileva un pulsante del cursore verso l'alto."
ms.assetid: bb10b032-a88d-4b52-9062-c0b63dfe98e9
title: Evento InkPicture.CursorButtonUp (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a84a5d8529ecf6387d3832608ae3821be9d317fef46211a6824bddc2ee9574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451080"
---
# <a name="inkpicturecursorbuttonup-event"></a>Evento InkPicture.CursorButtonUp

Si verifica quando [**InkCollector rileva**](inkcollector-class.md) un pulsante del cursore verso l'alto.

## <a name="syntax"></a>Sintassi


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cursore* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **CursorButtonUp.**

</dd> <dt>

*Pulsante* \[ Pollici\]
</dt> <dd>

Pulsante rilasciato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Un pulsante sulla punta di una penna è in alto quando l'utente completa un tratto e solleva la penna dal digitalizzatore. Quando il pulsante non è premuto, è disponibile un pulsante su una freccia verso l'alto.

Quando si rilascia il pulsante destro del mouse, si ricevono effettivamente due eventi **CursorButtonUp:** uno per il pulsante destro verso l'alto e uno per il pulsante sinistro in alto.

Questo metodo di evento è definito nelle interfacce dispatch **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con ID \_ DISPID ICECursorButtonUp.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**Evento CursorButtonDown**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**Evento CursorDown**](inkpicture-cursordown.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaccia IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




