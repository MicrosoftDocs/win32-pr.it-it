---
title: Stili di controllo comuni (CommCtrl. h)
description: Questa sezione elenca gli stili di controllo comuni. Ad eccezione dei casi indicati, questi stili si applicano ai controlli Rebar, ai controlli della barra degli strumenti e alle finestre di stato.
ms.assetid: aab0cd68-ede7-474b-8695-c75805669716
topic_type:
- apiref
api_name:
- CCS_ADJUSTABLE
- CCS_BOTTOM
- CCS_LEFT
- CCS_NODIVIDER
- CCS_NOMOVEX
- CCS_NOMOVEY
- CCS_NOPARENTALIGN
- CCS_NORESIZE
- CCS_RIGHT
- CCS_TOP
- CCS_VERT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a50b28a95d94a97da2fb6ac3522dbc568af111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327680"
---
# <a name="common-control-styles"></a>Stili di controllo comuni

Questa sezione elenca gli stili di controllo comuni. Ad eccezione dei casi indicati, questi stili si applicano ai controlli Rebar, ai controlli della barra degli strumenti e alle finestre di stato.



| Costante                                                                                                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CCS_ADJUSTABLE"></span><span id="ccs_adjustable"></span><dl> <dt>**con \_ regolazione CCS**</dt> </dl>          | Abilita le funzionalità di personalizzazione predefinite di una barra degli strumenti che consentono all'utente di trascinare un pulsante in una nuova posizione o di rimuovere un pulsante trascinandolo dalla barra degli strumenti. Inoltre, l'utente può fare doppio clic sulla barra degli strumenti per visualizzare la finestra di dialogo **Personalizza barra degli** strumenti, che consente all'utente di aggiungere, eliminare e riordinare i pulsanti della barra degli strumenti.<br/> |
| <span id="CCS_BOTTOM"></span><span id="ccs_bottom"></span><dl> <dt>**CCS in \_ basso**</dt> </dl>                      | Determina la posizione del controllo nella parte inferiore dell'area client della finestra padre e imposta la larghezza in modo che corrisponda alla larghezza della finestra padre. Per impostazione predefinita, le finestre di stato hanno questo stile.<br/>                                                                                                                                          |
| <span id="CCS_LEFT"></span><span id="ccs_left"></span><dl> <dt>**CCS a \_ sinistra**</dt> </dl>                            | [Versione 4,70](common-controls-intro.md). Fa in modo che il controllo venga visualizzato verticalmente sul lato sinistro della finestra padre.<br/>                                                                                                                                                                                                            |
| <span id="CCS_NODIVIDER"></span><span id="ccs_nodivider"></span><dl> <dt>**\_NOdivider CCS**</dt> </dl>             | Impedisce che l'evidenziazione di due pixel venga disegnata nella parte superiore del controllo. <br/>                                                                                                                                                                                                                                                                |
| <span id="CCS_NOMOVEX"></span><span id="ccs_nomovex"></span><dl> <dt>**\_NOMOVEX CCS**</dt> </dl>                   | [Versione 4,70](common-controls-intro.md). Determina il ridimensionamento e lo spostamento verticale del controllo, ma non orizzontalmente, in risposta a un messaggio di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) . Se \_ si utilizza CCS noresize, questo stile non viene applicato.<br/>                                                                                                    |
| <span id="CCS_NOMOVEY"></span><span id="ccs_nomovey"></span><dl> <dt>**CCS \_ NOmovey**</dt> </dl>                   | Fa in modo che il controllo venga ridimensionato e spostato orizzontalmente, ma non verticalmente, in risposta a un messaggio di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) . Se \_ si utilizza CCS noresize, questo stile non viene applicato. Per impostazione predefinita, le finestre di intestazione hanno questo stile.<br/>                                                                                                    |
| <span id="CCS_NOPARENTALIGN"></span><span id="ccs_noparentalign"></span><dl> <dt>**\_NOPARENTALIGN CCS**</dt> </dl> | Impedisce che il controllo si sposti automaticamente nella parte superiore o inferiore della finestra padre. Al contrario, il controllo mantiene la posizione all'interno della finestra padre, nonostante le modifiche apportate alle dimensioni dell'elemento padre. Se \_ viene utilizzata anche la fine CCS Top o CCS \_ , l'altezza viene modificata in base all'impostazione predefinita, ma la posizione e la larghezza rimangono invariate. <br/>        |
| <span id="CCS_NORESIZE"></span><span id="ccs_noresize"></span><dl> <dt>**CCS \_ NOresize**</dt> </dl>                | Impedisce al controllo di utilizzare la larghezza e l'altezza predefinite quando si imposta la dimensione iniziale o una nuova dimensione. Al contrario, il controllo Usa la larghezza e l'altezza specificate nella richiesta per la creazione o il ridimensionamento. <br/>                                                                                                                                 |
| <span id="CCS_RIGHT"></span><span id="ccs_right"></span><dl> <dt>**CCS a \_ destra**</dt> </dl>                         | [Versione 4,70](common-controls-intro.md). Fa in modo che il controllo venga visualizzato verticalmente sul lato destro della finestra padre.<br/>                                                                                                                                                                                                           |
| <span id="CCS_TOP"></span><span id="ccs_top"></span><dl> <dt>**\_primi CCS**</dt> </dl>                               | Determina la posizione del controllo nella parte superiore dell'area client della finestra padre e imposta la larghezza in modo che corrisponda alla larghezza della finestra padre. Per impostazione predefinita, le barre degli strumenti hanno questo stile. <br/>                                                                                                                                                  |
| <span id="CCS_VERT"></span><span id="ccs_vert"></span><dl> <dt>**\_vertici CCS**</dt> </dl>                            | [Versione 4,70](common-controls-intro.md). Determina la visualizzazione verticale del controllo.<br/>                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Commenti

