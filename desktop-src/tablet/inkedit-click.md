---
description: Si verifica quando un utente fa clic sul controllo InkEdit.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: Evento InkEdit. Click (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316851"
---
# <a name="inkeditclick-event"></a>Evento InkEdit. Click

Si verifica quando un utente fa clic sul controllo [InkEdit](inkedit-control-reference.md) .

## <a name="syntax"></a>Sintassi


```C++
void Click();
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Se si fa clic su un controllo, vengono generati eventi [**MouseDown**](inkedit-mousedown.md) e [**MouseUp**](inkedit-mouseup.md) oltre all'evento click.

> [!Note]  
> Per distinguere tra i pulsanti sinistro, destro e centrale del mouse, utilizzare gli eventi [**MouseDown**](inkedit-mousedown.md) e [**MouseUp**](inkedit-mouseup.md) .

 

Se nell'evento **Click** è presente codice, l'evento [**DblClick**](inkedit-dblclick.md) non verrà mai attivato, perché l'evento **Click** è il primo evento da attivare tra i due. Di conseguenza, il clic del mouse viene intercettato dall'evento **Click** , quindi l'evento **DblClick** non viene eseguito.

Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** . L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia IDispatch con un identificatore di **DISPID \_ IeeClick**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Inchiostrato. h (richiede anche il \_ . c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




