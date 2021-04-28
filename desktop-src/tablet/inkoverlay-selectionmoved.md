---
description: "Evento InkOverlay.SelectionMoved: si verifica quando la posizione della selezione corrente è stata modificata, ad esempio tramite modifiche all'interfaccia utente, alle procedure taglia e incolla o alla proprietà Selection."
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: Evento InkOverlay.SelectionMoved (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27bf1600683b5258bf899692b692c8cdcabb359
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116869"
---
# <a name="inkoverlayselectionmoved-event"></a>Evento InkOverlay.SelectionMoved

Si verifica quando la posizione della selezione corrente è stata modificata, ad esempio tramite modifiche all'interfaccia utente, alle procedure taglia e incolla o [**alla proprietà Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)

## <a name="syntax"></a>Sintassi


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OldSelectionRect* \[ Pollici\]
</dt> <dd>

Rettangolo di delimitazione della raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selezionata così come esisteva prima della generazione **dell'evento SelectionMoved.**

> [!Note]  
> Questo rettangolo viene specificato nelle coordinate dello spazio input penna, che consente scenari di annullamento.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento È definito nelle interfacce di solo invio \_ IInkOverlayEvents e \_ IInkPictureEvents (dispatchinterfaces) con ID \_ DISPID IOESelectionMoved.

Per ottenere il nuovo rettangolo di delimitazione della raccolta di tratti spostati, chiamare il [**metodo Selection.GetBoundingBox.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)

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

 

