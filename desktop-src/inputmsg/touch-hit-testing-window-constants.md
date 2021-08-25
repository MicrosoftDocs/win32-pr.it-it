---
title: Costanti della finestra di hit testing tocco
description: Indica il modo in cui i messaggi per l'hit testing tramite tocco vengono elaborati da finestre registrate tramite la funzione RegisterTouchHitTestingWindow.
ms.assetid: CC6CCD0B-882F-4DA7-B886-D4BD18D6060C
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
ms.date: 02/03/2020
ms.openlocfilehash: ccc26947241d5d777cacee504a066b7e070faf0a8febc39b86571537c14245f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829751"
---
# <a name="touch-hit-testing-window-constants"></a>Costanti della finestra di hit testing tocco

Indica il modo in cui i messaggi per l'hit testing tramite tocco vengono elaborati da finestre registrate tramite la [**funzione RegisterTouchHitTestingWindow.**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)



| Costante/valore                                                                                                                                                                                                                                                   | Descrizione                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TOUCH_HIT_TESTING_DEFAULT"></span><span id="touch_hit_testing_default"></span><dl> <dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt> </dl> | [**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messaggi non vengono inviati alla finestra di destinazione, ma alle finestre figlio.<br/> |
| <span id="TOUCH_HIT_TESTING_CLIENT"></span><span id="touch_hit_testing_client"></span><dl> <dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt> </dl>    | [**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messaggi vengono inviati alla finestra di destinazione.<br/>                                   |
| <span id="TOUCH_HIT_TESTING_NONE"></span><span id="touch_hit_testing_none"></span><dl> <dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt> </dl>          | [**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messaggi non vengono inviati alla finestra di destinazione o alle finestre figlio.<br/>              |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 solo \[ app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2012 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

