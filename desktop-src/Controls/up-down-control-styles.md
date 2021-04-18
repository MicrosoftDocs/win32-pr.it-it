---
title: Stili del controllo Up-Down (CommCtrl. h)
description: Questa sezione elenca gli stili usati per la creazione di controlli di scorrimento.
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
ms.openlocfilehash: 9b27cd27123f4c1a071314fd20d1874e61b590d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330432"
---
# <a name="up-down-control-styles"></a>Stili del controllo Up-Down

Questa sezione elenca gli stili usati per la creazione di controlli di scorrimento.



| Costante                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UDS_ALIGNLEFT"></span><span id="uds_alignleft"></span><dl> <dt>**\_ALIGNLEFT UDS**</dt> </dl>       | Posiziona il controllo di scorrimento accanto al bordo sinistro della finestra di contatto. La finestra di Buddy viene spostata a destra e la relativa larghezza viene ridotta per adattarsi alla larghezza del controllo di scorrimento.<br/>                                                                                                                                                                                                   |
| <span id="UDS_ALIGNRIGHT"></span><span id="uds_alignright"></span><dl> <dt>**\_ALIGNRIGHT UDS**</dt> </dl>    | Posiziona il controllo di scorrimento accanto al bordo destro della finestra di contatto. La larghezza della finestra di Buddy viene ridotta per adattarsi alla larghezza del controllo di scorrimento.<br/>                                                                                                                                                                                                                          |
| <span id="UDS_ARROWKEYS"></span><span id="uds_arrowkeys"></span><dl> <dt>**\_ARROWKEYS UDS**</dt> </dl>       | Fa in modo che il controllo di scorrimento aumenti e decrementa la posizione quando vengono premuti i tasti freccia su e freccia giù.<br/>                                                                                                                                                                                                                                                                          |
| <span id="UDS_AUTOBUDDY"></span><span id="uds_autobuddy"></span><dl> <dt>**AutoBuddy UDS \_**</dt> </dl>       | Seleziona automaticamente la finestra precedente nell'ordine z come finestra buddy del controllo di scorrimento.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="UDS_HORZ"></span><span id="uds_horz"></span><dl> <dt>**\_orizzontalmente UDS**</dt> </dl>                      | Consente di fare in modo che le frecce del controllo di scorrimento facciano riferimento a sinistra e a destra anziché verso l'alto e il basso.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="UDS_HOTTRACK"></span><span id="uds_hottrack"></span><dl> <dt>**\_HOTTRACK UDS**</dt> </dl>          | Fa in modo che il controllo mostri il comportamento di "rilevamento a caldo". Ovvero evidenzia le frecce verso l'alto e verso il basso sul controllo mentre il puntatore passa su di essi. Questo stile richiede Windows 98 o Windows 2000. Se il sistema esegue Windows 95 o Windows NT 4,0, il flag viene ignorato. Per verificare se è abilitata la funzionalità di rilevamento attivo, chiamare [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/> |
| <span id="UDS_NOTHOUSANDS"></span><span id="uds_nothousands"></span><dl> <dt>**nomigliaia di UDS \_**</dt> </dl> | Non inserisce un separatore delle migliaia tra ogni tre cifre decimali. <br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="UDS_SETBUDDYINT"></span><span id="uds_setbuddyint"></span><dl> <dt>**\_SETBUDDYINT UDS**</dt> </dl> | Fa in modo che il controllo di scorrimento imposti il testo della finestra di Buddy (usando il messaggio di [**\_ testo WM**](/windows/desktop/winmsg/wm-settext) ) quando cambia la posizione. Il testo è costituito dalla posizione formattata come stringa decimale o esadecimale.<br/>                                                                                                                                                             |
| <span id="UDS_WRAP"></span><span id="uds_wrap"></span><dl> <dt>**incapsulamento di UDS \_**</dt> </dl>                      | Determina il "ritorno a capo" della posizione se viene incrementato o decrementato oltre la fine o l'inizio dell'intervallo.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

