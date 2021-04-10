---
description: Si verifica quando la selezione dell'input penna all'interno del controllo InkPicture sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di selezione.
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: Evento InkPicture. SelectionChanging (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b8a35d57aeb9367bb9d30647cb074a7e0e6fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884933"
---
# <a name="inkpictureselectionchanging-event"></a>Evento InkPicture. SelectionChanging

Si verifica quando la selezione dell'input penna all'interno del controllo [InkPicture](inkpicture-control-reference.md) sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .

## <a name="syntax"></a>Sintassi


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewSelection* \[ in\]
</dt> <dd>

Nuova raccolta di [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) in corso di selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch-only (dispinterfaces) con ID DISPID \_ IOESelectionChanging.

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
</dt> <dt>

[**Controllo InkPicture della proprietà Selection \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> </dl>

 

