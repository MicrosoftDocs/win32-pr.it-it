---
title: Up-Down di controllo (CommCtrl.h)
description: Questa sezione elenca gli stili usati durante la creazione di controlli up-down.
ms.assetid: d35198cb-6a5b-485e-a914-1b2ede53462f
topic_type:
- apiref
api_name:
- UDS_ALIGNLEFT
- UDS_ALIGNRIGHT
- UDS_ARROWKEYS
- UDS_AUTOBUDDY
- UDS_HORZ
- UDS_HOTTRACK
- UDS_NOTHOUSANDS
- UDS_SETBUDDYINT
- UDS_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809ab4ce2c4d8670363dc7f0751ae4a3756ee7b4e5dc9b75c79986c3a56d359d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957700"
---
# <a name="up-down-control-styles"></a>Up-Down di controllo

Questa sezione elenca gli stili usati durante la creazione di controlli up-down.



| Costante                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UDS_ALIGNLEFT"></span><span id="uds_alignleft"></span><dl> <dt>**UDS \_ ALIGNLEFT**</dt> </dl>       | Posiziona il controllo verso l'alto accanto al bordo sinistro della finestra dell'amico. La finestra dell'amico viene spostata a destra e la relativa larghezza viene ridotta in base alla larghezza del controllo verso l'alto.<br/>                                                                                                                                                                                                   |
| <span id="UDS_ALIGNRIGHT"></span><span id="uds_alignright"></span><dl> <dt>**UDS \_ ALIGNRIGHT**</dt> </dl>    | Posiziona il controllo verso l'alto verso il basso accanto al bordo destro della finestra dell'amico. La larghezza della finestra dell'amico viene ridotta in base alla larghezza del controllo verso l'alto.<br/>                                                                                                                                                                                                                          |
| <span id="UDS_ARROWKEYS"></span><span id="uds_arrowkeys"></span><dl> <dt>**TASTI DI \_ DIREZIONE UDS**</dt> </dl>       | Determina l'incremento e la decrementazione della posizione del controllo verso l'alto quando vengono premuti i tasti FRECCIA SU e FRECCIA GIÙ.<br/>                                                                                                                                                                                                                                                                          |
| <span id="UDS_AUTOBUDDY"></span><span id="uds_autobuddy"></span><dl> <dt>**UDS \_ AUTOBUDDY**</dt> </dl>       | Seleziona automaticamente la finestra precedente nell'ordine z come finestra degli amici del controllo up-down.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="UDS_HORZ"></span><span id="uds_horz"></span><dl> <dt>**UDS \_ HORZ**</dt> </dl>                      | Fa in modo che le frecce verso l'alto verso il basso del controllo puntino verso sinistra e verso destra anziché verso l'alto e verso il basso.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="UDS_HOTTRACK"></span><span id="uds_hottrack"></span><dl> <dt>**HOTTRACK DI UDS \_**</dt> </dl>          | Fa sì che il controllo esererà un comportamento di "rilevamento a caldo". In questo modo vengono evidenziate le frecce SU e FRECCIA GIÙ sul controllo quando il puntatore passa sopra di essi. Questo stile richiede Windows 98 o Windows 2000. Se il sistema esegue Windows 95 o Windows NT 4.0, il flag viene ignorato. Per verificare se il rilevamento a caldo è abilitato, chiamare [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/> |
| <span id="UDS_NOTHOUSANDS"></span><span id="uds_nothousands"></span><dl> <dt>**UDS \_ NOTHOUSANDS**</dt> </dl> | Non inserisce un separatore delle migliaia tra tre cifre decimali. <br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="UDS_SETBUDDYINT"></span><span id="uds_setbuddyint"></span><dl> <dt>**UDS \_ SETBUDDYINT**</dt> </dl> | Determina l'impostazione del testo della finestra del controllo verso l'alto (usando il messaggio [**WM \_ SETTEXT)**](/windows/desktop/winmsg/wm-settext) quando la posizione cambia. Il testo è costituito dalla posizione formattata come stringa decimale o esadecimale.<br/>                                                                                                                                                             |
| <span id="UDS_WRAP"></span><span id="uds_wrap"></span><dl> <dt>**WRAPPING DEI TIPI DEFINITI \_ DALL'UTENTE**</dt> </dl>                      | Determina il ritorno a capo della posizione se viene incrementata o decrementata oltre la fine o l'inizio dell'intervallo.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

