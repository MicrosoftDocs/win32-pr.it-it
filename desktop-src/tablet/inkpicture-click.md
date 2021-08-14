---
description: Si verifica quando un utente fa clic sul controllo InkPicture.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: Evento InkPicture.Click (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ebde47609a36a92eca211f597345a9784fca03f66076ebb4db6f04ee6f5936
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218540"
---
# <a name="inkpictureclick-event"></a>Evento InkPicture.Click

Si verifica quando un utente fa clic sul [controllo InkPicture.](inkpicture-control-reference.md)

## <a name="syntax"></a>Sintassi


```C++
void Click();
```



## <a name="parameters"></a>Parametri

Questo evento non ha parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Facendo clic su un controllo vengono generati gli eventi [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) oltre all'evento Click.

> [!Note]  
> Per distinguere tra i pulsanti sinistro, destro e centrale del mouse, usare gli [**eventi MouseDown**](inkpicture-mousedown.md) [**e MouseUp.**](inkpicture-mouseup.md)

 

Se è presente codice nell'evento **Click,** l'evento [**DblClick**](inkpicture-dblclick.md) non verrà mai attivato, perché l'evento **Click** è il primo evento da attivare tra i due. Di conseguenza, il clic del mouse viene intercettato dall'evento **Click,** quindi l'evento **DblClick** non si verifica.

Questo metodo di evento è definito **\_ nell'interfaccia IInkPictureEvents.** **\_ L'interfaccia IInkPictureEvents** implementa l'interfaccia IDispatch con un identificatore **DISPID \_ IPEClick**.

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

 

 




