---
description: Si verifica dopo l'eliminazione di oggetti IInkStrokeDisp dalla proprietà Ink.
ms.assetid: 395544e1-dc93-45d3-ac7a-d54712f3c027
title: Evento InkPicture.StrokesDeleted (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b2d4f0be69adf6c9c44f3eadec250d8cba3ebb8935bde5c06cd026e478da3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717360"
---
# <a name="inkpicturestrokesdeleted-event"></a>Evento InkPicture.StrokesDeleted

Si verifica [**dopo l'eliminazione di oggetti IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dalla [**proprietà Ink.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink)

## <a name="syntax"></a>Sintassi


```C++
void StrokesDeleted();
```



## <a name="parameters"></a>Parametri

Questo evento non ha parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Non sono presenti dati dell'evento.

Questo metodo di evento è definito nelle interfacce di solo invio **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispatchinterfaces) con ID \_ DISPID IOEStrokesDeleted.

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
</dt> </dl>

 

 




