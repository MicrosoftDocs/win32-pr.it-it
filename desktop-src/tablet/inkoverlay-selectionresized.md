---
description: "Evento InkOverlay.SelectionResized: si verifica quando le dimensioni della selezione corrente sono state modificate, ad esempio tramite modifiche all'interfaccia utente, alle procedure di taglia e incolla o alla proprietà Selection."
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: Evento InkOverlay.SelectionResized (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f3dd3cf1bdda004733dde99bb66150710044310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116879"
---
# <a name="inkoverlayselectionresized-event"></a>Evento InkOverlay.SelectionResized

Si verifica quando le dimensioni della selezione corrente sono cambiate, ad esempio tramite modifiche all'interfaccia utente, alle procedure taglia e incolla o [**alla proprietà**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) Selection.

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

Rettangolo di delimitazione della raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selezionata così come esisteva prima della **generazione dell'evento SelectionResized.**

> [!Note]  
> Questo rettangolo viene specificato nelle coordinate dello spazio input penna, che consente scenari di annullamento.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce \_ dispatch (dispatchinterface) IInkOverlayEvents e \_ IInkPictureEvents con ID \_ DISPID IOESelectionResized.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Proprietà Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[**Classe InkRectangle**](inkrectangle-class.md)
</dt> </dl>

 

