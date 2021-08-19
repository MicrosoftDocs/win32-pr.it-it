---
title: EN_LINK di notifica (Richedit.h)
description: Un controllo Rich Edit invia codici di notifica EN LINK quando riceve vari messaggi, ad esempio quando l'utente fa clic sul mouse o quando il puntatore del mouse è sul testo con \_ l'effetto CFE \_ LINK.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- EN_LINK codice di notifica Windows controlli
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
ms.openlocfilehash: 3398f79a94982a8b7c843747f38f16431cad6a061388367037d259cfe862d468
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047661"
---
# <a name="en_link-notification-code"></a>Codice di notifica EN \_ LINK

Un controllo Rich Edit invia codici di notifica EN LINK quando riceve vari messaggi, ad esempio quando l'utente fa clic sul mouse o quando il puntatore del mouse è sul testo con \_ **l'effetto CFE \_ LINK.** Un controllo Rich Edit senza finestra invia questa notifica usando il [**metodo ITextHost::TxNotify.**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) La finestra padre del controllo riceve questo codice di notifica tramite un [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

ID della finestra recuperato chiamando la [**funzione GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con il valore \_ GWL ID.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura ENLINK.**](/windows/desktop/api/Richedit/ns-richedit-enlink) La struttura contiene una [**struttura NMHDR,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) informazioni sul codice di notifica e una struttura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) che indica l'intervallo di caratteri che hanno l'effetto **CFE \_ LINK.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per consentire al controllo di procedere con la normale gestione del messaggio.

Restituisce un valore diverso da zero per impedire al controllo di gestire il messaggio.

**Windows 8**: restituire **EN LINK DO DEFAULT \_ \_ \_ per** indirizzare il controllo Rich Edit a eseguire l'azione predefinita.

## <a name="remarks"></a>Commenti

Per ricevere **codici di notifica EN \_ LINK** quando il collegamento ha lo stato attivo, specificare il flag [**ENM \_ LINK**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**EM \_ SETEVENTMASK.**](em-seteventmask.md)

Se il collegamento non ha lo stato attivo, per ricevere i codici di notifica **EN \_ LINK** specificare il flag **\_ SES NOFOCUSLINKNOTIFY** nella maschera inviata con il messaggio [**EM \_ SETEDITSTYLE.**](em-seteditstyle.md)

Un controllo Rich Edit invia codici di notifica **EN \_ LINK** quando riceve i messaggi seguenti mentre il puntatore del mouse è posizionato sul testo con **l'effetto CFE \_ LINK:**

-   [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)
-   [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)
-   [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)
-   [**WM \_ RBUTTONDBLCLK**](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)
-   [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)
-   [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor)

**L'effetto \_ CFE LINK** identifica in genere un intervallo di testo che contiene un URL. Le applicazioni possono gestire il codice di notifica EN LINK modificando il puntatore del mouse quando si trova sull'URL o avviando un browser per visualizzare il percorso identificato \_ dall'URL.

Se si invia il messaggio [**EM \_ AUTOURLDETECT**](em-autourldetect.md) per abilitare il rilevamento automatico degli URL, il controllo Rich Edit imposta automaticamente l'effetto **CFE \_ LINK** per il testo modificato identificato come URL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[**EM \_ AUTOURLDETECT**](em-autourldetect.md)
</dt> <dt>

[**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[**ITextRange2::SetURL**](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

