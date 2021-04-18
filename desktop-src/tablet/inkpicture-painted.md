---
description: Si verifica quando il controllo InkPicture ha completato il ridisegno.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: Evento InkPicture. Painted (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313926"
---
# <a name="inkpicturepainted-event"></a>Evento InkPicture. Painted

Si verifica quando il controllo [InkPicture](inkpicture-control-reference.md) ha completato il ridisegno.

## <a name="syntax"></a>Sintassi


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HDC* \[ in\]
</dt> <dd>

Contesto di dispositivo in cui si è verificato l'evento.

</dd> <dt>

*Rect* \[ in\]
</dt> <dd>

[**InkRectangle**](inkrectangle-class.md) ridisegnato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento viene definito in **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispinterfaces con ID DISPID \_ IOEPainted.

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
</dt> </dl>

 

 




