---
title: Stili del controllo TrackBar (CommCtrl. h)
description: Questa sezione contiene informazioni sugli stili usati con i controlli TrackBar.
ms.assetid: ac2f59c6-85a2-4f41-aace-4132971d3559
topic_type:
- apiref
api_name:
- TBS_AUTOTICKS
- TBS_VERT
- TBS_HORZ
- TBS_TOP
- TBS_BOTTOM
- TBS_LEFT
- TBS_RIGHT
- TBS_BOTH
- TBS_NOTICKS
- TBS_ENABLESELRANGE
- TBS_FIXEDLENGTH
- TBS_NOTHUMB
- TBS_TOOLTIPS
- TBS_REVERSED
- TBS_DOWNISLEFT
- TBS_NOTIFYBEFOREMOVE
- TBS_TRANSPARENTBKGND
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42966f98db18257c9a6a9ca463d5bd88028a02f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326841"
---
# <a name="trackbar-control-styles"></a>Stili del controllo TrackBar

Questa sezione contiene informazioni sugli stili usati con i controlli TrackBar.



| Costante                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_AUTOTICKS"></span><span id="tbs_autoticks"></span><dl> <dt>**\_cicli autocicli TBS**</dt> </dl>                      | Il controllo TrackBar dispone di un segno di graduazione per ogni incremento nell'intervallo di valori. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_VERT"></span><span id="tbs_vert"></span><dl> <dt>**TBS \_ Vert**</dt> </dl>                                     | Il controllo TrackBar è orientato verticalmente.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="TBS_HORZ"></span><span id="tbs_horz"></span><dl> <dt>**orizzontalmente di TBS \_**</dt> </dl>                                     | Il controllo TrackBar è orientato orizzontalmente. Si tratta dell'orientamento predefinito. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOP"></span><span id="tbs_top"></span><dl> <dt>**\_primi TBS**</dt> </dl>                                        | Il controllo TrackBar Visualizza i segni di graduazione sopra il controllo. Questo stile è valido solo con TBS \_ orizzontalmente. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_BOTTOM"></span><span id="tbs_bottom"></span><dl> <dt>**TBS in \_ basso**</dt> </dl>                               | Il controllo TrackBar Visualizza i segni di graduazione sotto il controllo. Questo stile è valido solo con TBS \_ orizzontalmente. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_LEFT"></span><span id="tbs_left"></span><dl> <dt>**TBS a \_ sinistra**</dt> </dl>                                     | Il controllo TrackBar Visualizza i segni di graduazione a sinistra del controllo. Questo stile è valido solo con TBS \_ Vert. <br/>                                                                                                                                                                                                                                             |
| <span id="TBS_RIGHT"></span><span id="tbs_right"></span><dl> <dt>**TBS a \_ destra**</dt> </dl>                                  | Il controllo TrackBar Visualizza i segni di graduazione a destra del controllo. Questo stile è valido solo con TBS \_ Vert. <br/>                                                                                                                                                                                                                                            |
| <span id="TBS_BOTH"></span><span id="tbs_both"></span><dl> <dt>**TBS \_**</dt> </dl>                                     | Il controllo TrackBar Visualizza i segni di graduazione su entrambi i lati del controllo. Si tratta della parte superiore e inferiore quando viene usato con TBS \_ orizzontalmente o sia a sinistra che a destra se usato con TBS \_ Vert. <br/>                                                                                                                                                                           |
| <span id="TBS_NOTICKS"></span><span id="tbs_noticks"></span><dl> <dt>**TBS \_ nosegni**</dt> </dl>                            | Nel controllo TrackBar non vengono visualizzati segni di graduazione. <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TBS_ENABLESELRANGE"></span><span id="tbs_enableselrange"></span><dl> <dt>**ENABLESELRANGE di TBS \_**</dt> </dl>       | Il controllo TrackBar Visualizza solo un intervallo di selezione. I segni di graduazione nelle posizioni iniziale e finale di un intervallo di selezione vengono visualizzati come triangoli (anziché trattini verticali) e l'intervallo di selezione viene evidenziato. <br/>                                                                                                                           |
| <span id="TBS_FIXEDLENGTH"></span><span id="tbs_fixedlength"></span><dl> <dt>**FIXEDLENGTH di TBS \_**</dt> </dl>                | Il controllo TrackBar consente la modifica della dimensione del dispositivo di scorrimento con il [**messaggio \_ SETTHUMBLENGTH TBM**](tbm-setthumblength.md) . <br/>                                                                                                                                                                                                                      |
| <span id="TBS_NOTHUMB"></span><span id="tbs_nothumb"></span><dl> <dt>**TBS \_ NOthumb**</dt> </dl>                            | Il controllo TrackBar non visualizza un dispositivo di scorrimento. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOOLTIPS"></span><span id="tbs_tooltips"></span><dl> <dt>**\_descrizioni comandi di TBS**</dt> </dl>                         | [Versione 4,70](common-control-versions.md). Il controllo TrackBar supporta le descrizioni comandi. Quando si crea un controllo TrackBar usando questo stile, viene creato automaticamente un controllo ToolTip predefinito che visualizza la posizione corrente del dispositivo di scorrimento. È possibile modificare il punto in cui vengono visualizzate le descrizioni comandi usando il messaggio [**TBM \_ SETTIPSIDE**](tbm-settipside.md) . <br/> |
| <span id="TBS_REVERSED"></span><span id="tbs_reversed"></span><dl> <dt>**TBS \_ invertito**</dt> </dl>                         | [Versione 5,80.](common-control-versions.md) Questo bit di stile viene usato per gli TrackBar "invertiti", dove un numero inferiore indica "maggiore" e un numero maggiore indica "inferiore". Non ha alcun effetto sul controllo; si tratta semplicemente di un'etichetta che può essere verificata per determinare se un TrackBar è normale o invertito.<br/>                                             |
| <span id="TBS_DOWNISLEFT"></span><span id="tbs_downisleft"></span><dl> <dt>**DOWNISLEFT di TBS \_**</dt> </dl>                   | Per impostazione predefinita, il controllo TrackBar usa il valore di Down uguale a Right e il valore di Left. Usare lo \_ stile TBS DOWNISLEFT per invertire il valore predefinito, rendendo l'uguale a sinistra e verso l'alto a destra. <br/>                                                                                                                                                                          |
| <span id="TBS_NOTIFYBEFOREMOVE"></span><span id="tbs_notifybeforemove"></span><dl> <dt>**NOTIFYBEFOREMOVE di TBS \_**</dt> </dl> | [Versione 6,00](common-control-versions.md) e **Windows Vista.** TrackBar deve notificare all'elemento padre prima di riposizionare il dispositivo di scorrimento a causa dell'azione dell'utente (Abilita l'allineamento). <br/>                                                                                                                                                                                   |
| <span id="TBS_TRANSPARENTBKGND"></span><span id="tbs_transparentbkgnd"></span><dl> <dt>**TRANSPARENTBKGND di TBS \_**</dt> </dl> | [Versione 6,00](common-control-versions.md) e **Windows Vista.** Lo sfondo viene disegnato dall'elemento padre tramite il \_ messaggio WM PRINTCLIENT. <br/>                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





