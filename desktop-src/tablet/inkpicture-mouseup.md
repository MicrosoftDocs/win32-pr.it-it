---
description: Si verifica quando il puntatore del mouse viene spostato sul controllo InkPicture e viene rilasciato un pulsante del mouse.
ms.assetid: 5e49acc8-1ce1-45ff-b87c-04bdc653156a
title: Evento InkPicture. MouseUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf652e1ad4110afb4819e5326a5a19a894a310a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313934"
---
# <a name="inkpicturemouseup-event"></a>Evento InkPicture. MouseUp

Si verifica quando il puntatore del mouse viene spostato sul controllo [InkPicture](inkpicture-control-reference.md) e viene rilasciato un pulsante del mouse.

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

*Pulsante* \[ in\]
</dt> <dd>

Pulsante premuto.

</dd> <dt>

*Sposta* \[ in\]
</dt> <dd>

Stato del tasto MAIUSC.

</dd> <dt>

*px* \[ in\]
</dt> <dd>

Coordinata x, espressa in pixel, dell'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*py* \[ in\]
</dt> <dd>

Coordinata y, in pixel, dell'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*Annulla* \[ in uscita\]
</dt> <dd>

**Variante \_ TRUE** per annullare l'evento MouseUp per il controllo padre. in caso contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

> [!Note]  
> I parametri *px* e *py* sono in pixel e non le unità HIMETRIC associate al sistema di coordinate dello spazio di input penna. Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione che non è compatibile con la penna e che il tipo di applicazione fa riferimento solo ai pixel.

 

> [!Caution]  
> Alcuni controlli si basano su una relazione specifica tra gli eventi [**MouseDown**](inkpicture-mousedown.md), [**MouseMove**](inkpicture-mousemove.md)e **MouseUp** . L'annullamento di alcuni di questi eventi potrebbe avere risultati imprevisti.

 

Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** . L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IPEMouseDown.

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

 

