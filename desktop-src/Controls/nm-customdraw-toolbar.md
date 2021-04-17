---
title: Codice di notifica NM_CUSTOMDRAW (barra degli strumenti) (COMmctrl. h)
description: Inviato da una barra degli strumenti per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e83a85f4-7955-411d-9a08-29f5b30158c5
keywords:
- Codice di notifica di NM_CUSTOMDRAW (barra degli strumenti) controlli Windows
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
ms.openlocfilehash: c8d1a33e6b7e9a26237813ec3a90e560f05dd9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519318"
---
# <a name="nm_customdraw-toolbar-notification-code"></a>\_Codice di notifica CUSTOMDRAW di Nm (barra degli strumenti)

Inviato da una barra degli strumenti per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW
        
    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

[Versione 4,70](common-control-versions.md). Puntatore a una struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) che contiene informazioni sull'operazione di disegno. Il membro **dwItemSpec** della struttura contiene l'identificatore di comando dell'elemento da disegnare. Il membro **lItemlParam** della struttura contiene il valore **dwData** per l'elemento da disegnare.

[Versione 4,71](common-control-versions.md). Puntatore a una struttura [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) che contiene informazioni sull'operazione di disegno. Il membro **dwItemSpec** del membro **NMCD** di questa struttura contiene l'identificatore di comando dell'elemento da disegnare. Il membro **lItemlParam** del membro **NMCD** di questa struttura contiene il valore **dwData** per l'elemento da disegnare.

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
| <dl> <dt>**\_BLENDICON TBCDRF**</dt> </dl>       | [Versione 5,00](common-control-versions.md). Fondere il pulsante 50% con lo sfondo. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                      |
| <dl> <dt>**TBCDRF \_ NObackground**</dt> </dl>    | [Versione 5,00](common-control-versions.md). Non creare lo sfondo del pulsante. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                        |
| <dl> <dt>**TBCDRF \_ NOedges**</dt> </dl>         | [Versione 4,71](common-control-versions.md). Non creare bordi del pulsante. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                             |
| <dl> <dt>**\_HILITEHOTTRACK TBCDRF**</dt> </dl>  | [Versione 4,71](common-control-versions.md). Usare il membro **clrHighlightHotTrack** della struttura [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) per tracciare lo sfondo degli elementi rilevati con il tasto di scelta. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                        |
| <dl> <dt>**TBCDRF \_ NOoffset**</dt> </dl>        | [Versione 4,71](common-control-versions.md). Non sfalsare il pulsante quando viene premuto. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                |
| <dl> <dt>**TBCDRF \_ NOmark**</dt> </dl>          | Non creare un'evidenziazione predefinita degli elementi con [**TBSTATE \_ contrassegnato**](toolbar-button-states.md). Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                              |
| <dl> <dt>**\_NOETCHEDEFFECT TBCDRF**</dt> </dl>  | [Versione 4,71](common-control-versions.md). Non tracciare effetti incisi per gli elementi disabilitati. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                         |
| <dl> <dt>**\_USECDCOLORS TBCDRF**</dt> </dl>     | [Versione 6,00](common-control-versions.md), solo **Windows Vista** . Usare i colori di disegnare personalizzati per eseguire il rendering del testo indipendentemente dallo stile di visualizzazione.<br/>                                                                                                                                         |



 

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

 

 





