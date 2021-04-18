---
title: Flag di maschera eventi del controllo Rich Edit (RichEdit. h)
description: La maschera eventi specifica i codici di notifica che un controllo Rich Edit invia alla finestra padre. La maschera di evento può essere None o una combinazione di questi valori.
ms.assetid: ae0d2cbe-5cbc-42bb-aeb1-7e6be846a4ba
topic_type:
- apiref
api_name:
- ENM_CHANGE
- ENM_CLIPFORMAT
- ENM_CORRECTTEXT
- ENM_DRAGDROPDONE
- ENM_DROPFILES
- ENM_IMECHANGE
- ENM_KEYEVENTS
- ENM_LINK
- ENM_LOWFIRTF
- ENM_MOUSEEVENTS
- ENM_OBJECTPOSITIONS
- ENM_PARAGRAPHEXPANDED
- ENM_PROTECTED
- ENM_REQUESTRESIZE
- ENM_SCROLL
- ENM_SCROLLEVENTS
- ENM_SELCHANGE
- ENM_UPDATE
api_location:
- RichEdit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 006a6d82e7aa4958b03360d05d29a78564f99db7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327602"
---
# <a name="rich-edit-control-event-mask-flags"></a>Flag di maschera eventi controllo Rich Edit

La maschera eventi specifica i codici di notifica che un controllo Rich Edit invia alla finestra padre. La maschera di evento può essere None o una combinazione di questi valori.



