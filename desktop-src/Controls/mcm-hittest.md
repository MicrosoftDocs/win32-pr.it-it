---
title: MCM_HITTEST messaggio (Commctrl.h)
description: Determina quale parte di un controllo calendario mensile si trova in un determinato punto sullo schermo. È possibile inviare questo messaggio in modo esplicito o tramite la macro MonthCal \_ HitTest.
ms.assetid: 51e74b07-4ed7-488d-ad5d-116f046577fc
keywords:
- MCM_HITTEST dei messaggi Windows controlli
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
ms.openlocfilehash: 3ab43ae76a2e747ff019a5bafa32870a208851a143ad94dd0679e894366c3592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697191"
---
# <a name="mcm_hittest-message"></a>Messaggio \_ MCM HITTEST

Determina quale parte di un controllo calendario mensile si trova in un determinato punto sullo schermo. È possibile inviare questo messaggio in modo esplicito o usando la macro [**MonthCal \_ HitTest.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_hittest)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura MCHITTESTINFO.**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) Al momento dell'invio del messaggio, il membro **cbSize** deve essere impostato sulle dimensioni della struttura **MCHITTESTINFO** e **pt** deve essere impostato sul punto da hit test.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Imposta i valori nei membri dell'oggetto



| Codice restituito                                                                                           | Descrizione                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CALENDARIO \_ MCHT**</dt> </dl>         | Il punto specificato si trova all'interno del calendario.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**CALENDARIO \_ MCHTBK**</dt> </dl>       | Il punto specificato era sullo sfondo del calendario.<br/>                                                                                                                                                                                                              |
| <dl> <dt>**MCHT \_ CALENDARDATE**</dt> </dl>     | Il punto specificato si trova in una data specifica all'interno del calendario. La [**struttura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in *lParam->st* è impostata sulla data nel punto specificato.<br/>                                                                                    |
| <dl> <dt>**CALENDARIO \_ MCHTDATENEXT**</dt> </dl> | Il punto specificato era oltre una data del mese successivo (parzialmente visualizzato alla fine del mese attualmente visualizzato). Se l'utente fa clic qui, il calendario mensile scorrerà la visualizzazione fino al mese o al set di mesi successivo.<br/>                                 |
| <dl> <dt>**CALENDARIO \_ MCHTDATEPREV**</dt> </dl> | Il punto specificato è superiore a una data del mese precedente (parzialmente visualizzato alla fine del mese attualmente visualizzato). Se l'utente fa clic qui, il calendario mensile scorrerà la visualizzazione fino al mese o al set di mesi precedente.<br/>                         |
| <dl> <dt>**MCHT \_ CALENDARDAY**</dt> </dl>      | Il punto specificato era un'abbreviazione di giorno ("ven", ad esempio). La [**struttura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in *lParam->st* è impostata sulla data corrispondente nella riga superiore.<br/>                                                                      |
| <dl> <dt>**CALENDARIO \_ MCHTWEEKNUM**</dt> </dl>  | Il punto specificato è più di un numero di settimana (solo in stile [**\_ MCS WEEKNUMBERS).**](month-calendar-control-styles.md) La [**struttura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in *lParam->st* è impostata sulla data corrispondente nella colonna più a sinistra.<br/> |
| <dl> <dt>**MCHT \_ NEXT**</dt> </dl>             | Il punto specificato si trova in un'area che fa scorrere la visualizzazione del calendario mensile al mese o al set di mesi successivo. Questo flag viene usato per modificare altri flag di hit test.<br/>                                                                                   |
| <dl> <dt>**MCHT \_ DA NESSUNA PARTE**</dt> </dl>          | Il punto specificato non era nel controllo calendario mensile o era in una parte inattiva del controllo.<br/>                                                                                                                                                        |
| <dl> <dt>**MCHT \_ PREV**</dt> </dl>             | Il punto specificato si trova in un'area che farà scorrere la visualizzazione del calendario mensile fino al mese o al set di mesi precedente. Questo flag viene usato per modificare altri flag di hit test.<br/>                                                                               |
| <dl> <dt>**TITOLO \_ MCHT**</dt> </dl>            | Il punto specificato è il titolo di oltre un mese.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**MCHT \_ TITLEBK**</dt> </dl>          | Il punto specificato era sullo sfondo del titolo di un mese.<br/>                                                                                                                                                                                                    |
| <dl> <dt>**MCHT \_ TITLEBTNNEXT**</dt> </dl>     | Il punto specificato era sopra il pulsante nell'angolo superiore destro del controllo . Se l'utente fa clic qui, il calendario mensile scorrerà la visualizzazione fino al mese o al set di mesi successivo. <br/>                                                                           |
| <dl> <dt>**TITOLO \_ MCHTBTNPREV**</dt> </dl>     | Il punto specificato era sopra il pulsante nell'angolo superiore sinistro del controllo. Se l'utente fa clic qui, il calendario mensile scorrerà la visualizzazione fino al mese o al set di mesi precedente. <br/>                                                                        |
| <dl> <dt>**MCHT \_ TITLEMONTH**</dt> </dl>       | Il punto specificato era nella barra del titolo di un mese, oltre un nome di mese.<br/>                                                                                                                                                                                                 |
| <dl> <dt>**MCHT \_ TITLEYEAR**</dt> </dl>        | Il punto specificato era nella barra del titolo di un mese, rispetto al valore dell'anno.<br/>                                                                                                                                                                                               |
| <dl> <dt>**MCHT \_ TODAYLINK**</dt> </dl>        | Il punto specificato era sul collegamento "oggi" nella parte inferiore del controllo calendario mensile.<br/> Il **membro uHit** della struttura [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) in *lParam* sarà uguale al valore restituito. <br/>                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

