---
title: Codice di notifica NM_CUSTOMDRAW (visualizzazione elenco) (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco per notificare alle finestre padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 4e9b91e3-d042-4fd0-b063-a9e6ea9ad564
keywords:
- Codice di notifica NM_CUSTOMDRAW (visualizzazione elenco) controlli Windows
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
ms.openlocfilehash: 19d8927006f3a6a7e5543f2b072d24469a73a7ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121739"
---
# <a name="nm_customdraw-list-view-notification-code"></a>\_Codice di notifica di CUSTOMDRAW Nm (visualizzazione elenco)

Inviato da un controllo di visualizzazione elenco per notificare alle finestre padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) che contiene informazioni sull'operazione di disegno. Il primo membro della struttura, **NMCD**, è un puntatore a una struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) . Il membro **dwItemSpec** della struttura a cui punta **NMCD** contiene l'identificatore dell'elemento da disegnare e il membro **lItemlParam** contiene i dati definiti dall'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente. Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno. È necessario restituire uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_DODEFAULT CDRF**</dt> </dl>         | Il controllo viene disegnato automaticamente. Non invierà alcun codice di [notifica \_ CUSTOMDRAW di Nm](nm-customdraw.md) aggiuntivo per questo ciclo di disegno. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**\_DOERASE CDRF**</dt> </dl>           | Windows Vista. Il controllo non trarrà il rettangolo di attivazione intorno a un elemento. <br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**\_NOTIFYITEMDRAW CDRF**</dt> </dl>    | Il controllo invierà una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi. Invierà i codici di notifica di [ \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo il disegno degli elementi. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**\_NOTIFYPOSTERASE CDRF**</dt> </dl>   | Il controllo invierà una notifica al padre dopo la cancellazione di un elemento. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**\_NOTIFYPOSTPAINT CDRF**</dt> </dl>   | Il controllo invierà una notifica al padre dopo aver disegnato un elemento. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**\_NEWFONT CDRF**</dt> </dl>           | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. il controllo utilizzerà il nuovo tipo di carattere. Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere [modifica di tipi di carattere e colori](custom-draw.md). Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                                                              |
| <dl> <dt>**\_NOTIFYSUBITEMDRAW CDRF**</dt> </dl> | [Versione 4,71.](common-control-versions.md) L'applicazione riceverà un codice di controllo [nm \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** impostato su CDDS \_ ITEMPREPAINT \| CDDS \_ sottoelemento prima che ogni elemento secondario di visualizzazione elenco venga disegnato. È quindi possibile specificare il tipo di carattere e il colore per ogni elemento secondario separatamente oppure restituire [**CDRF \_ DODEFAULT**](cdrf-constants.md) per l'elaborazione predefinita. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**\_SKIPDEFAULT CDRF**</dt> </dl>       | L'applicazione ha disegnato manualmente l'elemento. L'elemento non viene disegnato dal controllo. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**\_SKIPPOSTPAINT CDRF**</dt> </dl>     | Windows Vista. Il controllo disegna solo lo sfondo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

[Versione 5,80.](common-control-versions.md) Se si modifica il tipo di carattere restituendo [**CDRF \_ NEWFONT**](cdrf-constants.md), il controllo elenco-visualizzazione potrebbe visualizzare il testo ritagliato. Questo comportamento è necessario per garantire la compatibilità con le versioni precedenti dei controlli comuni. Se si vuole modificare il tipo di carattere di un controllo visualizzazione elenco, si otterranno risultati migliori se si invia un messaggio di tipo [**CCM \_**](ccm-setversion.md) con il valore *wParam* impostato su 5 prima di aggiungere elementi al controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





