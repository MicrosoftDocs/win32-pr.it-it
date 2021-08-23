---
description: Si verifica prima che il controllo InkPicture ridisegni se stesso.
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: Evento InkPicture.Painting (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129e5f74ee8097794112b70fb709ab9b9a3b8fadc9f3e5a2fd7d874c65c0d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966970"
---
# <a name="inkpicturepainting-event"></a>Evento InkPicture.Painting

Si verifica prima [che il controllo InkPicture](inkpicture-control-reference.md) ridisegni se stesso.

## <a name="syntax"></a>Sintassi


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDC* \[ Pollici\]
</dt> <dd>

Contesto di dispositivo in cui verrà eseguito il disegno.

</dd> <dt>

*Rect* \[ Pollici\]
</dt> <dd>

Rettangolo di input penna da ridisegnare.

</dd> <dt>

*Consenti* \[ in, out\]
</dt> <dd>

Indica se verrà eseguito il ridisegno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce dispatch (dispatchinterface) **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con ID \_ DISPID IOEPainting.

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

 

 




