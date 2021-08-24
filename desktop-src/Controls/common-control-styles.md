---
title: Stili dei controlli comuni (CommCtrl.h)
description: In questa sezione vengono elencati gli stili dei controlli comuni. Fatta eccezione per i casi in cui è stato fatto, questi stili si applicano ai controlli Rebar, ai controlli barra degli strumenti e alle finestre di stato.
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
ms.openlocfilehash: bd9ec00cd7cedc4bb105543f932cd5fdcfc76d7c038fb930abb7f0b5d1aeb13d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698821"
---
# <a name="common-control-styles"></a>Stili di controllo comuni

In questa sezione vengono elencati gli stili dei controlli comuni. Fatta eccezione per i casi in cui è stato fatto, questi stili si applicano ai controlli Rebar, ai controlli barra degli strumenti e alle finestre di stato.



| Costante                                                                                                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CCS_ADJUSTABLE"></span><span id="ccs_adjustable"></span><dl> <dt>**CCS \_ REGOLABILE**</dt> </dl>          | Abilita le funzionalità di personalizzazione incorporate di una barra degli strumenti, che consentono all'utente di trascinare un pulsante in una nuova posizione o di rimuovere un pulsante trascinandolo fuori dalla barra degli strumenti. Inoltre, l'utente può fare doppio clic  sulla barra degli strumenti per visualizzare la finestra di dialogo Personalizza barra degli strumenti, che consente all'utente di aggiungere, eliminare e ridisporre i pulsanti della barra degli strumenti.<br/> |
| <span id="CCS_BOTTOM"></span><span id="ccs_bottom"></span><dl> <dt>**CCS \_ IN BASSO**</dt> </dl>                      | Fa in modo che il controllo si posizioni nella parte inferiore dell'area client della finestra padre e imposta la larghezza sulla stessa larghezza della finestra padre. Le finestre di stato hanno questo stile per impostazione predefinita.<br/>                                                                                                                                          |
| <span id="CCS_LEFT"></span><span id="ccs_left"></span><dl> <dt>**CCS \_ LEFT**</dt> </dl>                            | [Versione 4.70.](common-controls-intro.md) Determina la visualizzazione verticale del controllo sul lato sinistro della finestra padre.<br/>                                                                                                                                                                                                            |
| <span id="CCS_NODIVIDER"></span><span id="ccs_nodivider"></span><dl> <dt>**CCS \_ NODIVIDER**</dt> </dl>             | Impedisce di disegnare un'evidenziazione di due pixel nella parte superiore del controllo. <br/>                                                                                                                                                                                                                                                                |
| <span id="CCS_NOMOVEX"></span><span id="ccs_nomovex"></span><dl> <dt>**CCS \_ NOMOVEX**</dt> </dl>                   | [Versione 4.70.](common-controls-intro.md) Fa in modo che il controllo si ridimensioni e si sposti verticalmente, ma non orizzontalmente, in risposta a un [**messaggio WM \_ SIZE.**](/windows/desktop/winmsg/wm-size) Se si usa \_ CCS NORESIZE, questo stile non è applicabile.<br/>                                                                                                    |
| <span id="CCS_NOMOVEY"></span><span id="ccs_nomovey"></span><dl> <dt>**CCS \_ NOMOVEY**</dt> </dl>                   | Fa sì che il controllo si ridimensioni e si sposti orizzontalmente, ma non verticalmente, in risposta a un [**messaggio WM \_ SIZE.**](/windows/desktop/winmsg/wm-size) Se si usa \_ CCS NORESIZE, questo stile non è applicabile. Per impostazione predefinita, le finestre di intestazione hanno questo stile.<br/>                                                                                                    |
| <span id="CCS_NOPARENTALIGN"></span><span id="ccs_noparentalign"></span><dl> <dt>**CCS \_ NOPARENTALIGN**</dt> </dl> | Impedisce al controllo di spostarsi automaticamente nella parte superiore o inferiore della finestra padre. Al contrario, il controllo mantiene la propria posizione all'interno della finestra padre nonostante le modifiche alle dimensioni dell'elemento padre. Se si usa anche CCS TOP o CCS BOTTOM, l'altezza viene regolata sul valore predefinito, ma la posizione e la \_ \_ larghezza rimangono invariate. <br/>        |
| <span id="CCS_NORESIZE"></span><span id="ccs_noresize"></span><dl> <dt>**CCS \_ NORESIZE**</dt> </dl>                | Impedisce al controllo di usare la larghezza e l'altezza predefinite durante l'impostazione delle dimensioni iniziali o di una nuova dimensione. Il controllo usa invece la larghezza e l'altezza specificate nella richiesta per la creazione o il ridimensionamento. <br/>                                                                                                                                 |
| <span id="CCS_RIGHT"></span><span id="ccs_right"></span><dl> <dt>**CCS \_ RIGHT**</dt> </dl>                         | [Versione 4.70.](common-controls-intro.md) Determina la visualizzazione verticale del controllo sul lato destro della finestra padre.<br/>                                                                                                                                                                                                           |
| <span id="CCS_TOP"></span><span id="ccs_top"></span><dl> <dt>**CCS \_ TOP**</dt> </dl>                               | Fa in modo che il controllo si posizioni nella parte superiore dell'area client della finestra padre e imposta la larghezza sulla stessa larghezza della finestra padre. Le barre degli strumenti hanno questo stile per impostazione predefinita. <br/>                                                                                                                                                  |
| <span id="CCS_VERT"></span><span id="ccs_vert"></span><dl> <dt>**CCS \_ VERT**</dt> </dl>                            | [Versione 4.70.](common-controls-intro.md) Determina la visualizzazione verticale del controllo.<br/>                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Commenti

Negli argomenti seguenti vengono descritti altri stili dei controlli:

-   [**Stili del controllo Animation**](animation-control-styles.md)
-   [**Stili dei pulsanti**](button-styles.md)
-   [**Stili delle caselle combinate**](combo-box-styles.md)
-   [**Stili estesi del controllo ComboBoxEx**](comboboxex-control-extended-styles.md)
-   [**Stili del controllo Selezione data e ora**](date-and-time-picker-control-styles.md)
-   [**Modificare gli stili dei controlli**](edit-control-styles.md)
-   [**Stili del controllo Header**](header-control-styles.md)
-   [**Stili della casella di riepilogo**](list-box-styles.md)
-   [**Stili della finestra Visualizzazione elenco**](list-view-window-styles.md)
-   [**Stili del controllo Calendario mensile**](month-calendar-control-styles.md)
-   [**Stili del controllo Pager**](pager-control-styles.md)
-   [**Stili del controllo Indicatore di stato**](progress-bar-control-styles.md)
-   [**Stili del controllo Rebar**](rebar-control-styles.md)
-   [**Stili del controllo Rich Edit**](rich-edit-control-styles.md)
-   [**Stili del controllo Barra di scorrimento**](scroll-bar-control-styles.md)
-   [Stili dei controlli statici](static-control-styles.md)
-   [**Stili della barra di stato**](status-bar-styles.md)
-   [**Stili del controllo SysLink**](syslink-control-styles.md)
-   [**Stili del controllo Tab**](tab-control-styles.md)
-   [**Stili dei pulsanti e dei controlli Barra degli strumenti**](toolbar-control-and-button-styles.md)
-   [**Stili della descrizione comando**](tooltip-styles.md)
-   [**Stili del controllo Trackbar**](trackbar-control-styles.md)
-   [**Stili della finestra del controllo Visualizzazione struttura ad albero**](tree-view-control-window-styles.md)
-   [**Stili dei controlli up-down**](up-down-control-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

