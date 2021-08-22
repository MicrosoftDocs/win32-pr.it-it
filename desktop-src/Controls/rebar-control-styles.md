---
title: Stili del controllo Rebar (CommCtrl.h)
description: I controlli Rebar supportano un'ampia gamma di stili di controllo oltre agli stili di finestra standard.
ms.assetid: 9690a4bd-51bd-4df9-8988-7da3ece7899f
topic_type:
- apiref
api_name:
- RBS_AUTOSIZE
- RBS_BANDBORDERS
- RBS_DBLCLKTOGGLE
- RBS_FIXEDORDER
- RBS_REGISTERDROP
- RBS_TOOLTIPS
- RBS_VARHEIGHT
- RBS_VERTICALGRIPPER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e40a2f93820391d0c2b928c67784157c1f58d7995d42c51df5373d642bd796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078525"
---
# <a name="rebar-control-styles"></a>Stili del controllo Rebar

I controlli Rebar supportano un'ampia gamma di stili di controllo oltre agli stili di finestra standard.



| Costante                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RBS_AUTOSIZE"></span><span id="rbs_autosize"></span><dl> <dt>**RBS \_ AUTOSIZE**</dt> </dl>                      | [Versione 4.71.](common-control-versions.md) Il controllo Rebar cambierà automaticamente il layout delle bande quando cambiano le dimensioni o la posizione del controllo. In questo caso, verrà inviata una notifica [RBN \_ AUTOSIZE.](rbn-autosize.md)<br/>                                                                                              |
| <span id="RBS_BANDBORDERS"></span><span id="rbs_bandborders"></span><dl> <dt>**RBS \_ BANDBORDERS**</dt> </dl>             | [Versione 4.71.](common-control-versions.md) Il controllo Rebar visualizza linee ristrette per separare le bande adiacenti.<br/>                                                                                                                                                                                                                                 |
| <span id="RBS_DBLCLKTOGGLE"></span><span id="rbs_dblclktoggle"></span><dl> <dt>**RBS \_ DBLCLKTOGGLE**</dt> </dl>          | [Versione 4.71.](common-control-versions.md) La banda rebar attiva o disattiva lo stato ingrandito o ridotto a icona quando l'utente fa doppio clic sulla banda. Senza questo stile, lo stato ingrandito o ridotto a icona viene attivato o disattivato quando l'utente fa clic sulla banda.<br/>                                                                                          |
| <span id="RBS_FIXEDORDER"></span><span id="rbs_fixedorder"></span><dl> <dt>**RBS \_ FIXEDORDER**</dt> </dl>                | [Versione 4.70.](common-control-versions.md) Il controllo Rebar visualizza sempre le bande nello stesso ordine. È possibile spostare le bande in righe diverse, ma l'ordine delle bande è statico.<br/>                                                                                                                                                                      |
| <span id="RBS_REGISTERDROP"></span><span id="rbs_registerdrop"></span><dl> <dt>**RBS \_ REGISTERDROP**</dt> </dl>          | [Versione 4.71.](common-control-versions.md) Il controllo Rebar genera codici [di notifica \_ RBN GETOBJECT](rbn-getobject.md) quando un oggetto viene trascinato su una banda nel controllo. Per ricevere le notifiche \_ GETOBJECT RBN, inizializzare OLE con una chiamata a [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) o [**CoInitialize.**](/windows/desktop/api/objbase/nf-objbase-coinitialize)<br/> |
| <span id="RBS_TOOLTIPS"></span><span id="rbs_tooltips"></span><dl> <dt>**DESCRIZIONI COMANDO \_ DI RBS**</dt> </dl>                      | [Versione 4.71.](common-control-versions.md) Non ancora supportato.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="RBS_VARHEIGHT"></span><span id="rbs_varheight"></span><dl> <dt>**RBS \_ VARHEIGHT**</dt> </dl>                   | [Versione 4.71.](common-control-versions.md) Il controllo Rebar visualizza le bande all'altezza minima richiesta, quando possibile. Senza questo stile, il controllo Rebar visualizza tutte le bande alla stessa altezza, usando l'altezza della banda visibile più alta per determinare l'altezza di altre bande.<br/>                                                   |
| <span id="RBS_VERTICALGRIPPER"></span><span id="rbs_verticalgripper"></span><dl> <dt>**RBS \_ VERTICALGROPPER**</dt> </dl> | [Versione 4.71.](common-control-versions.md) Il ridimensionamento verrà visualizzato verticalmente anziché orizzontalmente in un controllo Rebar verticale. Questo stile viene ignorato per i controlli Rebar che non hanno lo [**stile CCS \_ VERT.**](common-control-styles.md)<br/>                                                                            |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

