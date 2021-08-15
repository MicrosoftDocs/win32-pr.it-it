---
description: "Evento InkPicture.SelectionResized: si verifica quando le dimensioni della selezione corrente sono state modificate, ad esempio tramite modifiche all'interfaccia utente, alle procedure di taglia e incolla o alla proprietà Selection."
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: Evento InkPicture.SelectionResized (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e67bc19d4d35c356e0774f0843ba62432606c1ee4f1f84095e64c4808d09bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451055"
---
# <a name="inkpictureselectionresized-event"></a>Evento InkPicture.SelectionResized

Si verifica quando le dimensioni della selezione corrente sono cambiate, ad esempio tramite modifiche all'interfaccia utente, alle procedure taglia e incolla o [**alla proprietà**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) Selection.

## <a name="syntax"></a>Sintassi


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OldSelectionRect* \[ Pollici\]
</dt> <dd>

Rettangolo di delimitazione della raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selezionata così come esisteva prima che venga generato **l'evento SelectionResized.**

> [!Note]  
> Questo rettangolo viene specificato nelle coordinate dello spazio input penna, che consente scenari di annullamento.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce dispatch (dispatchinterface) **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con ID \_ DISPID IOESelectionResized.

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
</dt> <dt>

[**Controllo \[ InkPicture della proprietà Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> <dt>

[**Classe InkRectangle**](inkrectangle-class.md)
</dt> </dl>

 

