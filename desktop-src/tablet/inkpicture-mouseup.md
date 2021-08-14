---
description: Si verifica quando il puntatore del mouse viene spostato sul controllo InkPicture e viene rilasciato un pulsante del mouse.
ms.assetid: 5e49acc8-1ce1-45ff-b87c-04bdc653156a
title: Evento InkPicture.MouseUp (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec780348191a4bfe8d0aadb0ad075a3784f49f23504c7dc02ca5f6da14c0d54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218378"
---
# <a name="inkpicturemouseup-event"></a>Evento InkPicture.MouseUp

Si verifica quando il puntatore del mouse viene spostato [sul controllo InkPicture](inkpicture-control-reference.md) e viene rilasciato un pulsante del mouse.

## <a name="syntax"></a>Sintassi


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pulsante* \[ Pollici\]
</dt> <dd>

Pulsante premuto.

</dd> <dt>

*MAIUSC* \[ Pollici\]
</dt> <dd>

Stato del tasto MAIUSC.

</dd> <dt>

*pX* \[ Pollici\]
</dt> <dd>

Coordinata x, in pixel, [**dell'oggetto IInkCursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

</dd> <dt>

*pY* \[ Pollici\]
</dt> <dd>

Coordinata y, in pixel, [**dell'oggetto IInkCursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

</dd> <dt>

*Annulla* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** per annullare l'evento MouseUp per il controllo padre. in caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

> [!Note]  
> I parametri *pX* e *pY* sono in pixel e non le unità HIMETRIC associate al sistema di coordinate dello spazio input penna. Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione che non supporta la penna e tale tipo di applicazione fa riferimento solo ai pixel.

 

> [!Caution]  
> Alcuni controlli si basano su una relazione specifica tra gli eventi [**MouseDown,**](inkpicture-mousedown.md) [**MouseMove**](inkpicture-mousemove.md) **e MouseUp.** L'annullamento di alcuni di questi eventi può avere risultati imprevisti.

 

Questo metodo di evento è definito **\_ nell'interfaccia IInkPictureEvents.** **\_ L'interfaccia IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore \_ DISPID IPEMouseDown.

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
</dt> </dl>

 

