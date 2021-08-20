---
title: Stili del controllo Tab (CommCtrl.h)
description: In questa sezione sono elencati gli stili di controllo struttura a schede supportati.
ms.assetid: a01a6609-b02e-4ada-afa0-ed5ad8dde0d6
topic_type:
- apiref
api_name:
- TCS_BOTTOM
- TCS_BUTTONS
- TCS_FIXEDWIDTH
- TCS_FLATBUTTONS
- TCS_FOCUSNEVER
- TCS_FOCUSONBUTTONDOWN
- TCS_FORCEICONLEFT
- TCS_FORCELABELLEFT
- TCS_HOTTRACK
- TCS_MULTILINE
- TCS_MULTISELECT
- TCS_OWNERDRAWFIXED
- TCS_RAGGEDRIGHT
- TCS_RIGHT
- TCS_RIGHTJUSTIFY
- TCS_SCROLLOPPOSITE
- TCS_SINGLELINE
- TCS_TABS
- TCS_TOOLTIPS
- TCS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4dfdcfb17b2f4a8ffebd4a7cfba5042e19ba2b566d4b03635032438a2f7fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078415"
---
# <a name="tab-control-styles"></a>Stili del controllo Tab

In questa sezione sono elencati gli stili di controllo struttura a schede supportati.



