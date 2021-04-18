---
title: Stili del controllo calendario mensile (CommCtrl. h)
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
ms.openlocfilehash: 45ccef4a3cc8e16851c0676b8b0dce8c53cfdd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327232"
---
# <a name="month-calendar-control-styles"></a>Stili del controllo calendario mensile

Le costanti di stile seguenti vengono usate durante la creazione di controlli calendario mensile.



| Costante                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <dt>**\_DAYSTATE MCS**</dt> </dl>                         | [Versione 4,70](common-control-versions.md). Il calendario mensile Invia [notifiche \_ GETDAYSTATE di MCN](mcn-getdaystate.md) per richiedere informazioni sui giorni da visualizzare in grassetto.<br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <dt>**MultiSelect MCS \_**</dt> </dl>                | [Versione 4,70](common-control-versions.md). Il calendario mensile consente all'utente di selezionare un intervallo di date all'interno del controllo. Per impostazione predefinita, l'intervallo massimo è di una settimana. È possibile modificare l'intervallo massimo che è possibile selezionare usando il messaggio [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) . <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <dt>**\_su WEEKNUMBERS MCS**</dt> </dl>                | [Versione 4,70](common-control-versions.md). Il controllo calendario mensile Visualizza i numeri di settimana (1-52) a sinistra di ogni riga di giorni. La settimana 1 è definita come prima settimana che contiene almeno quattro giorni. <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <dt>**\_NOTODAYCIRCLE MCS**</dt> </dl>          | [Versione 4,70](common-control-versions.md). Il controllo calendario mensile non esegue il cerchio della data odierna. <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <dt>**MCS \_ NOtoday**</dt> </dl>                            | [Versione 4,70](common-control-versions.md). Il controllo calendario mensile non Visualizza la data "Today" nella parte inferiore del controllo. <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <dt>**\_NOTRAILINGDATES MCS**</dt> </dl>    | **Windows Vista.** Le date dei mesi precedenti e successivi non vengono visualizzate nel calendario del mese corrente.<br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <dt>**\_SHORTDAYSOFWEEK MCS**</dt> </dl>    | **Windows Vista.** I nomi dei giorni brevi vengono visualizzati nell'intestazione.<br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <dt>**\_NOSELCHANGEONNAV MCS**</dt> </dl> | **Windows Vista.** La selezione non viene modificata quando l'utente passa a avanti o indietro nel calendario. Ciò consente all'utente di selezionare un intervallo maggiore di quello visibile.<br/>                                                                                                                                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





