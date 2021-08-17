---
description: "Evento InkPicture.SelectionResizing: si verifica quando le dimensioni della selezione corrente sta per cambiare, ad esempio tramite modifiche all'interfaccia utente, procedure di taglia e incolla o la proprietà Selection."
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: Evento InkPicture.SelectionResizing (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caeae852802599a401c1cdff97436672e0cbfe252f8f1e96d6f4c98367c828ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966960"
---
# <a name="inkpictureselectionresizing-event"></a>Evento InkPicture.SelectionResizing

Si verifica quando le dimensioni della selezione corrente sta per cambiare, ad esempio tramite modifiche all'interfaccia utente, alle procedure taglia e incolla o [**alla proprietà Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)

## <a name="syntax"></a>Sintassi


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CurSelectionRect* \[ Pollici\]
</dt> <dd>

Rettangolo di delimitazione della selezione dopo **l'evento SelectionResizing.**

> [!Note]  
> Questo rettangolo viene specificato nelle coordinate della finestra client, che consente scenari come la gestione delle proporzioni durante il ridimensionamento.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce dispatch (dispatchinterface) **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con ID \_ DISPID IOESelectionResizing.

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

 

 




