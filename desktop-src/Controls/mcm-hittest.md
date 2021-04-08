---
title: Messaggio MCM_HITTEST (COMmctrl. h)
description: Determina quale parte di un controllo di calendario mensile si trova in un determinato punto sullo schermo. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal HitTest.
ms.assetid: 51e74b07-4ed7-488d-ad5d-116f046577fc
keywords:
- Controlli di Windows Message MCM_HITTEST
topic_type:
- apiref
api_name:
- MCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3670ac8ab663ceda1786f7136a50c4da255a76c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740287"
---
# <a name="mcm_hittest-message"></a>Messaggio di MCM \_ HITTEST

Determina quale parte di un controllo di calendario mensile si trova in un determinato punto sullo schermo. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_hittest) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) . Quando si invia il messaggio, il membro **cbSize** deve essere impostato sulla dimensione della struttura **MCHITTESTINFO** e **PT** deve essere impostato sul punto di cui si desidera eseguire l'hit test.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Imposta i valori nei membri del



| Codice restituito                                                                                           | Descrizione                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Calendario MCHT**</dt> </dl>         | Il punto specificato si trovava nel calendario.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**\_CALENDARBK MCHT**</dt> </dl>       | Il punto specificato si trovava nello sfondo del calendario.<br/>                                                                                                                                                                                                              |
| <dl> <dt>**\_CALENDARDATE MCHT**</dt> </dl>     | Il punto specificato si trovava in una data specifica nel calendario. La struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in *lParam->St* è impostata sulla data in corrispondenza del punto specificato.<br/>                                                                                    |
| <dl> <dt>**\_CALENDARDATENEXT MCHT**</dt> </dl> | Il punto specificato è stato superato una data del mese successivo (visualizzato parzialmente alla fine del mese attualmente visualizzato). Se l'utente fa clic qui, il calendario mensile scorre la visualizzazione al mese o al set di mesi successivo.<br/>                                 |
| <dl> <dt>**\_CALENDARDATEPREV MCHT**</dt> </dl> | Il punto specificato si trovava in una data del mese precedente (visualizzata parzialmente alla fine del mese attualmente visualizzato). Se l'utente fa clic qui, il calendario mensile scorrerà il relativo display al mese o al set di mesi precedente.<br/>                         |
| <dl> <dt>**\_CALENDARDAY MCHT**</dt> </dl>      | Il punto specificato era sopra un'abbreviazione del giorno (ad esempio, "ven"). La struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in *lParam->St* è impostata sulla data corrispondente nella riga superiore.<br/>                                                                      |
| <dl> <dt>**\_CALENDARWEEKNUM MCHT**</dt> </dl>  | Il punto specificato è più di un numero di settimana (solo stile [**MCS \_ su WeekNumbers**](month-calendar-control-styles.md) ). La struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in *lParam->St* è impostata sulla data corrispondente nella colonna più a sinistra.<br/> |
| <dl> <dt>**MCHT \_ successivo**</dt> </dl>             | Il punto specificato si trova in un'area che determinerà lo scorrimento dello schermo del calendario mensile al mese o al set di mesi successivo. Questo flag viene usato per modificare altri flag di hit test.<br/>                                                                                   |
| <dl> <dt>**\_Nessun MCHT**</dt> </dl>          | Il punto specificato non era incluso nel controllo calendario mensile oppure era in una parte inattiva del controllo.<br/>                                                                                                                                                        |
| <dl> <dt>**MCHT \_ Prev**</dt> </dl>             | Il punto specificato si trova in un'area che determinerà lo scorrimento del calendario mensile sullo schermo al mese o al set di mesi precedente. Questo flag viene usato per modificare altri flag di hit test.<br/>                                                                               |
| <dl> <dt>**\_titolo MCHT**</dt> </dl>            | Il punto specificato era oltre il titolo di un mese.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**\_TITLEBK MCHT**</dt> </dl>          | Il punto specificato si trovava sullo sfondo del titolo di un mese.<br/>                                                                                                                                                                                                    |
| <dl> <dt>**\_TITLEBTNNEXT MCHT**</dt> </dl>     | Il punto specificato si trovava sul pulsante nell'angolo superiore destro del controllo. Se l'utente fa clic qui, il calendario mensile scorre la visualizzazione al mese o al set di mesi successivo. <br/>                                                                           |
| <dl> <dt>**\_TITLEBTNPREV MCHT**</dt> </dl>     | Il punto specificato si trovava sul pulsante nell'angolo superiore sinistro del controllo. Se l'utente fa clic qui, il calendario mensile scorrerà il relativo display al mese o al set di mesi precedente. <br/>                                                                        |
| <dl> <dt>**\_TITLEMONTH MCHT**</dt> </dl>       | Il punto specificato si trovava nella barra del titolo di un mese, oltre il nome di un mese.<br/>                                                                                                                                                                                                 |
| <dl> <dt>**\_TITLEYEAR MCHT**</dt> </dl>        | Il punto specificato si trovava nella barra del titolo di un mese, sul valore dell'anno.<br/>                                                                                                                                                                                               |
| <dl> <dt>**\_TODAYLINK MCHT**</dt> </dl>        | Il punto specificato si trovava sul collegamento "Today" nella parte inferiore del controllo calendario mensile.<br/> Il membro **uhit** della struttura [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) in *lParam* corrisponderà al valore restituito. <br/>                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

