---
title: Codice di notifica di NM_CUSTOMDRAW (TrackBar) (COMmctrl. h)
description: Inviato da un controllo TrackBar per notificare alle finestre padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- Codice di notifica di NM_CUSTOMDRAW (TrackBar)-controlli Windows
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
ms.openlocfilehash: 68ebbffd531fb44e2491d72954ce111db208f2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121731"
---
# <a name="nm_customdraw-trackbar-notification-code"></a>Codice di notifica di NM \_ CUSTOMDRAW (TrackBar)

Inviato da un controllo TrackBar per notificare alle finestre padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) che contiene informazioni sull'operazione di disegno. Il membro **dwItemSpec** di questa struttura conterrà uno dei [valori di disegno personalizzati](custom-draw-values.md) che indica quale parte del controllo viene disegnata. I controlli TrackBar inseriscono i valori seguenti nel membro **dwItemSpec** della struttura per identificare la parte del controllo da disegnare:



| Valore                                                                                                                                                      | Significato                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**\_canale TBCD**</dt> </dl> | Identifica il canale con cui scorre il marcatore Thumb del controllo TrackBar. <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD \_ Thumb**</dt> </dl>       | Identifica il marcatore Thumb del controllo TrackBar. Si tratta della parte del controllo che l'utente sposta. <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**\_TIC TBCD**</dt> </dl>          | Identifica i segni di graduazione di incremento visualizzati lungo il bordo del controllo TrackBar. <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente. Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno. È necessario restituire uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_DODEFAULT CDRF**</dt> </dl>         | Il controllo viene disegnato automaticamente. Non invierà alcun codice di [notifica \_ CUSTOMDRAW di Nm](nm-customdraw.md) aggiuntivo per questo ciclo di disegno. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                             |
| <dl> <dt>**\_NOTIFYITEMDRAW CDRF**</dt> </dl>    | Il controllo invierà una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi. Invierà i codici di notifica di [ \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo il disegno degli elementi. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                         |
| <dl> <dt>**\_NOTIFYPOSTERASE CDRF**</dt> </dl>   | Il controllo invierà una notifica al padre dopo la cancellazione di un elemento. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                              |
| <dl> <dt>**\_NOTIFYPOSTPAINT CDRF**</dt> </dl>   | Il controllo invierà una notifica al padre dopo aver disegnato un elemento. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                             |
| <dl> <dt>**\_NOTIFYSUBITEMDRAW CDRF**</dt> </dl> | [Versione 4,71](common-control-versions.md). Il controllo invierà una notifica all'elemento padre quando viene disegnato un sottoelemento di visualizzazione elenco. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                               |
| <dl> <dt>**\_NEWFONT CDRF**</dt> </dl>           | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. il controllo utilizzerà il nuovo tipo di carattere. Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere [modifica di tipi di carattere e colori](custom-draw.md). Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**\_SKIPDEFAULT CDRF**</dt> </dl>       | L'applicazione ha disegnato manualmente l'elemento. L'elemento non viene disegnato dal controllo. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di un progetto personalizzato](custom-draw.md)
</dt> </dl>

 

 





