---
description: Si verifica prima che i tratti vengano eliminati dalla proprietà Ink.
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: Evento InkOverlay. StrokesDeleting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64422e61869c633514c3e219e3d090476a693dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968253"
---
# <a name="inkoverlaystrokesdeleting-event"></a>Evento InkOverlay. StrokesDeleting

Si verifica prima che i tratti vengano eliminati dalla proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .

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

Questo metodo di evento è definito nelle \_ interfacce IInkOverlayEvents e \_ IInkPictureEvents dispatch-only (dispinterfaces) con ID DISPID \_ IOEStrokesDeleting.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**InkOverlay (classe)**](inkoverlay-class.md)
</dt> <dt>

[**\[Classe InkCollector/InkOverLay della proprietà Ink\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)
</dt> </dl>

 

