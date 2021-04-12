---
description: Si verifica quando si fa doppio clic sul controllo InkPicture.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: Evento InkPicture. DblClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c3d9bb9125c8142186da969acf6ce03f5f76b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347886"
---
# <a name="inkpicturedblclick-event"></a>Evento InkPicture. DblClick

Si verifica quando si fa doppio clic sul controllo [InkPicture](inkpicture-control-reference.md) .

## <a name="syntax"></a>Sintassi


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Annulla* \[ in uscita\]
</dt> <dd>

Indica se l'evento deve essere annullato per il controllo padre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per distinguere tra i pulsanti sinistro, destro e centrale del mouse, utilizzare gli eventi [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) . Se nell'evento [**Click**](inkpicture-click.md) è presente codice, l'evento **DblClick** non verrà mai attivato.

 

Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** . L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia IDispatch con un identificatore di **DISPID \_ IPEDblClick**.

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

 

 




