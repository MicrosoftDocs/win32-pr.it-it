---
description: Si verifica prima dell'eliminazione degli oggetti IInkStrokeDisp dalla proprietà Ink.
ms.assetid: 747e0fdf-c68b-4805-bdc8-aa05e95ec0f7
title: Evento InkPicture. StrokesDeleting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef70e8526798f306f99c17b511b5c18c502858a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057990"
---
# <a name="inkpicturestrokesdeleting-event"></a>Evento InkPicture. StrokesDeleting

Si verifica prima dell'eliminazione degli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dalla proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .

## <a name="syntax"></a>Sintassi


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tratti* \[ in\]
</dt> <dd>

Raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) eliminata quando viene generato l'evento **StrokesDeleting** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch-only (dispinterfaces) con ID DISPID \_ IOEStrokesDeleting.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

