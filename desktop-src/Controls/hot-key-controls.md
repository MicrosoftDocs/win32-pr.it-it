---
title: Informazioni sui controlli dei tasti di scelta rapida
description: Un controllo tasto di scelta rapida è una finestra che consente all'utente di immettere una combinazione di tasti da usare come tasto di scelta rapida.
ms.assetid: 5f011459-4c30-45d4-9668-19f575b041ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256fcfde87a1fb6603f90e8a2a41cb4f2cc9356f9f45d861efdc6836aa5344fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672245"
---
# <a name="about-hot-key-controls"></a>Informazioni sui controlli dei tasti di scelta rapida

Un controllo tasto di scelta rapida è una finestra che consente all'utente di immettere una combinazione di tasti da usare come tasto di scelta rapida. Un tasto di scelta rapida è una combinazione di tasti che l'utente può premere per eseguire rapidamente un'azione. Ad esempio, un utente può creare un tasto di scelta rapida che attiva una determinata finestra e la porta all'inizio dell'ordine Z. Il controllo tasto di scelta visualizza le scelte dell'utente e assicura che l'utente selezioni una combinazione di tasti valida. Lo screenshot seguente mostra come viene visualizzato un controllo tasto di scelta rapida in una finestra di dialogo dopo che l'utente preme ALT.

![Screenshot di una finestra di dialogo che contiene un controllo tasto di scelta rapida](images/hotkey.png)

## <a name="using-hot-key-controls"></a>Uso dei controlli tasto di scelta rapida

Quando l'utente immette una combinazione di tasti da usare come tasto di scelta rapida, i nomi dei tasti vengono visualizzati nel controllo tasto di scelta rapida. Una combinazione di tasti può essere costituita da un tasto di modifica (ad esempio CTRL, ALT o MAIUSC) e da un tasto di scelta rapida (ad esempio un tasto carattere, un tasto di direzione, un tasto funzione e così via).

Dopo che l'utente ha scelto una combinazione di tasti, l'applicazione recupera la combinazione di tasti dal controllo tasto di scelta rapida e la usa per configurare un tasto di scelta rapida nel sistema. Le informazioni recuperate dal controllo tasto di scelta rapida includono un flag che indica il tasto di modifica e il codice del tasto virtuale del tasto associato.

L'applicazione può usare le informazioni fornite da un controllo tasto di scelta rapida per configurare un tasto di scelta rapida globale o un tasto di scelta rapida specifico del thread. Un tasto di scelta rapida globale è associato a una determinata finestra. consente all'utente di attivare la finestra da qualsiasi parte del sistema. Un'applicazione imposta un tasto di scelta rapida globale usando il [**messaggio WM \_ SETHOTKEY.**](/windows/desktop/inputdev/wm-sethotkey) Ogni volta che l'utente preme un tasto di scelta rapida globale, la finestra specificata in **WM \_ SETHOTKEY** riceve un messaggio [**\_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) che specifica il [**valore SC \_ HOTKEY.**](/windows/desktop/inputdev/wm-sethotkey) Questo messaggio attiva la finestra che lo riceve. Il tasto di scelta rapida rimane valido fino alla chiusura dell'applicazione che ha chiamato **WM \_ SETHOTKEY.**

Un tasto di scelta rapida specifico del thread genera un messaggio [**WM \_ HOTKEY**](/windows/desktop/inputdev/wm-hotkey) inviato all'inizio di un thread specifico in modo che venga rimosso dall'iterazione successiva del ciclo di messaggi. Un'applicazione imposta un tasto di scelta rapida specifico del thread usando la [**funzione RegisterHotKey.**](/windows/desktop/api/winuser/nf-winuser-registerhotkey)

### <a name="hot-key-control-messages"></a>Messaggi di controllo dei tasti di scelta rapida

Dopo aver creato un controllo tasto di scelta rapida, un'applicazione interagisce con esso usando tre messaggi: [**HKM \_ SETRULES**](hkm-setrules.md), [**HKM \_ SETHOTKEY**](hkm-sethotkey.md)e [**HKM \_ GETHOTKEY**](hkm-gethotkey.md).

