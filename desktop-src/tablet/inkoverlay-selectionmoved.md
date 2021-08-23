---
description: "Evento InkOverlay.SelectionMoved: si verifica quando la posizione della selezione corrente viene modificata, ad esempio tramite modifiche all'interfaccia utente, procedure taglia e incolla o proprietà Selection."
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: Evento InkOverlay.SelectionMoved (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141e1c9501a9670ebfa89cdcf30fac7a1044450cef932e7c7abb522a5199fd47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032069"
---
# <a name="inkoverlayselectionmoved-event"></a>Evento InkOverlay.SelectionMoved

Si verifica quando la posizione della selezione corrente viene modificata, ad esempio tramite modifiche all'interfaccia utente, procedure taglia e incolla o proprietà [**Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)

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

Rettangolo di delimitazione della raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selezionata esistente prima che venga generato **l'evento SelectionMoved.**

> [!Note]  
> Questo rettangolo viene specificato nelle coordinate dello spazio input penna, che consente scenari di annullamento.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID IOESelectionMoved.

Per ottenere il nuovo rettangolo di delimitazione della raccolta di tratti spostati, chiama il [**metodo Selection.GetBoundingBox.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
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

 

