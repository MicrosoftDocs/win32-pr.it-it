---
description: Si verifica quando viene spostata la rotellina del mouse mentre il controllo InkPicture dispone dello stato attivo.
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: Evento InkPicture. MouseWheel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cab870f3a00b2aa0cea3c003993e2b35cd2abbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346111"
---
# <a name="inkpicturemousewheel-event"></a>Evento InkPicture. MouseWheel

Si verifica quando viene spostata la rotellina del mouse mentre il controllo [InkPicture](inkpicture-control-reference.md) dispone dello stato attivo.

## <a name="syntax"></a>Sintassi


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
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

*Delta* \[ in\]
</dt> <dd>

Distanza di spostamento della rotellina del mouse.

</dd> <dt>

*x* \[ in\]
</dt> <dd>

Coordinata x, espressa in pixel, dell'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*y* \[ in\]
</dt> <dd>

Coordinata y, in pixel, dell'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*Annulla* \[ in uscita\]
</dt> <dd>

VARIANT \_ true per annullare l'evento **MouseWheel** per il controllo padre; in caso contrario, VARIANT \_ false.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

> [!Note]  
> I parametri *x* e *y* sono in pixel e non le unità HIMETRIC associate al sistema di coordinate dello spazio di input penna. Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione che non è compatibile con la penna e che il tipo di applicazione fa riferimento solo ai pixel.

 

Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** . L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IPEMouseWheel.

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

 

