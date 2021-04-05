---
title: Codice di notifica di NM_CUSTOMDRAW (visualizzazione albero) (COMmctrl. h)
description: Inviato da un controllo di visualizzazione albero per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- NM_CUSTOMDRAW (visualizzazione albero) controlli di Windows per il codice di notifica
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
ms.openlocfilehash: 2bb3f7b44748c2ac9c5b9651c079a8b90df0c508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873317"
---
# <a name="nm_customdraw-tree-view-notification-code"></a>\_Codice di notifica di CUSTOMDRAW Nm (visualizzazione albero)

Inviato da un controllo di visualizzazione albero per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) che contiene e riceve informazioni sull'operazione di disegno. Il membro **dwItemSpec** del membro **NMCD** di questa struttura contiene l'handle dell'elemento da disegnare. Il membro **lItemlParam** del membro **NMCD** di questa struttura contiene il *lParam* dell'elemento da disegnare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente. Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno. È necessario restituire uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_DODEFAULT CDRF**</dt> </dl>         | Il controllo disegna se stesso. Non invia alcun codice [ \_ CUSTOMDRAW Nm](nm-customdraw.md) aggiuntivo per questo ciclo di disegno. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                              |
| <dl> <dt>**\_NOTIFYITEMDRAW CDRF**</dt> </dl>    | Il controllo Invia una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi. Invia i codici di notifica di [ \_ CUSTOMDRAW di Nm](nm-customdraw.md) prima e dopo il disegno di elementi. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                |
| <dl> <dt>**\_NOTIFYPOSTERASE CDRF**</dt> </dl>   | Il controllo Invia una notifica all'elemento padre dopo la cancellazione di un elemento. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                                  |
| <dl> <dt>**\_NOTIFYPOSTPAINT CDRF**</dt> </dl>   | Il controllo Invia una notifica al padre dopo aver disegnato un elemento. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                                |
| <dl> <dt>**\_NOTIFYSUBITEMDRAW CDRF**</dt> </dl> | [Versione 4,71.](common-control-versions.md) Il controllo Invia una notifica all'elemento padre quando viene disegnato un sottoelemento di visualizzazione elenco. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                  |
| <dl> <dt>**\_NEWFONT CDRF**</dt> </dl>           | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. il controllo utilizzerà il nuovo tipo di carattere. Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere [modifica di tipi di carattere e colori](custom-draw.md). Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**\_SKIPDEFAULT CDRF**</dt> </dl>       | L'applicazione ha disegnato manualmente l'elemento. L'elemento non viene disegnato dal controllo. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

[Versione 5,80.](common-control-versions.md) Se si modifica il tipo di carattere restituendo [**CDRF \_ NEWFONT**](cdrf-constants.md), il controllo di visualizzazione albero potrebbe visualizzare il testo ritagliato. Questo comportamento è necessario per garantire la compatibilità con le versioni precedenti dei controlli comuni. Se si desidera modificare il tipo di carattere di un controllo di visualizzazione albero, è possibile ottenere risultati migliori se si invia un messaggio della [**\_ versione CCM**](ccm-setversion.md) con il valore *wParam* impostato su 5 prima di aggiungere elementi al controllo.

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

 

 





