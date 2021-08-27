---
title: Stili del controllo Calendario mensile (CommCtrl.h)
description: Le costanti di stile seguenti vengono usate durante la creazione di controlli calendario mensile.
ms.assetid: 8d9b2239-fd13-4579-81a2-0385fd318e83
topic_type:
- apiref
api_name:
- MCS_DAYSTATE
- MCS_MULTISELECT
- MCS_WEEKNUMBERS
- MCS_NOTODAYCIRCLE
- MCS_NOTODAY
- MCS_NOTRAILINGDATES
- MCS_SHORTDAYSOFWEEK
- MCS_NOSELCHANGEONNAV
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d236526792d4b965f58dc6c188add6a257845bcb8450e84f4b691849acb493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061851"
---
# <a name="month-calendar-control-styles"></a>Stili del controllo Calendario mensile

Le costanti di stile seguenti vengono usate durante la creazione di controlli calendario mensile.



| Costante                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <dt>**MCS \_ DAYSTATE**</dt> </dl>                         | [Versione 4.70.](common-control-versions.md) Il calendario mensile invia [notifiche \_ MCN GETDAYSTATE](mcn-getdaystate.md) per richiedere informazioni sui giorni da visualizzare in grassetto.<br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <dt>**MCS \_ MULTISELECT**</dt> </dl>                | [Versione 4.70.](common-control-versions.md) Il calendario mensile consente all'utente di selezionare un intervallo di date all'interno del controllo . Per impostazione predefinita, l'intervallo massimo è una settimana. È possibile modificare l'intervallo massimo che può essere selezionato usando il [**messaggio \_ MCM SETMAXSELCOUNT.**](mcm-setmaxselcount.md) <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <dt>**MCS \_ WEEKNUMBERS**</dt> </dl>                | [Versione 4.70.](common-control-versions.md) Il controllo calendario mensile visualizza i numeri delle settimane (da 1 a 52) a sinistra di ogni riga di giorni. La settimana 1 è definita come la prima settimana che contiene almeno quattro giorni. <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <dt>**MCS \_ NOTODAYCIRCLE**</dt> </dl>          | [Versione 4.70.](common-control-versions.md) Il controllo calendario mensile non fa il cerchio sulla data "today". <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <dt>**MCS \_ NOTODAY**</dt> </dl>                            | [Versione 4.70.](common-control-versions.md) Il controllo calendario mensile non visualizza la data "oggi" nella parte inferiore del controllo. <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <dt>**MCS \_ NOTRAILINGDATES**</dt> </dl>    | **Windows Vista.** Le date dei mesi precedenti e successivi non vengono visualizzate nel calendario del mese corrente.<br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <dt>**MCS \_ SHORTDAYSOFWEEK**</dt> </dl>    | **Windows Vista.** I nomi dei giorni brevi vengono visualizzati nell'intestazione.<br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <dt>**MCS \_ NOSELCHANGEONNAV**</dt> </dl> | **Windows Vista.** La selezione non viene modificata quando l'utente si sposta avanti o precedente nel calendario. In questo modo l'utente può selezionare un intervallo più grande di quanto sia visibile.<br/>                                                                                                                                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





