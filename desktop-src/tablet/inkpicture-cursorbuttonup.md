---
description: "Evento InkPicture.CursorButtonUp: si verifica quando InkCollector rileva un pulsante del cursore verso l'alto."
ms.assetid: bb10b032-a88d-4b52-9062-c0b63dfe98e9
title: Evento InkPicture.CursorButtonUp (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639d0cbd89e2ca44d8855b6508c5284f59a7c654
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086659"
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

Oggetto [**interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **CursorButtonUp.**

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
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC \[ Edition\]<br/>                                                       |
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

 

 




