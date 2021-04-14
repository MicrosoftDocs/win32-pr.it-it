---
title: Codice di notifica EN_LINK (RichEdit. h)
description: Un controllo Rich Edit invia \_ i codici di notifica dei collegamenti it quando riceve diversi messaggi, ad esempio quando l'utente fa clic sul mouse o quando il puntatore del mouse è posizionato su un testo con l' \_ effetto del collegamento CFE.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- Controlli di Windows per il codice di notifica EN_LINK
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0eeb134804f671502d4cd3abbe2cb6995194af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478556"
---
# <a name="en_link-notification-code"></a>\_Codice di notifica del collegamento it

Un controllo Rich Edit invia \_ i codici di notifica dei collegamenti it quando riceve diversi messaggi, ad esempio quando l'utente fa clic sul mouse o quando il puntatore del mouse è posizionato su un testo con l'effetto del **\_ collegamento CFE** . Un controllo Rich Edit senza finestra Invia questa notifica tramite il metodo [**ITextHost:: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) . La finestra padre del controllo riceve questo codice di notifica tramite un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

ID della finestra recuperato chiamando la funzione [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con il \_ valore ID GWL.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**collegamento**](/windows/desktop/api/Richedit/ns-richedit-enlink) . La struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , informazioni sul codice di notifica e una struttura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) che indica l'intervallo di caratteri con effetto di **\_ collegamento CFE** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per consentire al controllo di procedere con la normale gestione del messaggio.

Restituisce un valore diverso da zero per impedire che il controllo gestisca il messaggio.

**Windows 8**: Return **en \_ link \_ ( \_ impostazione predefinita** ) per indirizzare il controllo Rich Edit per eseguire l'azione predefinita.

## <a name="remarks"></a>Commenti

Per ricevere i codici di notifica dei **\_ collegamenti** in quando il collegamento ha lo stato attivo, specificare il flag di [**\_ collegamento ENM**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .

Se il collegamento non ha lo stato attivo, per ricevere i codici di notifica dei **\_ collegamenti it** specificare il flag **ses \_ NOFOCUSLINKNOTIFY** nella maschera inviata con il messaggio [**\_ SETEDITSTYLE em**](em-seteditstyle.md) .

Un controllo Rich Edit invia i codici di notifica di **\_ collegamento it** quando riceve i messaggi seguenti mentre il puntatore del mouse è sopra il testo con l'effetto del **\_ collegamento CFE** :

-   [**\_LBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)
-   [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)
-   [**MOUSEMOVE di WM \_**](/windows/desktop/inputdev/wm-mousemove)
-   [**\_RBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [**\_RBUTTONDOWN WM**](/windows/desktop/inputdev/wm-rbuttondown)
-   [**\_RBUTTONUP WM**](/windows/desktop/inputdev/wm-rbuttonup)
-   [**\_cursore WM**](/windows/desktop/menurc/wm-setcursor)

L'effetto del **\_ collegamento CFE** in genere identifica un intervallo di testo che contiene un URL. Le applicazioni possono gestire il \_ codice di notifica del collegamento it cambiando il puntatore del mouse quando è posizionato sull'URL oppure avviando un browser per visualizzare il percorso identificato dall'URL.

Se si invia il [**messaggio \_ AUTOURLDETECT em**](em-autourldetect.md) per abilitare il rilevamento automatico degli URL, il controllo Rich Edit imposta automaticamente l'effetto del **\_ collegamento CFE** per il testo modificato che identifica come un URL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[**\_AUTOURLDETECT em**](em-autourldetect.md)
</dt> <dt>

[**COLLEGAMENTO**](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[**ITextRange2:: SetURL**](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

