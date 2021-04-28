---
description: "Evento InkPicture.SelectionMoving: si verifica quando la posizione della selezione corrente sta per cambiare, ad esempio tramite modifiche all'interfaccia utente, procedure taglia e incolla o proprietà Selection."
ms.assetid: 310003a1-f282-4efa-9a75-c575a9193a77
title: Evento InkPicture.SelectionMoving (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eee50fe1115ce72dff0674ad4e6c2457500c7de8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086459"
---
# <a name="inkpictureselectionmoving-event"></a>Evento InkPicture.SelectionMoving

Si verifica quando la posizione della selezione corrente sta per cambiare, ad esempio tramite modifiche all'interfaccia utente, procedure taglia e incolla o proprietà [**Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)

## <a name="syntax"></a>Sintassi


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CurSelectionRect* \[ Pollici\]
</dt> <dd>

Rettangolo in cui viene spostata la selezione dopo **l'evento SelectionMoving.**

> [!Note]  
> Questo rettangolo viene specificato nelle coordinate della finestra client, che consente scenari come la gestione delle proporzioni durante il ridimensionamento.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce di solo invio **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID \_ DISPID IOESelectionMoving.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC \[ Edition\]<br/>                                                       |
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

 

 




