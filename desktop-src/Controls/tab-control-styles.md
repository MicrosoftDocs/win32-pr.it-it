---
title: Stili del controllo scheda (CommCtrl. h)
description: Questa sezione elenca gli stili del controllo scheda supportati.
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
ms.openlocfilehash: 352864fe71b5efc39529109bafb3bdc49cee68e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327229"
---
# <a name="tab-control-styles"></a>Stili del controllo Tab

Questa sezione elenca gli stili del controllo scheda supportati.



| Costante                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_BOTTOM"></span><span id="tcs_bottom"></span><dl> <dt>**TC in \_ basso**</dt> </dl>                                  | [Versione 4,70](common-control-versions.md). Le schede vengono visualizzate nella parte inferiore del controllo. Questo valore è uguale a TCS \_ right. Questo stile non è supportato se si usa ComCtl32.dll versione 6.<br/>                                                                                                                                                                 |
| <span id="TCS_BUTTONS"></span><span id="tcs_buttons"></span><dl> <dt>**\_pulsanti TCS**</dt> </dl>                               | Le schede vengono visualizzate come pulsanti e non viene disegnato alcun bordo intorno all'area di visualizzazione.<br/>                                                                                                                                                                                                                                                                             |
| <span id="TCS_FIXEDWIDTH"></span><span id="tcs_fixedwidth"></span><dl> <dt>**\_FIXEDWIDTH TCS**</dt> </dl>                      | Tutte le schede hanno la stessa larghezza. Questo stile non può essere combinato con lo \_ stile RIGHTJUSTIFY di TCS.<br/>                                                                                                                                                                                                                                                        |
| <span id="TCS_FLATBUTTONS"></span><span id="tcs_flatbuttons"></span><dl> <dt>**\_FLATBUTTONS TCS**</dt> </dl>                   | [Versione 4,71](common-control-versions.md). Le schede selezionate vengono visualizzate come rientri sullo sfondo mentre le altre schede appaiono sullo stesso piano dello sfondo. Questo stile interessa solo i controlli struttura a schede con lo \_ stile dei pulsanti TCS.<br/>                                                                                                     |
| <span id="TCS_FOCUSNEVER"></span><span id="tcs_focusnever"></span><dl> <dt>**\_FOCUSNEVER TCS**</dt> </dl>                      | Quando si fa clic, il controllo struttura a schede non riceve lo stato attivo per l'input.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="TCS_FOCUSONBUTTONDOWN"></span><span id="tcs_focusonbuttondown"></span><dl> <dt>**\_FOCUSONBUTTONDOWN TCS**</dt> </dl> | Quando si fa clic, il controllo struttura a schede riceve lo stato attivo per l'input.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="TCS_FORCEICONLEFT"></span><span id="tcs_forceiconleft"></span><dl> <dt>**\_FORCEICONLEFT TCS**</dt> </dl>             | Le icone sono allineate al bordo sinistro di ogni scheda a larghezza fissa. Questo stile può essere usato solo con lo \_ stile FIXEDWIDTH di TCS.<br/>                                                                                                                                                                                                                           |
| <span id="TCS_FORCELABELLEFT"></span><span id="tcs_forcelabelleft"></span><dl> <dt>**\_FORCELABELLEFT TCS**</dt> </dl>          | Le etichette sono allineate al bordo sinistro di ogni scheda a larghezza fissa; ovvero l'etichetta viene visualizzata immediatamente a destra dell'icona anziché centrata. Questo stile può essere usato solo con lo \_ stile FIXEDWIDTH di TCS e implica lo \_ stile FORCEICONLEFT di TCS.<br/>                                                                             |
| <span id="TCS_HOTTRACK"></span><span id="tcs_hottrack"></span><dl> <dt>**\_HOTTRACK TCS**</dt> </dl>                            | [Versione 4,70](common-control-versions.md). Gli elementi sotto il puntatore vengono evidenziati automaticamente. È possibile verificare se il rilevamento a caldo è abilitato chiamando [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/>                                                                                                                              |
| <span id="TCS_MULTILINE"></span><span id="tcs_multiline"></span><dl> <dt>**multiriga TCS \_**</dt> </dl>                         | Se necessario, vengono visualizzate più righe di schede, in modo che tutte le schede siano visibili in una sola volta.<br/>                                                                                                                                                                                                                                                                 |
| <span id="TCS_MULTISELECT"></span><span id="tcs_multiselect"></span><dl> <dt>**MultiSelect TCS \_**</dt> </dl>                   | [Versione 4,70](common-control-versions.md). È possibile selezionare più schede tenendo premuto il tasto CTRL quando si fa clic su. Questo stile deve essere usato con lo \_ stile dei pulsanti TCS.<br/>                                                                                                                                                                         |
| <span id="TCS_OWNERDRAWFIXED"></span><span id="tcs_ownerdrawfixed"></span><dl> <dt>**\_OwnerDrawFixed TCS**</dt> </dl>          | La finestra padre è responsabile della creazione di schede.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="TCS_RAGGEDRIGHT"></span><span id="tcs_raggedright"></span><dl> <dt>**\_RAGGEDRIGHT TCS**</dt> </dl>                   | Le righe di tabulazioni non verranno estese per riempire l'intera larghezza del controllo. Questo stile è il valore predefinito.<br/>                                                                                                                                                                                                                                              |
| <span id="TCS_RIGHT"></span><span id="tcs_right"></span><dl> <dt>**TCS a \_ destra**</dt> </dl>                                     | [Versione 4,70](common-control-versions.md). Le schede vengono visualizzate verticalmente sul lato destro dei controlli che usano lo \_ stile verticale TCS. Questo valore è uguale a TCS in \_ basso. Questo stile non è supportato se si utilizzano gli stili di visualizzazione.<br/>                                                                                                                            |
| <span id="TCS_RIGHTJUSTIFY"></span><span id="tcs_rightjustify"></span><dl> <dt>**\_RIGHTJUSTIFY TCS**</dt> </dl>                | La larghezza di ogni scheda è aumentata, se necessario, in modo che ogni riga di schede riempia l'intera larghezza del controllo struttura a schede. Questo stile della finestra viene ignorato a meno che non \_ sia specificato anche lo stile multiriga di TCS.<br/>                                                                                                                                               |
| <span id="TCS_SCROLLOPPOSITE"></span><span id="tcs_scrollopposite"></span><dl> <dt>**\_SCROLLOPPOSITE TCS**</dt> </dl>          | [Versione 4,70](common-control-versions.md). Le schede non necessarie scorrono verso il lato opposto del controllo quando viene selezionata una scheda.<br/>                                                                                                                                                                                                                       |
| <span id="TCS_SINGLELINE"></span><span id="tcs_singleline"></span><dl> <dt>**\_Singleline TCS**</dt> </dl>                      | Viene visualizzata solo una riga di schede. Se necessario, l'utente può scorrere per visualizzare altre schede. Questo stile è il valore predefinito.<br/>                                                                                                                                                                                                                                   |
| <span id="TCS_TABS"></span><span id="tcs_tabs"></span><dl> <dt>**\_schede TCS**</dt> </dl>                                        | Le schede vengono visualizzate come tabulazioni e viene disegnato un bordo intorno all'area di visualizzazione. Questo stile è il valore predefinito.<br/>                                                                                                                                                                                                                                                      |
| <span id="TCS_TOOLTIPS"></span><span id="tcs_tooltips"></span><dl> <dt>**\_descrizioni comando TCS**</dt> </dl>                            | Al controllo struttura a schede è associato un controllo ToolTip. <br/>                                                                                                                                                                                                                                                                                          |
| <span id="TCS_VERTICAL"></span><span id="tcs_vertical"></span><dl> <dt>**TC \_ verticale**</dt> </dl>                            | [Versione 4,70](common-control-versions.md). Le schede vengono visualizzate sul lato sinistro del controllo, con il testo della scheda visualizzato verticalmente. Questo stile è valido solo se usato con lo \_ stile multiriga di TCS. Per fare in modo che le schede vengano visualizzate sul lato destro del controllo, usare anche lo stile di TCS a \_ destra. Questo stile non è supportato se si usa ComCtl32.dll versione 6.<br/> |



## <a name="remarks"></a>Commenti

Gli stili seguenti possono essere modificati dopo la creazione del controllo.

-   TC in \_ basso
-   \_pulsanti TCS
-   \_FIXEDWIDTH TCS
-   \_FLATBUTTONS TCS
-   \_FORCEICONLEFT TCS
-   \_FORCELABELLEFT TCS
-   multiriga TCS \_
-   \_OwnerDrawFixed TCS
-   \_RAGGEDRIGHT TCS
-   TCS a \_ destra
-   TC \_ verticale

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

