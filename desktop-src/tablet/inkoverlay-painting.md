---
description: Si verifica prima che l'oggetto InkOverlay o InkPicture abbia completato il ridisegno.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: Evento InkOverlay.Painting (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42075f6ae8641c895611196b80a904228cc27c45e5d84bdc798b5cc9242e7c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218943"
---
# <a name="inkoverlaypainting-event"></a>InkOverlay.Painting - evento

Si verifica prima [**che l'oggetto InkOverlay**](inkoverlay-class.md) [o InkPicture](inkpicture-control-reference.md) abbia completato il ridisegno.

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

Rettangolo da ridisegnare.

</dd> <dt>

*Consenti* \[ in, out\]
</dt> <dd>

Indica se si verificherà il ridisegno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID IOEPainting.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> </dl>

 

 