| Costante                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_BOTTOM"></span><span id="tcs_bottom"></span><dl> <dt>**TCS \_ IN BASSO**</dt> </dl>                                  | [Versione 4.70.](common-control-versions.md) Le schede vengono visualizzate nella parte inferiore del controllo. Questo valore è uguale a TCS \_ RIGHT. Questo stile non è supportato se si usa ComCtl32.dll versione 6.<br/>                                                                                                                                                                 |
| <span id="TCS_BUTTONS"></span><span id="tcs_buttons"></span><dl> <dt>**PULSANTI \_ TCS**</dt> </dl>                               | Le schede vengono visualizzate come pulsanti e non viene disegnato alcun bordo intorno all'area di visualizzazione.<br/>                                                                                                                                                                                                                                                                             |
| <span id="TCS_FIXEDWIDTH"></span><span id="tcs_fixedwidth"></span><dl> <dt>**LARGHEZZA \_ FISSA TCS**</dt> </dl>                      | Tutte le schede hanno la stessa larghezza. Questo stile non può essere combinato con lo stile \_ TCS RIGHTJUSTIFY.<br/>                                                                                                                                                                                                                                                        |
| <span id="TCS_FLATBUTTONS"></span><span id="tcs_flatbuttons"></span><dl> <dt>**TCS \_ FLATBUTTONS**</dt> </dl>                   | [Versione 4.71.](common-control-versions.md) Le schede selezionate vengono visualizzate come rientrate sullo sfondo, mentre le altre schede vengono visualizzate sullo stesso piano dello sfondo. Questo stile influisce solo sui controlli struttura a schede con lo stile \_ TCS BUTTONS.<br/>                                                                                                     |
| <span id="TCS_FOCUSNEVER"></span><span id="tcs_focusnever"></span><dl> <dt>**TCS \_ FOCUSNEVER**</dt> </dl>                      | Quando si fa clic su , il controllo Struttura a schede non riceve lo stato attivo per l'input.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="TCS_FOCUSONBUTTONDOWN"></span><span id="tcs_focusonbuttondown"></span><dl> <dt>**TCS \_ FOCUSONBUTTONDOWN**</dt> </dl> | Quando si fa clic, il controllo Struttura a schede riceve lo stato attivo per l'input.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="TCS_FORCEICONLEFT"></span><span id="tcs_forceiconleft"></span><dl> <dt>**TCS \_ FORCEICONLEFT**</dt> </dl>             | Le icone sono allineate al bordo sinistro di ogni scheda a larghezza fissa. Questo stile può essere usato solo con lo stile \_ TCS FIXEDWIDTH.<br/>                                                                                                                                                                                                                           |
| <span id="TCS_FORCELABELLEFT"></span><span id="tcs_forcelabelleft"></span><dl> <dt>**TCS \_ FORCELABELLEFT**</dt> </dl>          | Le etichette sono allineate al bordo sinistro di ogni scheda a larghezza fissa. ciò significa che l'etichetta viene visualizzata immediatamente a destra dell'icona anziché essere centrata. Questo stile può essere usato solo con lo stile TCS FIXEDWIDTH e implica lo stile \_ \_ TCS FORCEICONLEFT.<br/>                                                                             |
| <span id="TCS_HOTTRACK"></span><span id="tcs_hottrack"></span><dl> <dt>**TCS \_ HOTTRACK**</dt> </dl>                            | [Versione 4.70.](common-control-versions.md) Gli elementi sotto il puntatore vengono evidenziati automaticamente. È possibile controllare se il rilevamento a caldo è abilitato chiamando [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/>                                                                                                                              |
| <span id="TCS_MULTILINE"></span><span id="tcs_multiline"></span><dl> <dt>**TCS \_ MULTILINE**</dt> </dl>                         | Se necessario, vengono visualizzate più righe di schede, in modo che tutte le schede siano visibili contemporaneamente.<br/>                                                                                                                                                                                                                                                                 |
| <span id="TCS_MULTISELECT"></span><span id="tcs_multiselect"></span><dl> <dt>**TCS \_ MULTISELECT**</dt> </dl>                   | [Versione 4.70.](common-control-versions.md) È possibile selezionare più schede tenendo premuto CTRL quando si fa clic. Questo stile deve essere utilizzato con lo stile TCS \_ BUTTONS.<br/>                                                                                                                                                                         |
| <span id="TCS_OWNERDRAWFIXED"></span><span id="tcs_ownerdrawfixed"></span><dl> <dt>**OWNERDRAWFIXED DI TCS \_**</dt> </dl>          | La finestra padre è responsabile del disegno delle schede.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="TCS_RAGGEDRIGHT"></span><span id="tcs_raggedright"></span><dl> <dt>**TCS \_ RAGGEDRIGHT**</dt> </dl>                   | Le righe delle schede non verranno adattate per riempire l'intera larghezza del controllo. Questo stile è quello predefinito.<br/>                                                                                                                                                                                                                                              |
| <span id="TCS_RIGHT"></span><span id="tcs_right"></span><dl> <dt>**TCS \_ RIGHT**</dt> </dl>                                     | [Versione 4.70.](common-control-versions.md) Le schede vengono visualizzate verticalmente sul lato destro dei controlli che usano lo stile VERTICAL di \_ TCS. Questo valore è uguale a TCS \_ BOTTOM. Questo stile non è supportato se si usano gli stili di visualizzazione.<br/>                                                                                                                            |
| <span id="TCS_RIGHTJUSTIFY"></span><span id="tcs_rightjustify"></span><dl> <dt>**TCS \_ RIGHTJUSTIFY**</dt> </dl>                | La larghezza di ogni scheda viene aumentata, se necessario, in modo che ogni riga di schede riempia l'intera larghezza del controllo struttura a schede. Questo stile di finestra viene ignorato a meno che non venga specificato anche \_ lo stile MULTILINE TCS.<br/>                                                                                                                                               |
| <span id="TCS_SCROLLOPPOSITE"></span><span id="tcs_scrollopposite"></span><dl> <dt>**TCS \_ SCROLLOPPOSITE**</dt> </dl>          | [Versione 4.70.](common-control-versions.md) Le schede non necessario scorrono verso il lato opposto del controllo quando viene selezionata una scheda.<br/>                                                                                                                                                                                                                       |
| <span id="TCS_SINGLELINE"></span><span id="tcs_singleline"></span><dl> <dt>**TCS \_ SINGLELINE**</dt> </dl>                      | Viene visualizzata una sola riga di schede. L'utente può scorrere per visualizzare altre schede, se necessario. Questo stile è quello predefinito.<br/>                                                                                                                                                                                                                                   |
| <span id="TCS_TABS"></span><span id="tcs_tabs"></span><dl> <dt>**SCHEDE \_ TCS**</dt> </dl>                                        | Le schede vengono visualizzate come schede e viene disegnato un bordo intorno all'area di visualizzazione. Questo stile è quello predefinito.<br/>                                                                                                                                                                                                                                                      |
| <span id="TCS_TOOLTIPS"></span><span id="tcs_tooltips"></span><dl> <dt>**DESCRIZIONI \_ COMANDO TCS**</dt> </dl>                            | Al controllo Struttura a schede è associato un controllo descrizione comando. <br/>                                                                                                                                                                                                                                                                                          |
| <span id="TCS_VERTICAL"></span><span id="tcs_vertical"></span><dl> <dt>**TCS \_ VERTICAL**</dt> </dl>                            | [Versione 4.70.](common-control-versions.md) Le schede vengono visualizzate sul lato sinistro del controllo, con il testo della scheda visualizzato verticalmente. Questo stile è valido solo se usato con lo stile \_ MULTILINE TCS. Per fare in modo che le schede vengano visualizzate sul lato destro del controllo, usare anche lo stile \_ TCS RIGHT. Questo stile non è supportato se si usa ComCtl32.dll versione 6.<br/> |



## <a name="remarks"></a>Commenti

Gli stili seguenti possono essere modificati dopo la creazione del controllo .

-   TCS \_ IN BASSO
-   PULSANTI \_ TCS
-   LARGHEZZA \_ FISSA TCS
-   TCS \_ FLATBUTTONS
-   TCS \_ FORCEICONLEFT
-   TCS \_ FORCELABELLEFT
-   TCS \_ MULTILINE
-   OWNERDRAWFIXED DI TCS \_
-   TCS \_ RAGGEDRIGHT
-   TCS \_ RIGHT
-   TCS \_ VERTICAL

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

