---
description: Si verifica quando la selezione dell'input penna all'interno del controllo viene modificata, ad esempio tramite modifiche all'interfaccia utente, alle procedure di taglia e incolla o alla proprietà Selection.
ms.assetid: 6b4cd9fe-b09f-4a70-9aa5-92ef9409ff1b
title: Evento InkOverlay.SelectionChanged (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11bbe4e239b1100277adea0b784a93bf16bf8497cfd8dd44877f7fe7e3fd7652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218974"
---
# <a name="inkoverlayselectionchanged-event"></a>Evento InkOverlay.SelectionChanged

Si verifica quando la selezione dell'input penna all'interno del controllo viene modificata, ad esempio tramite modifiche all'interfaccia utente, alle procedure di taglia e incolla o [**alla proprietà Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)

## <a name="syntax"></a>Sintassi


```C++
void SelectionChanged();
```



## <a name="parameters"></a>Parametri

Questo evento non ha parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Non sono presenti dati dell'evento.

Questo metodo di evento è definito nelle interfacce di solo invio \_ (dispatchinterface) IInkOverlayEvents e \_ IInkPictureEvents con ID \_ DISPID IOESelectionChanged.

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

 

 