Negli argomenti seguenti vengono descritti gli stili di controllo aggiuntivi:

-   [**Stili del controllo di animazione**](animation-control-styles.md)
-   [**Stili pulsante**](button-styles.md)
-   [**Stili casella combinata**](combo-box-styles.md)
-   [**Stili estesi del controllo ComboBoxEx**](comboboxex-control-extended-styles.md)
-   [**Stili del controllo selezione data e ora**](date-and-time-picker-control-styles.md)
-   [**Modificare gli stili del controllo**](edit-control-styles.md)
-   [**Stili del controllo intestazione**](header-control-styles.md)
-   [**Stili casella di riepilogo**](list-box-styles.md)
-   [**Stili della finestra visualizzazione elenco**](list-view-window-styles.md)
-   [**Stili del controllo calendario mensile**](month-calendar-control-styles.md)
-   [**Stili del controllo pager**](pager-control-styles.md)
-   [**Stili del controllo indicatore di stato**](progress-bar-control-styles.md)
-   [**Stili del controllo Rebar**](rebar-control-styles.md)
-   [**Stili del controllo Rich Edit**](rich-edit-control-styles.md)
-   [**Stili del controllo barra di scorrimento**](scroll-bar-control-styles.md)
-   [Stili del controllo statico](static-control-styles.md)
-   [**Stili della barra di stato**](status-bar-styles.md)
-   [**Stili del controllo SysLink**](syslink-control-styles.md)
-   [**Stili del controllo Tab**](tab-control-styles.md)
-   [**Stili del pulsante e del controllo Toolbar**](toolbar-control-and-button-styles.md)
-   [**Stili descrizione comando**](tooltip-styles.md)
-   [**Stili del controllo TrackBar**](trackbar-control-styles.md)
-   [**Stili della finestra controllo visualizzazione albero**](tree-view-control-window-styles.md)
-   [**Stili di controllo di scorrimento**](up-down-control-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

