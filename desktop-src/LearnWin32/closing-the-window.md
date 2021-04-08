---
title: Chiusura della finestra
description: Quando l'utente chiude una finestra, tale azione attiva una sequenza di messaggi di finestra.
ms.assetid: f0449f11-0569-4a3a-92bc-bced7e0db516
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6422966d6b0351654632a1c77b7ebf07e2b5ffef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872533"
---
# <a name="closing-the-window"></a>Chiusura della finestra

Quando l'utente chiude una finestra, tale azione attiva una sequenza di messaggi di finestra.

L'utente può chiudere una finestra dell'applicazione facendo clic sul pulsante **Chiudi** oppure utilizzando un tasto di scelta rapida, ad esempio ALT + F4. Ognuna di queste azioni causa la ricezione di un messaggio [**di \_ chiusura WM**](/windows/desktop/winmsg/wm-close) da parte della finestra. Il messaggio **WM \_ Close** consente di richiedere conferma all'utente prima di chiudere la finestra. Se si vuole effettivamente chiudere la finestra, chiamare la funzione [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) . In caso contrario, è sufficiente restituire zero dal messaggio **WM \_ Close** e il sistema operativo ignorerà il messaggio e non eliminerà definitivamente la finestra.

Di seguito è riportato un esempio di come un programma può gestire [**WM \_ Close**](/windows/desktop/winmsg/wm-close).

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

In questo esempio, la funzione [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) Mostra una finestra di dialogo modale che contiene i pulsanti **OK** e **Annulla** . Se l'utente fa clic su **OK**, il programma chiama [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow). In caso contrario, se l'utente fa clic su **Annulla**, la chiamata a **DestroyWindow** viene ignorata e la finestra rimane aperta. In entrambi i casi, restituire zero per indicare che è stato gestito il messaggio.

Se si desidera chiudere la finestra senza richiedere conferma all'utente, è possibile chiamare semplicemente [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) senza la chiamata a [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox). Tuttavia, in questo caso è presente un collegamento. Ricordare che [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) esegue l'azione predefinita per qualsiasi messaggio della finestra. Nel caso di [**WM \_ Close**](/windows/desktop/winmsg/wm-close), **DefWindowProc** chiama automaticamente **DestroyWindow**. Ciò significa che se si ignora il messaggio **WM \_ Close** nell'istruzione **Switch** , la finestra viene distrutta per impostazione predefinita.

Quando una finestra sta per essere distrutta, riceve un messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) . Questo messaggio viene inviato dopo la rimozione della finestra dallo schermo, ma prima che venga eseguita la distruzione (in particolare, prima che qualsiasi finestra figlio venga distrutta).

Nella finestra principale dell'applicazione, in genere si risponde a [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) chiamando [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

Nella sezione messaggi della [finestra](window-messages.md) è stato visualizzato un messaggio [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) nella coda di messaggi [**, che causa**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) la fine del ciclo di messaggi.

Ecco un diagramma di flusso che mostra il modo tipico per elaborare i messaggi [**WM \_ Close**](/windows/desktop/winmsg/wm-close) e [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) :

![diagramma di flusso che illustra come gestire \- i messaggi WM Close e WM \- Destroy](images/wmclose01.png)

## <a name="next"></a>Prossima

[Gestione dello stato di un'applicazione](managing-application-state-.md)