---
title: Messaggi di controllo
description: Questa sezione contiene informazioni sul modo in cui i messaggi di Windows vengono usati per comunicare con i controlli.
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923a1b47d625a2797a900a6c582d00c5169097f3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873173"
---
# <a name="control-messages"></a>Messaggi di controllo

Questa sezione contiene informazioni sul modo in cui i messaggi di Windows vengono usati per comunicare con i controlli.

Vengono illustrati gli argomenti seguenti.

-   [Messaggi ai controlli comuni](#messages-to-common-controls)
-   [Notifiche da controlli](#notifications-from-controls)
-   [Argomenti correlati](#related-topics)

## <a name="messages-to-common-controls"></a>Messaggi ai controlli comuni

Poiché i controlli comuni sono Windows, un'applicazione può comunicare con essi usando messaggi Microsoft Win32 comuni, ad esempio [**WM \_ GetFont**](/windows/desktop/winmsg/wm-getfont) o [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext). Inoltre, la classe della finestra di ogni controllo comune supporta un set di messaggi specifici del controllo. In genere, un'applicazione utilizza [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) per passare messaggi al controllo (spesso ricevendo informazioni nel valore restituito).

Alcuni controlli comuni includono anche un set di macro che un'applicazione può usare anziché [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage). Le macro sono in genere più semplici da utilizzare rispetto alle funzioni. Nell'esempio di codice seguente viene recuperato il testo dell'elemento della visualizzazione albero selezionato, prima utilizzando i messaggi non elaborati e il secondo tramite le macro equivalenti. Si supponga che *HWND* sia l'handle della finestra del controllo.


```
BOOL fSuccess;
WCHAR itemText[99];
TVITEM tvItem = { 0 };
tvItem.mask = TVIF_TEXT;
tvItem.cchTextMax = ARRAYSIZE(itemText);
tvItem.pszText = itemText;

// This...
tvItem.hItem = (HTREEITEM)SendMessage(hwnd, TVM_GETNEXTITEM, TVGN_CARET, NULL);
fSuccess = SendMessage(hwnd, TVM_GETITEM, 0, (LPARAM)&tvItem);

// ... is equivalent to this.
tvItem.hItem = TreeView_GetSelection(hwnd);
fSuccess = TreeView_GetItem(hwnd, &tvItem);
```



Quando viene apportata una modifica alle impostazioni dei colori di sistema, Windows invia un messaggio [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) a tutte le finestre di primo livello. La finestra di primo livello deve trasmettere il messaggio **WM \_ SYSCOLORCHANGE** ai controlli comuni; in caso contrario, i controlli non riceveranno una notifica della modifica del colore. L'invio del messaggio assicura che i colori utilizzati dai controlli comuni siano coerenti con quelli utilizzati da altri oggetti dell'interfaccia utente. Ad esempio, un controllo Toolbar usa il colore "oggetti 3D" per creare i pulsanti. Se l'utente modifica il colore dell'oggetto 3D, ma il messaggio **WM \_ SYSCOLORCHANGE** non viene trasmesso alla barra degli strumenti, i pulsanti della barra degli strumenti rimarranno nel colore originale (o anche in una combinazione di colori vecchi e nuovi), mentre il colore degli altri pulsanti del sistema cambia.

## <a name="notifications-from-controls"></a>Notifiche da controlli

I controlli sono finestre figlio che inviano messaggi di notifica alla finestra padre quando gli eventi, in genere attivati dall'input dell'utente, si verificano nel controllo. L'applicazione si basa su questi messaggi di notifica per determinare l'azione che l'utente desidera eseguire. Ad eccezione di trackbars, che usano i messaggi [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) per notificare al padre le modifiche, i controlli comuni inviano le notifiche tramite il [**\_ comando WM**](/windows/desktop/menurc/wm-command) o [**WM \_ Notify**](wm-notify.md) , come specificato nell'argomento di riferimento per la notifica. In genere, le notifiche precedenti (quelle che sono state nell'API per molto tempo) usano **il \_ comando WM**.

Il parametro *lParam* di [**WM \_ Notify**](wm-notify.md) è l'indirizzo di una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) o l'indirizzo di una struttura più ampia che include **NMHDR** come primo membro. La struttura contiene il codice di notifica e identifica il controllo comune che ha inviato il messaggio di notifica. Il significato degli eventuali membri della struttura rimanenti varia a seconda del codice di notifica.

Ogni tipo di controllo comune ha un set di codici di notifica corrispondente. La libreria di controlli comuni fornisce anche codici di notifica che possono essere inviati da più di un tipo di controllo comune. Vedere la documentazione relativa al controllo di interesse per individuare i codici di notifica che verranno inviati e il formato da essi presi.

Per un esempio di codice che illustra come gestire i messaggi di [**\_ notifica WM**](wm-notify.md) , vedere l'argomento di riferimento per il messaggio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo generale](common-control-reference.md)
</dt> </dl>

 

 
