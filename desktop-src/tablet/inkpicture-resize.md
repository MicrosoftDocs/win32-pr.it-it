---
description: Si verifica quando il controllo InkPicture viene ridimensionato (quando cambiano i valori della proprietà Width e/o Height).
ms.assetid: 436db420-f9ea-46f1-b922-c8663371edd5
title: Evento InkPicture. Resize (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4c5df298658f6ac98ddbf8fc00873f6f22dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057992"
---
# <a name="inkpictureresize-event"></a>Evento InkPicture. Resize

Si verifica quando il controllo [InkPicture](inkpicture-control-reference.md) viene ridimensionato (quando cambiano i valori della proprietà Width e/o Height).

## <a name="syntax"></a>Sintassi


```C++
void Resize(
   long Left,
   long Top,
   long Right,
   long Bottom
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Sinistra* 
</dt> <dd>

Il numero di pixel del lato sinistro della finestra che contiene il controllo a sinistra del controllo.

</dd> <dt>

*Top* 
</dt> <dd>

Il numero di pixel dalla parte superiore della finestra che contiene il controllo nella parte superiore del controllo.

</dd> <dt>

*Ok* 
</dt> <dd>

Il numero di pixel dal lato sinistro della finestra che contiene il controllo sul lato destro del controllo.

</dd> <dt>

*Ultimo* 
</dt> <dd>

Il numero di pixel dalla parte superiore della finestra che contiene il controllo nella parte inferiore del controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

La nuova larghezza del controllo in pixel sarà uguale alla differenza tra i parametri *destro* e *sinistro* . Analogamente, la nuova altezza sarà uguale alla differenza tra *Bottom* e *Top*.

Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** . L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia IDispatch con un identificatore di **DISPID \_ IPEResize**.

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

 

 




