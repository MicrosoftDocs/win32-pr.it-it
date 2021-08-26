---
description: Si verifica quando la selezione dell'input penna all'interno del controllo InkPicture viene modificata, ad esempio tramite modifiche all'interfaccia utente, procedure di taglia e incolla o la proprietà Selection.
ms.assetid: e300ec91-e8f3-473f-b526-efeafafaa32a
title: Evento InkPicture.SelectionChanged (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a1fce27d9aa0dd043c5e474d790c1bd9737a9c10bffbed3eff6a287be67030f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939001"
---
# <a name="inkpictureselectionchanged-event"></a>Evento InkPicture.SelectionChanged

Si verifica quando la selezione dell'input penna all'interno del controllo [InkPicture](inkpicture-control-reference.md) viene modificata, ad esempio tramite modifiche all'interfaccia utente, procedure di taglia e incolla o la [**proprietà Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)

## <a name="syntax"></a>Sintassi


```C++
void SelectionChanged();
```



## <a name="parameters"></a>Parametri

Questo evento non ha parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Per altri dettagli su questo evento, fare riferimento all'evento [**SelectionChanged**](inkoverlay-selectionchanged.md) dell'oggetto [**InkOverlay,**](inkoverlay-class.md) che ha la stessa funzionalità.

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

 

 




