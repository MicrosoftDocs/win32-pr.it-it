---
description: Di seguito sono riportate le costanti Flicks.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Costanti Flicks (Tabflicks.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e927d0715c9f34e7e1db979c32545a0d8c8efad18186192a751f2cdbed13172
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092648"
---
# <a name="flicks-constants"></a>Costanti di Flicks

Di seguito sono riportate le costanti Flicks.



| Costante/valore                                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <dt>**FLICK \_ MASCHERA \_ GESTITA \_ WM**</dt> <dt>0x1</dt> </dl> | Valore da restituire dopo la gestione del [**messaggio WM TABLET FLICK \_ \_ Message.**](wm-tablet-flick-message.md) Se **viene \_ restituito FLICK WM \_ HANDLED \_ MASK,** non viene eseguita alcuna altra azione. In caso contrario, Windows notifiche di follow-up, ad esempio [**WM \_ APPCOMMAND,**](/windows/desktop/inputdev/wm-appcommand) [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)o [**WM \_ KEYDOWN,**](/windows/desktop/inputdev/wm-keydown)a seconda dell'azione associata allo scorrimento della penna. <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <dt>**NUM \_ FLICK \_ DIRECTIONS**</dt> <dt>8</dt> </dl>       | Numero di direzioni definite [**nell'enumerazione FLICKDIRECTION.**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)<br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Tabflicks.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Enumerazione FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[**MESSAGGIO FLICK \_ PER TABLET \_ WM**](wm-tablet-flick-message.md)
</dt> <dt>

[Movimenti di Scorrimento rapido](flicks-gestures.md)
</dt> <dt>

[Risposta ai gesti rapidi della penna](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

