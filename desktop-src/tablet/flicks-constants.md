---
description: Di seguito sono riportate le costanti di gesti rapidi.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Scorre le costanti (Tabflicks. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9a83f9a35a2c1a9cbd7c4b048a8c985f5eea34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129535"
---
# <a name="flicks-constants"></a>Costanti rapide

Di seguito sono riportate le costanti di gesti rapidi.



| Costante/valore                                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <dt>**Gesto rapido \_ 0x1 \_ \_ maschera gestita WM**</dt> <dt></dt> </dl> | Valore da restituire dopo la gestione del messaggio del [**\_ messaggio del messaggio di \_ scorrimento del Tablet WM**](wm-tablet-flick-message.md) . Se viene restituita la **\_ \_ \_ maschera gestibile con scorrimento rapido** , non viene eseguita alcuna azione. In caso contrario, Windows invia notifiche di completamento, ad esempio [**WM \_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)o [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown), a seconda dell'azione associata al gesto rapido della penna. <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> Numero di <dt>**\_ \_Direzioni di scorrimento**</dt> <dt>8</dt> </dl>       | Il numero di direzioni definito nell'enumerazione [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) .<br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Tabflicks. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Enumerazione FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[**\_Messaggio di \_ scorrimento rapido del Tablet WM**](wm-tablet-flick-message.md)
</dt> <dt>

[Movimenti rapidi](flicks-gestures.md)
</dt> <dt>

[Risposta ai gesti rapidi della penna](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

