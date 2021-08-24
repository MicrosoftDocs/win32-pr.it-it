---
description: Si verifica prima dell'eliminazione dei tratti dalla proprietà Ink.
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: Evento InkOverlay.StrokesDeleting (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b85e01eabc46e8e9cc4ca844ae8f5efa8b58e83fdee2724792a3856445b7dbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712671"
---
# <a name="inkoverlaystrokesdeleting-event"></a>Evento InkOverlay.StrokesDeleting

Si verifica prima dell'eliminazione dei tratti dalla [**proprietà Ink.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)

## <a name="syntax"></a>Sintassi


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tratti* \[ Pollici\]
</dt> <dd>

Raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) eliminata quando viene generato l'evento **StrokesDeleting.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce \_ dispatch (dispatchinterface) IInkOverlayEvents e \_ IInkPictureEvents con ID DISPID \_ IOEStrokesDeleting.

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

[**Classe \[ InkCollector/InkOverLay della proprietà Ink\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)
</dt> </dl>

 

