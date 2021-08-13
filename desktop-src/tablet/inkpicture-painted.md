---
description: Si verifica quando il controllo InkPicture ha completato il ridisegno stesso.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: Evento InkPicture.Painted (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201027ba2626cd3a3dd8d76a8794a1a5430785e0e1602633ee9f39ac36caa023
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451057"
---
# <a name="inkpicturepainted-event"></a>Evento InkPicture.Painted

Si verifica quando [il controllo InkPicture](inkpicture-control-reference.md) ha completato il ridisegno stesso.

## <a name="syntax"></a>Sintassi


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDC* \[ Pollici\]
</dt> <dd>

Contesto di dispositivo in cui si è verificato l'evento.

</dd> <dt>

*Rect* \[ Pollici\]
</dt> <dd>

[**InkRectangle**](inkrectangle-class.md) ridisegnato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce dispatch **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con ID \_ DISPID IOEPainted.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




