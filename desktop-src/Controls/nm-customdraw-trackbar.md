---
title: NM_CUSTOMDRAW di notifica (trackbar) (Commctrl.h)
description: Inviato da un controllo trackbar per notificare alle finestre padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- NM_CUSTOMDRAW di notifica (trackbar) Windows controlli
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d863b180948676342a49615a526c8f6860905744aaf5269468807ad6dc04fa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109551"
---
# <a name="nm_customdraw-trackbar-notification-code"></a>Codice \_ di notifica NM CUSTOMDRAW (trackbar)

Inviato da un controllo trackbar per notificare alle finestre padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) che contiene informazioni sull'operazione di disegno. Il **membro dwItemSpec** di questa struttura [](custom-draw-values.md) conterrà uno dei valori di disegno personalizzati che indica quale parte del controllo viene disegnata. I controlli Trackbar inseriscono i valori seguenti nel **membro dwItemSpec** di questa struttura per identificare la parte del controllo da disegnare:



| Valore                                                                                                                                                      | Significato                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**CANALE \_ TBCD**</dt> </dl> | Identifica il canale lungo cui scorre l'indicatore di scorrimento del controllo trackbar. <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD \_ THUMB**</dt> </dl>       | Identifica l'indicatore di scorrimento del controllo trackbar. Si tratta della parte del controllo spostata dall'utente. <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD \_ TICS**</dt> </dl>          | Identifica i segni di graduazione di incremento visualizzati lungo il bordo del controllo trackbar. <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente. Il **membro dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata contiene un valore che specifica la fase di disegno. È necessario restituire uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | Il controllo verrà di disegno. Non invierà codici di notifica [NM \_ CUSTOMDRAW](nm-customdraw.md) aggiuntivi per questo ciclo di disegno. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Il controllo invierà una notifica all'elemento padre di qualsiasi operazione di disegno correlata all'elemento. Invierà codici [di notifica NM \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo gli elementi di disegno. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                         |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Il controllo invierà una notifica all'elemento padre dopo la cancellazione di un elemento. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Il controllo invierà una notifica all'elemento padre dopo il disegno di un elemento. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versione 4.71.](common-control-versions.md) Il controllo invierà una notifica all'elemento padre quando viene disegnato un elemento secondario della visualizzazione elenco. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                               |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. Il controllo userà il nuovo tipo di carattere. Per altre informazioni sulla modifica dei tipi di carattere, vedere Modifica [dei tipi di carattere e dei colori.](custom-draw.md) Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | L'applicazione ha creato l'elemento manualmente. Il controllo non disegna l'elemento. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso del disegno personalizzato](custom-draw.md)
</dt> </dl>

 

 





