---
description: Si verifica quando la selezione dell'input penna all'interno del controllo sta per cambiare, ad esempio tramite modifiche all'interfaccia utente, alle procedure di taglia e incolla o alla proprietà Selection.
ms.assetid: dffdb183-d363-40d3-81a2-d496433f7075
title: Evento InkOverlay.SelectionChanging (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb9b7fa52c4897c7e1152deff7636259e07e2768929223327243c2da0b59e362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218954"
---
# <a name="inkoverlayselectionchanging-event"></a>Evento InkOverlay.SelectionChanging

Si verifica quando la selezione dell'input penna all'interno del controllo sta per cambiare, ad esempio tramite modifiche all'interfaccia utente, alle procedure di taglia e incolla o alla [**proprietà Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)

## <a name="syntax"></a>Sintassi


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewSelection* \[ Pollici\]
</dt> <dd>

Nuova raccolta di [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) da selezionare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce \_ dispatch (dispatchinterface) IInkOverlayEvents e \_ IInkPictureEvents con ID \_ DISPID IOESelectionChanging.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Proprietà Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

