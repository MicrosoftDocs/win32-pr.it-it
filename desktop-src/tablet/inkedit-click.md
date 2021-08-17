---
description: Si verifica quando un utente fa clic sul controllo InkEdit.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: Evento InkEdit.Click (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f126035319c5d225da3fe57e075044c50f91f928277de89fce8e516e4723c701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718139"
---
# <a name="inkeditclick-event"></a>Evento InkEdit.Click

Si verifica quando un utente fa clic sul [controllo InkEdit.](inkedit-control-reference.md)

## <a name="syntax"></a>Sintassi


```C++
void Click();
```



## <a name="parameters"></a>Parametri

Questo evento non ha parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Facendo clic su un controllo vengono generati gli eventi [**MouseDown**](inkedit-mousedown.md) e [**MouseUp**](inkedit-mouseup.md) oltre all'evento Click.

> [!Note]  
> Per distinguere tra i pulsanti sinistro, destro e centrale del mouse, usare gli [**eventi MouseDown**](inkedit-mousedown.md) [**e MouseUp.**](inkedit-mouseup.md)

 

Se è presente codice nell'evento **Click,** l'evento [**DblClick**](inkedit-dblclick.md) non verrà mai attivato, perché l'evento **Click** è il primo evento da attivare tra i due. Di conseguenza, il clic del mouse viene intercettato dall'evento **Click,** quindi l'evento **DblClick** non si verifica.

Questo metodo di evento è definito **\_ nell'interfaccia IInkEditEvents.** **\_ L'interfaccia IInkEditEvents** implementa l'interfaccia IDispatch con un identificatore **di DISPID \_ IeeClick**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Inked.h (richiede anche \_ l'input penna i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> </dl>

 

 




