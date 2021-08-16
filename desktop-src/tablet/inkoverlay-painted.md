---
description: Si verifica quando l'oggetto InkOverlay o il controllo InkPicture ha completato il ridisegno.
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: Evento InkOverlay.Painted (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f433f18d5e94be1163be519f4ee33fbe0b8d08a2e33feadd363a8eb3a43a6b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218935"
---
# <a name="inkoverlaypainted-event"></a>Evento InkOverlay.Painted

Si verifica quando [**l'oggetto InkOverlay**](inkoverlay-class.md) o [il controllo InkPicture](inkpicture-control-reference.md) ha completato il ridisegno.

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

Questo metodo di evento è definito nelle interfacce di solo invio \_ (dispatchinterface) IInkOverlayEvents e \_ IInkPictureEvents con ID DISPID \_ IOEPainted.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> </dl>

 

 




