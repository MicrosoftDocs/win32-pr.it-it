---
title: Messaggi di controllo
description: Questa sezione contiene informazioni su come Windows messaggi vengono usati per comunicare con i controlli.
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed60ebb66341332b6248b8427045abc5b62a2311427d56e46b25fe93b3d899ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921101"
---
# <a name="control-messages"></a>Messaggi di controllo

Questa sezione contiene informazioni su come Windows messaggi vengono usati per comunicare con i controlli.

Vengono illustrati gli argomenti seguenti.

-   [Messaggi a controlli comuni](#messages-to-common-controls)
-   [Notifiche dai controlli](#notifications-from-controls)
-   [Argomenti correlati](#related-topics)

## <a name="messages-to-common-controls"></a>Messaggi a controlli comuni

Poiché i controlli comuni sono finestre, un'applicazione può comunicare con essi usando messaggi Microsoft Win32 comuni, ad esempio [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont) o [**WM \_ SETTEXT.**](/windows/desktop/winmsg/wm-settext) Inoltre, la classe finestra di ogni controllo comune supporta un set di messaggi specifici del controllo. In genere, un'applicazione usa [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) per passare messaggi al controllo (spesso ricevendo informazioni nel valore restituito).

Alcuni controlli comuni hanno anche un set di macro che un'applicazione può usare al posto di [**SendMessage.**](/windows/desktop/api/winuser/nf-winuser-sendmessage) Le macro sono in genere più facili da usare rispetto alle funzioni . Nell'esempio di codice seguente viene recuperato il testo dell'elemento della visualizzazione albero selezionato, utilizzando prima i messaggi non elaborati e il secondo tramite le macro equivalenti. Si supponga *che hwnd* sia l'handle della finestra di controllo.


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



Quando viene apportata una modifica alle impostazioni dei colori di sistema, Windows invia un messaggio [**\_ SYSCOLORCHANGE WM**](/windows/desktop/gdi/wm-syscolorchange) a tutte le finestre di primo livello. La finestra di primo livello deve inoltrare il messaggio **\_ SYSCOLORCHANGE DI WM** ai controlli comuni. In caso contrario, i controlli non riceveranno notifica della modifica del colore. L'inoltro del messaggio garantisce che i colori utilizzati dai controlli comuni siano coerenti con quelli usati da altri oggetti dell'interfaccia utente. Ad esempio, un controllo barra degli strumenti usa il colore "Oggetti 3D" per disegnare i pulsanti. Se l'utente modifica il colore dell'oggetto 3D ma il messaggio **WM \_ SYSCOLORCHANGE** non viene inoltrato alla barra degli strumenti, i pulsanti della barra degli strumenti rimarranno nel colore originale (o anche in una combinazione di colori vecchi e nuovi) mentre il colore degli altri pulsanti nel sistema cambia.

## <a name="notifications-from-controls"></a>Notifiche dai controlli

I controlli sono finestre figlio che inviano messaggi di notifica alla finestra padre quando gli eventi, in genere attivati dall'input dell'utente, si verificano nel controllo. L'applicazione si basa su questi messaggi di notifica per determinare l'azione che l'utente vuole eseguire. Ad eccezione dei trackbar, che usano i messaggi [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) per notificare le modifiche all'elemento padre, i controlli comuni inviano notifiche come [**messaggi WM \_ COMMAND**](/windows/desktop/menurc/wm-command) o [**WM \_ NOTIFY,**](wm-notify.md) come specificato nell'argomento di riferimento per la notifica. In genere, le notifiche meno recenti (quelle che sono state nell'API per molto tempo) usano **WM \_ COMMAND.**

Il *parametro lParam* di [**WM \_ NOTIFY**](wm-notify.md) è l'indirizzo di una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) o l'indirizzo di una struttura più grande che include **NMHDR** come primo membro. La struttura contiene il codice di notifica e identifica il controllo comune che ha inviato il messaggio di notifica. Il significato dei membri rimanenti della struttura, se presenti, varia a seconda del codice di notifica.

Ogni tipo di controllo comune ha un set corrispondente di codici di notifica. La libreria di controlli comune fornisce anche codici di notifica che possono essere inviati da più di un tipo di controllo comune. Vedere la documentazione per il controllo di interesse per determinare i codici di notifica che invierà e il formato che avranno.

Per un esempio di codice che illustra come gestire [**i messaggi WM \_ NOTIFY,**](wm-notify.md) vedere l'argomento di riferimento per tale messaggio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento generali sul controllo](common-control-reference.md)
</dt> </dl>

 

 