| Costante                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENM_CHANGE"></span><span id="enm_change"></span><dl> <dt>**\_modifica ENM**</dt> </dl>                                  | Invia le notifiche di [ \_ modifica](en-change--rich-edit-control-.md) .<br/>                                                                                                                                                                                                                                   |
| <span id="ENM_CLIPFORMAT"></span><span id="enm_clipformat"></span><dl> <dt>**\_CLIPFORMAT ENM**</dt> </dl>                      | Invia notifiche [en \_ CLIPFORMAT](/windows/desktop/Controls/en-clipformat) .<br/>                                                                                                                                                                                                                                          |
| <span id="ENM_CORRECTTEXT"></span><span id="enm_correcttext"></span><dl> <dt>**\_CORRECTTEXT ENM**</dt> </dl>                   | Invia notifiche [en \_ CORRECTTEXT](en-correcttext.md) .<br/>                                                                                                                                                                                                                                             |
| <span id="ENM_DRAGDROPDONE"></span><span id="enm_dragdropdone"></span><dl> <dt>**\_DRAGDROPDONE ENM**</dt> </dl>                | Invia notifiche [en \_ DRAGDROPDONE](en-dragdropdone.md) .<br/>                                                                                                                                                                                                                                           |
| <span id="ENM_DROPFILES"></span><span id="enm_dropfiles"></span><dl> <dt>**\_DropFiles ENM**</dt> </dl>                         | Invia notifiche [en \_ DropFiles](en-dropfiles.md) .<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_IMECHANGE"></span><span id="enm_imechange"></span><dl> <dt>**\_IMECHANGE ENM**</dt> </dl>                         | Solo Microsoft Rich Edit 1,0: Invia notifiche [en \_ IMECHANGE](en-imechange.md) quando lo stato della conversione IME è stato modificato. Solo per le versioni in lingua asiatica del sistema operativo.<br/>                                                                                                              |
| <span id="ENM_KEYEVENTS"></span><span id="enm_keyevents"></span><dl> <dt>**ENM di \_ UNIformi**</dt> </dl>                         | Invia notifiche [en \_ msgfilter](en-msgfilter.md) per gli eventi della tastiera.<br/>                                                                                                                                                                                                                             |
| <span id="ENM_LINK"></span><span id="enm_link"></span><dl> <dt>**\_collegamento ENM**</dt> </dl>                                        | **Rich Edit 2,0 e versioni successive:** Invia notifiche di [ \_ collegamento it](en-link.md) quando il puntatore del mouse è sopra il testo con il \_ collegamento CFE e viene eseguita una delle diverse azioni del mouse.<br/>                                                                                                                     |
| <span id="ENM_LOWFIRTF"></span><span id="enm_lowfirtf"></span><dl> <dt>**\_LOWFIRTF ENM**</dt> </dl>                            | Invia notifiche [en \_ LOWFIRTF](en-lowfirtf.md) .<br/>                                                                                                                                                                                                                                                   |
| <span id="ENM_MOUSEEVENTS"></span><span id="enm_mouseevents"></span><dl> <dt>**\_MOUSEEVENTS ENM**</dt> </dl>                   | Invia notifiche [en \_ msgfilter](en-msgfilter.md) per gli eventi del mouse.<br/>                                                                                                                                                                                                                                |
| <span id="ENM_OBJECTPOSITIONS"></span><span id="enm_objectpositions"></span><dl> <dt>**\_OBJECTPOSITIONS ENM**</dt> </dl>       | Invia notifiche [en \_ OBJECTPOSITIONS](en-objectpositions.md) .<br/>                                                                                                                                                                                                                                     |
| <span id="ENM_PARAGRAPHEXPANDED"></span><span id="enm_paragraphexpanded"></span><dl> <dt>**\_PARAGRAPHEXPANDED ENM**</dt> </dl> | Invia notifiche [en \_ PARAGRAPHEXPANDED](/windows/desktop/Controls/en-paragraphexpanded) .<br/>                                                                                                                                                                                                                            |
| <span id="ENM_PROTECTED"></span><span id="enm_protected"></span><dl> <dt>**ENM \_ protetto**</dt> </dl>                         | Invia notifiche [it \_ protette](en-protected.md) .<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_REQUESTRESIZE"></span><span id="enm_requestresize"></span><dl> <dt>**\_REQUESTRESIZE ENM**</dt> </dl>             | Invia notifiche [en \_ REQUESTRESIZE](en-requestresize.md) .<br/>                                                                                                                                                                                                                                         |
| <span id="ENM_SCROLL"></span><span id="enm_scroll"></span><dl> <dt>**\_scorrimento ENM**</dt> </dl>                                  | Invia le notifiche [en \_ HSCROLL](en-hscroll.md) e [en \_ VSCROLL](en-vscroll.md) .<br/>                                                                                                                                                                                                                   |
| <span id="ENM_SCROLLEVENTS"></span><span id="enm_scrollevents"></span><dl> <dt>**\_SCROLLEVENTS ENM**</dt> </dl>                | Invia notifiche [en \_ msgfilter](en-msgfilter.md) per gli eventi della rotellina del mouse.<br/>                                                                                                                                                                                                                          |
| <span id="ENM_SELCHANGE"></span><span id="enm_selchange"></span><dl> <dt>**\_selChange ENM**</dt> </dl>                         | Invia notifiche [en \_ selChange](en-selchange.md) .<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_UPDATE"></span><span id="enm_update"></span><dl> <dt>**aggiornamento di ENM \_**</dt> </dl>                                  | Invia le notifiche di [ \_ aggiornamento](en-update.md) . <br/> **Rich Edit 2,0 e versioni successive:** questo flag viene ignorato e le notifiche di [ \_ aggiornamento en](en-update.md) vengono inviate sempre. Tuttavia, se Rich Edit 3,0 emula Microsoft Rich Edit 1,0, è necessario usare questo flag per inviare le \_ notifiche di aggiornamento.<br/> |



## <a name="remarks"></a>Commenti

La maschera di evento predefinita è ENM \_ None, nel qual caso non viene inviata alcuna notifica alla finestra padre. È possibile recuperare e impostare la maschera eventi per un controllo Rich Edit usando i messaggi [**em \_ GETEVENTMASK**](em-geteventmask.md) e [**em \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>RichEdit. h</dt> </dl> |



 

