---
title: Stili del controllo Trackbar (CommCtrl.h)
description: Questa sezione contiene informazioni sugli stili usati con i controlli trackbar.
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
ms.openlocfilehash: 9165325c2d78ac6e4dc1ae69e410d293100de24cb8d38868475e99e49c0faaa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046021"
---
# <a name="trackbar-control-styles"></a>Stili del controllo Trackbar

Questa sezione contiene informazioni sugli stili usati con i controlli trackbar.



| Costante                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_AUTOTICKS"></span><span id="tbs_autoticks"></span><dl> <dt>**TBS \_ AUTOTICKS**</dt> </dl>                      | Il controllo trackbar ha un segno di graduazione per ogni incremento nell'intervallo di valori. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_VERT"></span><span id="tbs_vert"></span><dl> <dt>**TBS \_ VERT**</dt> </dl>                                     | Il controllo trackbar è orientato verticalmente.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="TBS_HORZ"></span><span id="tbs_horz"></span><dl> <dt>**TBS \_ HORZ**</dt> </dl>                                     | Il controllo trackbar è orientato orizzontalmente. Questo è l'orientamento predefinito. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOP"></span><span id="tbs_top"></span><dl> <dt>**TBS \_ TOP**</dt> </dl>                                        | Il controllo trackbar visualizza segni di graduazione sopra il controllo. Questo stile è valido solo con TBS \_ HORZ. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_BOTTOM"></span><span id="tbs_bottom"></span><dl> <dt>**TBS \_ BOTTOM**</dt> </dl>                               | Il controllo trackbar visualizza segni di graduazione sotto il controllo. Questo stile è valido solo con TBS \_ HORZ. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_LEFT"></span><span id="tbs_left"></span><dl> <dt>**TBS \_ LEFT**</dt> </dl>                                     | Il controllo trackbar visualizza segni di graduazione a sinistra del controllo. Questo stile è valido solo con TBS \_ VERT. <br/>                                                                                                                                                                                                                                             |
| <span id="TBS_RIGHT"></span><span id="tbs_right"></span><dl> <dt>**TBS \_ RIGHT**</dt> </dl>                                  | Il controllo trackbar visualizza segni di graduazione a destra del controllo. Questo stile è valido solo con TBS \_ VERT. <br/>                                                                                                                                                                                                                                            |
| <span id="TBS_BOTH"></span><span id="tbs_both"></span><dl> <dt>**TBS \_ BOTH**</dt> </dl>                                     | Il controllo trackbar visualizza segni di graduazione su entrambi i lati del controllo. Questo valore sarà sia superiore che inferiore se usato con TBS HORZ o sia a sinistra che a destra se usato \_ con TBS \_ VERT. <br/>                                                                                                                                                                           |
| <span id="TBS_NOTICKS"></span><span id="tbs_noticks"></span><dl> <dt>**NOTICK DA \_ TB**</dt> </dl>                            | Il controllo trackbar non visualizza alcun segno di graduazione. <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TBS_ENABLESELRANGE"></span><span id="tbs_enableselrange"></span><dl> <dt>**TBS \_ ENABLESELRANGE**</dt> </dl>       | Il controllo trackbar visualizza solo un intervallo di selezione. I segni di graduazione nelle posizioni iniziale e finale di un intervallo di selezione vengono visualizzati come triangoli (anziché trattini verticali) e l'intervallo di selezione viene evidenziato. <br/>                                                                                                                           |
| <span id="TBS_FIXEDLENGTH"></span><span id="tbs_fixedlength"></span><dl> <dt>**TBS \_ FIXEDLENGTH**</dt> </dl>                | Il controllo trackbar consente di modificare le dimensioni del dispositivo di scorrimento con il [**\_ messaggio TBM SETTHUMBLENGTH.**](tbm-setthumblength.md) <br/>                                                                                                                                                                                                                      |
| <span id="TBS_NOTHUMB"></span><span id="tbs_nothumb"></span><dl> <dt>**TBS \_ NOTHUMB**</dt> </dl>                            | Il controllo trackbar non visualizza un dispositivo di scorrimento. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOOLTIPS"></span><span id="tbs_tooltips"></span><dl> <dt>**DESCRIZIONI \_ COMANDO TBS**</dt> </dl>                         | [Versione 4.70.](common-control-versions.md) Il controllo trackbar supporta le descrizioni comando. Quando un controllo trackbar viene creato usando questo stile, crea automaticamente un controllo descrizione comando predefinito che visualizza la posizione corrente del dispositivo di scorrimento. È possibile modificare la posizione in cui vengono visualizzate le descrizioni comando usando il messaggio [**\_ TBM SETTIPSIDE.**](tbm-settipside.md) <br/> |
| <span id="TBS_REVERSED"></span><span id="tbs_reversed"></span><dl> <dt>**TB IN \_ ORDINE INVERSO**</dt> </dl>                         | [Versione 5.80.](common-control-versions.md) Questo bit di stile viene usato per i trackbar "invertti", dove un numero più piccolo indica "superiore" e un numero maggiore indica "inferiore". Non ha alcun effetto sul controllo. è semplicemente un'etichetta che può essere controllata per determinare se un trackbar è normale o invertito.<br/>                                             |
| <span id="TBS_DOWNISLEFT"></span><span id="tbs_downisleft"></span><dl> <dt>**TBS \_ DOWNISLEFT**</dt> </dl>                   | Per impostazione predefinita, il controllo trackbar usa verso il basso uguale a destra e verso l'alto uguale a sinistra. Usare lo stile TBS DOWNISLEFT per invertire l'impostazione predefinita, rendendo uguale a \_ sinistra e a destra. <br/>                                                                                                                                                                          |
| <span id="TBS_NOTIFYBEFOREMOVE"></span><span id="tbs_notifybeforemove"></span><dl> <dt>**TBS \_ NOTIFYBEFOREMOVE**</dt> </dl> | [Versione 6.00](common-control-versions.md) **e Windows Vista.** Trackbar deve inviare una notifica all'elemento padre prima di riposizionare il dispositivo di scorrimento a causa dell'azione dell'utente (abilita l'allineamento). <br/>                                                                                                                                                                                   |
| <span id="TBS_TRANSPARENTBKGND"></span><span id="tbs_transparentbkgnd"></span><dl> <dt>**TBS \_ TRANSPARENTBKGND**</dt> </dl> | [Versione 6.00](common-control-versions.md) **e Windows Vista.** Lo sfondo viene dipinta dall'elemento padre tramite il messaggio \_ PRINTCLIENT WM. <br/>                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





