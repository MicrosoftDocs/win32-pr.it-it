---
description: Si verifica prima che l'oggetto InkOverlay o InkPicture abbia completato il ridisegno.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: Evento InkOverlay. painting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc056667f88c0631e84a76767fc97f90ca05a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529904"
---
# <a name="inkoverlaypainting-event"></a>Evento InkOverlay. painting

Si verifica prima che l'oggetto [**InkOverlay**](inkoverlay-class.md) o [InkPicture](inkpicture-control-reference.md) abbia completato il ridisegno.

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

*HDC* \[ in\]
</dt> <dd>

Contesto di dispositivo in cui si verificherà il disegno.

</dd> <dt>

*Rect* \[ in\]
</dt> <dd>

Rettangolo da ridisegnare.

</dd> <dt>

*Consenti* \[ in uscita\]
</dt> <dd>

Indica se si verificherà il ridisegno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle \_ interfacce IInkOverlayEvents e \_ IInkPictureEvents dispatch-only (dispinterfaces) con ID DISPID \_ IOEPainting.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**InkOverlay (classe)**](inkoverlay-class.md)
</dt> </dl>

 

 




