---
title: Comportamenti di hit testing tocco
description: Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare la modalità di elaborazione dei messaggi per l'hit testing di tocco da parte di Windows registrate tramite la funzione RegisterTouchHitTestingWindow.
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302207"
---
# <a name="touch-hit-testing-behaviors"></a>Comportamenti di hit testing tocco

Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare la modalità di elaborazione dei messaggi per l'hit testing di tocco da parte di Windows registrate tramite la funzione [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .

| Costante/valore | Descrizione |
|---|---|
| **TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0x0) | Indica che i messaggi di [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) non vengono inviati alla finestra di destinazione, ma vengono inviati alle finestre figlio.<br/> |
| **TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)    | Indica che [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messaggi vengono inviati alla finestra di destinazione.<br/>                                   |
| **TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0x2)          | Indica che i messaggi di [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) non vengono inviati alla finestra di destinazione o alle finestre figlio.<br/>              |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Winuser. h |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti](constants.md)
