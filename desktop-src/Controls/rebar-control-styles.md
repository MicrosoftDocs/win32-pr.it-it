---
title: Stili del controllo Rebar (CommCtrl. h)
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
ms.openlocfilehash: 67b9f447df2cbf1bb2b956a7ec300d1f29280eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327603"
---
# <a name="rebar-control-styles"></a>Stili del controllo Rebar

I controlli Rebar supportano un'ampia gamma di stili di controllo oltre agli stili di finestra standard.



| Costante                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RBS_AUTOSIZE"></span><span id="rbs_autosize"></span><dl> <dt>**\_ridimensionamento automatico RBS**</dt> </dl>                      | [Versione 4,71](common-control-versions.md). Il controllo Rebar cambierà automaticamente il layout delle bande quando cambiano le dimensioni o la posizione del controllo. Quando si verifica questa situazione, viene inviata una notifica di [RBN \_ AUTOSIZE](rbn-autosize.md) .<br/>                                                                                              |
| <span id="RBS_BANDBORDERS"></span><span id="rbs_bandborders"></span><dl> <dt>**\_BANDBORDERS RBS**</dt> </dl>             | [Versione 4,71](common-control-versions.md). Il controllo Rebar Visualizza linee strette per separare le bande adiacenti.<br/>                                                                                                                                                                                                                                 |
| <span id="RBS_DBLCLKTOGGLE"></span><span id="rbs_dblclktoggle"></span><dl> <dt>**\_DBLCLKTOGGLE RBS**</dt> </dl>          | [Versione 4,71](common-control-versions.md). La banda Rebar attiverà lo stato ingrandito o ridotto a icona quando l'utente fa doppio clic sulla banda. Senza questo stile, lo stato ingrandito o ridotto a icona viene attivato o disattivato quando l'utente fa clic sulla banda.<br/>                                                                                          |
| <span id="RBS_FIXEDORDER"></span><span id="rbs_fixedorder"></span><dl> <dt>**\_FIXEDORDER RBS**</dt> </dl>                | [Versione 4,70](common-control-versions.md). Il controllo Rebar Visualizza sempre le bande nello stesso ordine. È possibile spostare bande in righe diverse, ma l'ordine delle bande è statico.<br/>                                                                                                                                                                      |
| <span id="RBS_REGISTERDROP"></span><span id="rbs_registerdrop"></span><dl> <dt>**\_REGISTERDROP RBS**</dt> </dl>          | [Versione 4,71](common-control-versions.md). Il controllo Rebar genera codici di notifica [ \_ GetObject RBN](rbn-getobject.md) quando un oggetto viene trascinato su una banda nel controllo. Per ricevere le \_ notifiche RBN GetObject, inizializzare OLE con una chiamata a [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) o [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).<br/> |
| <span id="RBS_TOOLTIPS"></span><span id="rbs_tooltips"></span><dl> <dt>**\_descrizioni comando di RBS**</dt> </dl>                      | [Versione 4,71](common-control-versions.md). Non ancora supportato.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="RBS_VARHEIGHT"></span><span id="rbs_varheight"></span><dl> <dt>**\_VARHEIGHT RBS**</dt> </dl>                   | [Versione 4,71](common-control-versions.md). Il controllo Rebar Visualizza le bande con l'altezza minima richiesta, quando possibile. Senza questo stile, il controllo Rebar Visualizza tutte le bande alla stessa altezza, usando l'altezza della banda visibile più alta per determinare l'altezza di altre bande.<br/>                                                   |
| <span id="RBS_VERTICALGRIPPER"></span><span id="rbs_verticalgripper"></span><dl> <dt>**\_VERTICALGRIPPER RBS**</dt> </dl> | [Versione 4,71](common-control-versions.md). Il riquadro di ridimensionamento verrà visualizzato verticalmente anziché orizzontalmente in un controllo Rebar verticale. Questo stile viene ignorato per i controlli Rebar che non hanno lo stile di [**\_ vertici CCS**](common-control-styles.md) .<br/>                                                                            |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

