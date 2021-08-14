---
description: Si verifica quando la selezione dell'input penna all'interno del controllo InkPicture sta per cambiare, ad esempio tramite modifiche all'interfaccia utente, procedure di taglia e incolla o la proprietà Selection.
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: Evento InkPicture.SelectionChanging (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5960fd212b4362f697c1c83b1bc03729cb9d619081ee6c4895a01a7d7124dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118042063"
---
# <a name="inkpictureselectionchanging-event"></a>Evento InkPicture.SelectionChanging

Si verifica quando la selezione dell'input penna all'interno del controllo [InkPicture](inkpicture-control-reference.md) sta per cambiare, ad esempio tramite modifiche all'interfaccia utente, procedure di taglia e incolla o la [**proprietà Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)

## <a name="syntax"></a>Sintassi


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nuovaselezione* \[ Pollici\]
</dt> <dd>

Nuovo insieme di [inkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selezionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce di solo invio **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID \_ DISPID IOESelectionChanging.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**Controllo \[ InkPicture della proprietà Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> </dl>

 

