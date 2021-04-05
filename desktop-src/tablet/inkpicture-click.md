---
description: Si verifica quando un utente fa clic sul controllo InkPicture.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: Evento InkPicture. Click (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1dd90cd69555f65531f5ab2684f886dab23e191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884373"
---
# <a name="inkpictureclick-event"></a>Evento InkPicture. Click

Si verifica quando un utente fa clic sul controllo [InkPicture](inkpicture-control-reference.md) .

## <a name="syntax"></a>Sintassi


```C++
void Click();
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Se si fa clic su un controllo, vengono generati eventi [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) oltre all'evento click.

> [!Note]  
> Per distinguere tra i pulsanti sinistro, destro e centrale del mouse, utilizzare gli eventi [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) .

 

Se nell'evento **Click** è presente codice, l'evento [**DblClick**](inkpicture-dblclick.md) non verrà mai attivato, perché l'evento **Click** è il primo evento da attivare tra i due. Di conseguenza, il clic del mouse viene intercettato dall'evento **Click** , quindi l'evento **DblClick** non viene eseguito.

Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** . L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia IDispatch con un identificatore di **DISPID \_ IPEClick**.

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

 

 




