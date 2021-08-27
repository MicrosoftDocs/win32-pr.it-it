---
title: NM_CUSTOMDRAW di notifica (visualizzazione elenco) (Commctrl.h)
description: Inviato da un controllo visualizzazione elenco per notificare alle finestre padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 4e9b91e3-d042-4fd0-b063-a9e6ea9ad564
keywords:
- NM_CUSTOMDRAW di notifica (visualizzazione elenco) Windows controlli
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
ms.openlocfilehash: ba991f5af43ee5513ec0713208aed84319bd5a9a
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812678"
---
# <a name="nm_customdraw-list-view-notification-code"></a>Codice \_ di notifica NM CUSTOMDRAW (visualizzazione elenco)

Inviato da un controllo visualizzazione elenco per notificare alle finestre padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) che contiene informazioni sull'operazione di disegno. Il primo membro di questa struttura, **nmcd**, è un puntatore a [**una struttura NMCUSTOMDRAW.**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) Il **membro dwItemSpec** della struttura a cui punta **nmcd** contiene l'identificatore dell'elemento da disegnare e il membro **lItemlParam** contiene i dati definiti dall'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente. Il **membro dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata contiene un valore che specifica la fase di disegno. È necessario restituire uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | Il controllo verrà di disegno. Non invierà codici di notifica [NM \_ CUSTOMDRAW](nm-customdraw.md) aggiuntivi per questo ciclo di disegno. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ DOERASE**</dt> </dl>           | Windows Vista. Il controllo dipingerà solo lo sfondo. <br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Il controllo invierà una notifica all'elemento padre di qualsiasi operazione di disegno correlata all'elemento. Invierà codici [di notifica NM \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo gli elementi di disegno. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Il controllo invierà una notifica all'elemento padre dopo la cancellazione di un elemento. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Il controllo invierà una notifica all'elemento padre dopo il disegno di un elemento. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ PREPAINT.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. Il controllo userà il nuovo tipo di carattere. Per altre informazioni sulla modifica dei tipi di carattere, vedere Modifica [dei tipi di carattere e dei colori.](custom-draw.md) Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versione 4.71.](common-control-versions.md) L'applicazione riceverà un codice di controllo [NM \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** impostato su CDDS \_ ITEMPREPAINT CDDS SUBITEM prima che venga disegnato ogni elemento secondario \| della visualizzazione \_ elenco. È quindi possibile specificare il tipo di carattere e il colore per ogni elemento secondario separatamente o restituire [**CDRF \_ DODEFAULT per**](cdrf-constants.md) l'elaborazione predefinita. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | L'applicazione ha estratto l'elemento manualmente. Il controllo non disegna l'elemento. Questo errore si verifica **quando dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> </dl>     | Windows Vista. Il controllo non disegna il rettangolo di attivazione. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

[Versione 5.80.](common-control-versions.md) Se si modifica il tipo di carattere tramite la restituzione di [**CDRF \_ NEWFONT**](cdrf-constants.md), il controllo visualizzazione elenco potrebbe visualizzare testo ritagliato. Questo comportamento è necessario per la compatibilità con le versioni precedenti dei controlli comuni. Se si vuole modificare il tipo di carattere di un controllo visualizzazione elenco, si otterrà un risultato migliore se si invia un messaggio [**\_ CCM SETVERSION**](ccm-setversion.md) con il valore *wParam* impostato su 5 prima di aggiungere elementi al controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