Un'applicazione può inviare il messaggio [**HKM \_ SETRULES**](hkm-setrules.md) per specificare un set di combinazioni di tasti CTRL, ALT e MAIUSC considerate tasti di scelta rapida non validi. Se l'applicazione specifica una combinazione di tasti non valida, deve anche specificare una combinazione di modificatori predefinita da usare quando l'utente seleziona la combinazione non valida. Quando l'utente immette la combinazione non valida, il sistema esegue un'operazione or logica sulla combinazione non valida e sulla combinazione predefinita. Il risultato è considerato una combinazione valida. viene convertito in una stringa e visualizzato nel controllo .

Il [**messaggio HKM \_ SETHOTKEY**](hkm-sethotkey.md) consente a un'applicazione di impostare la combinazione di tasti di scelta rapida per un controllo tasto di scelta rapida. Questo messaggio viene in genere usato anche quando viene creato il controllo tasto di scelta rapida.

Le applicazioni usano il [**messaggio \_ HKM GETHOTKEY**](hkm-gethotkey.md) per recuperare il codice del tasto virtuale e i flag di modifica del tasto di scelta rapida scelto dall'utente.

### <a name="hot-key-control-notifications"></a>Notifiche di controllo dei tasti di scelta rapida

Il controllo tasto di scelta rapida non invia alcun codice di notifica tramite il [**messaggio WM \_ NOTIFY.**](wm-notify.md) Tuttavia, invierà la notifica [EN \_ CHANGE](en-change.md) tramite il [**messaggio WM \_ COMMAND**](/windows/desktop/menurc/wm-command) quando l'utente modifica il contenuto del controllo.

### <a name="default-hot-key-message-processing"></a>Elaborazione predefinita dei messaggi con tasto di scelta rapida

Questa sezione descrive i messaggi della finestra gestiti dalla routine della finestra per la classe di finestra [**HOTKEY \_ CLASS**](common-control-window-classes.md) predefinita usata con i controlli tasto di scelta rapida.

|    Message                                            |    Elaborazione eseguita                               |
|------------------------------------------------|--------------------------------------------------------------|
| [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)               | Recupera il codice della chiave virtuale.             |
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)             | Inizializza il controllo del tasto di scelta rapida, cancella tutte le regole dei tasti di scelta rapida e usa il tipo di carattere di sistema.   |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)     | Nasconde il punto di ingresso, chiama la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) e visualizza di nuovo il punto di ingresso.   |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)     | Restituisce una combinazione dei [**valori DLGC \_ WANTCHARS**](/windows/desktop/dlgbox/wm-getdlgcode) [**e DLGC \_ WANTARROWS.**](/windows/desktop/dlgbox/wm-getdlgcode)   |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)           | Recupera il tipo di carattere.                         |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)         | Chiama la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) se il tasto è INVIO, TAB, BARRA SPAZIATRICE, CANC, ESC o BACKSPACE. Se il tasto è MAIUSC, CTRL o ALT, controlla se la combinazione è valida e, in caso contrario, imposta il tasto di scelta rapida usando la combinazione. Tutte le altre chiavi vengono impostate come tasti di scelta rapida senza prima verificarne la validità. |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)             | Recupera il codice della chiave virtuale.             |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)     | Elimina il caret.                         |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) | Imposta lo stato attivo sulla finestra.               |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)         | Imposta lo [**stile della \_ finestra WS EX \_ CLIENTEDGE.**](/windows/desktop/winmsg/extended-window-styles)        |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                  | Disegna il controllo tasto di scelta rapida.                 |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)       | Crea e mostra il caret.                |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)           | Imposta il tipo di carattere.                              |
| [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)           | Recupera il codice della chiave virtuale.             |
| [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)   | Chiama la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) se il tasto è INVIO, TAB, BARRA SPAZIATRICE, CANC, ESC o BACKSPACE. Se il tasto è MAIUSC, CTRL o ALT, controlla se la combinazione è valida e, in caso contrario, imposta il tasto di scelta rapida usando la combinazione. Tutte le altre chiavi vengono impostate come tasti di scelta rapida senza prima verificarne la validità. |
| [**WM \_ SYSKEYUP**](/windows/desktop/inputdev/wm-syskeyup)       | Recupera il codice della chiave virtuale.             |
