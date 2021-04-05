---
title: Informazioni sui controlli tasto di scelta
description: Un controllo tasto di scelta è una finestra che consente all'utente di immettere una combinazione di sequenze di tasti da utilizzare come tasto di scelta.
ms.assetid: 5f011459-4c30-45d4-9668-19f575b041ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec45d61df535025cff00fee6428f604aa670bf3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730482"
---
# <a name="about-hot-key-controls"></a>Informazioni sui controlli tasto di scelta

Un controllo tasto di scelta è una finestra che consente all'utente di immettere una combinazione di sequenze di tasti da utilizzare come tasto di scelta. Un tasto di scelta è una combinazione di tasti che l'utente può premere per eseguire rapidamente un'azione. Ad esempio, un utente può creare un tasto di scelta che attiva una determinata finestra e la porta nella parte superiore dell'ordine z. Il controllo tasto di scelta consente di visualizzare le scelte dell'utente e garantisce che l'utente selezioni una combinazione di tasti valida. Lo screenshot seguente mostra come viene visualizzato un controllo tasto di scelta in una finestra di dialogo dopo che l'utente ha premuto Alt.

![Screenshot di una finestra di dialogo che contiene un controllo tasto di scelta](images/hotkey.png)

## <a name="using-hot-key-controls"></a>Uso di controlli tasto di scelta

Quando l'utente immette una combinazione di tasti da usare come tasto di scelta, i nomi delle chiavi vengono visualizzati nel controllo tasto di scelta. Una combinazione di tasti può essere costituita da un tasto di modifica, ad esempio CTRL, ALT o MAIUSC, e da una chiave di accompagnamento, ad esempio un tasto carattere, un tasto di direzione, un tasto funzione e così via.

Dopo che l'utente ha scelto una combinazione di tasti, l'applicazione recupera la combinazione di tasti dal controllo tasto di scelta e la usa per impostare un tasto di scelta nel sistema. Le informazioni recuperate dal controllo tasto di scelta includono un flag che indica il tasto di modifica e il codice della chiave virtuale della chiave associata.

L'applicazione può utilizzare le informazioni fornite da un controllo tasto di scelta rapida per impostare un tasto di scelta rapida globale o un tasto di scelta rapida specifico del thread. Un tasto di scelta rapida globale è associato a una particolare finestra; consente all'utente di attivare la finestra da qualsiasi parte del sistema. Un'applicazione imposta un tasto di scelta rapida globale usando il messaggio di [**\_ AutoHotkey WM**](/windows/desktop/inputdev/wm-sethotkey) . Ogni volta che l'utente preme un tasto di scelta rapida globale, la finestra specificata in **WM \_ sehotkey** riceve un messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) che specifica il valore del [**tasto di \_ scelta rapida SC**](/windows/desktop/inputdev/wm-sethotkey) . Questo messaggio attiva la finestra che la riceve. Il tasto di scelta rimane valido fino a quando l'applicazione che ha chiamato **WM \_ sehotkey** non viene chiusa.

Un tasto di scelta rapida specifico del thread genera un messaggio di [**\_ scelta rapida WM**](/windows/desktop/inputdev/wm-hotkey) che viene pubblicato all'inizio di un determinato thread, in modo che venga rimosso dall'iterazione successiva del ciclo di messaggi. Un'applicazione imposta un tasto di scelta rapida specifico del thread utilizzando la funzione [**RegisterHotKey**](/windows/desktop/api/winuser/nf-winuser-registerhotkey) .

### <a name="hot-key-control-messages"></a>Messaggi di controllo tasto di scelta

Dopo la creazione di un controllo tasto di scelta, un'applicazione interagisce con esso utilizzando tre messaggi: [**HKM \_ serules**](hkm-setrules.md), [**HKM \_ sehotkey**](hkm-sethotkey.md)e [**HKM \_ GetHotKey**](hkm-gethotkey.md).

Un'applicazione può inviare il messaggio [**HKM \_ serules**](hkm-setrules.md) per specificare un set di combinazioni di tasti CTRL, ALT e MAIUSC considerati tasti di scelta non validi. Se l'applicazione specifica una combinazione di tasti non valida, è necessario specificare anche una combinazione di modificatore predefinita da usare quando l'utente seleziona la combinazione non valida. Quando l'utente immette la combinazione non valida, il sistema esegue un'operazione OR logica sulla combinazione non valida e sulla combinazione predefinita. Il risultato viene considerato una combinazione valida. viene convertito in una stringa e visualizzato nel controllo.

Il [**messaggio \_ sehotkey HKM**](hkm-sethotkey.md) consente a un'applicazione di impostare la combinazione di tasti di scelta rapida per un controllo tasto di scelta. Questo messaggio viene usato in genere anche quando viene creato il controllo tasto di scelta.

Le applicazioni usano il messaggio [**\_ GetHotKey HKM**](hkm-gethotkey.md) per recuperare il codice della chiave virtuale e i flag di modifica del tasto di scelta rapida scelto dall'utente.

### <a name="hot-key-control-notifications"></a>Notifiche di controllo del tasto di scelta

Il controllo tasto di scelta non invia alcun codice di notifica tramite il messaggio di [**\_ notifica WM**](wm-notify.md) . Tuttavia, invierà la notifica di [ \_ modifica en](en-change.md) tramite il messaggio [**di \_ comando WM**](/windows/desktop/menurc/wm-command) quando l'utente modifica il contenuto del controllo.

### <a name="default-hot-key-message-processing"></a>Elaborazione del messaggio del tasto di scelta predefinita

In questa sezione vengono descritti i messaggi della finestra gestiti dalla routine della finestra per la classe della finestra di [**scelta rapida \_**](common-control-window-classes.md) predefinita utilizzata con i controlli tasto di scelta.



|                                                |                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Messaggio**                                    | **Elaborazione eseguita**                                                                                                                                                                                                                                                                                                                      |
| [**\_carattere WM**](/windows/desktop/inputdev/wm-char)               | Recupera il codice della chiave virtuale.                                                                                                                                                                                                                                                                                                               |
| [**creazione di WM \_**](/windows/desktop/winmsg/wm-create)             | Inizializza il controllo tasto di scelta, cancella tutte le regole del tasto di scelta e usa il tipo di carattere di sistema.                                                                                                                                                                                                                                                          |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd)     | Nasconde il cursore, chiama la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) e Mostra di nuovo il cursore.                                                                                                                                                                                                                                     |
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)     | Restituisce una combinazione dei valori [**DLGC \_ WANTCHARS**](/windows/desktop/dlgbox/wm-getdlgcode) e [**DLGC \_ WANTARROWS**](/windows/desktop/dlgbox/wm-getdlgcode) .                                                                                                                                               |
| [**\_tipo di carattere WM GetFont**](/windows/desktop/winmsg/wm-getfont)           | Recupera il tipo di carattere.                                                                                                                                                                                                                                                                                                                           |
| [**KeyDown di WM \_**](/windows/desktop/inputdev/wm-keydown)         | Chiama la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) se il tasto è invio, TAB, barra spaziatrice, CANC, ESC o BACKSPACE. Se il tasto è SHIFT, CTRL o ALT, verifica se la combinazione è valida e, in tal caso, imposta il tasto di scelta utilizzando la combinazione. Tutte le altre chiavi vengono impostate come tasti di scelta rapida senza che la relativa validità venga verificata per prima. |
| [**KEYUP di WM \_**](/windows/desktop/inputdev/wm-keyup)             | Recupera il codice della chiave virtuale.                                                                                                                                                                                                                                                                                                               |
| [**\_KILLFOCUS WM**](/windows/desktop/inputdev/wm-killfocus)     | Elimina il punto di inserimento.                                                                                                                                                                                                                                                                                                                           |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown) | Imposta lo stato attivo sulla finestra.                                                                                                                                                                                                                                                                                                                 |
| [**\_NCCREATE WM**](/windows/desktop/winmsg/wm-nccreate)         | Imposta lo stile della finestra [**WS \_ es \_ CLIENTEDGE**](/windows/desktop/winmsg/extended-window-styles) .                                                                                                                                                                                                                              |
| [**\_disegno WM**](/windows/desktop/gdi/wm-paint)                  | Disegna il controllo tasto di scelta.                                                                                                                                                                                                                                                                                                                   |
| [**\_stato attivo WM**](/windows/desktop/inputdev/wm-setfocus)       | Crea e Mostra il punto di inserimento.                                                                                                                                                                                                                                                                                                                  |
| [**\_tipo di carattere WM**](/windows/desktop/winmsg/wm-setfont)           | Imposta il tipo di carattere.                                                                                                                                                                                                                                                                                                                                |
| [**\_SYSCHAR WM**](/windows/desktop/menurc/wm-syschar)           | Recupera il codice della chiave virtuale.                                                                                                                                                                                                                                                                                                               |
| [**\_SYSKEYDOWN WM**](/windows/desktop/inputdev/wm-syskeydown)   | Chiama la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) se il tasto è invio, TAB, barra spaziatrice, CANC, ESC o BACKSPACE. Se il tasto è SHIFT, CTRL o ALT, verifica se la combinazione è valida e, in tal caso, imposta il tasto di scelta utilizzando la combinazione. Tutte le altre chiavi vengono impostate come tasti di scelta rapida senza che la relativa validità venga verificata per prima. |
| [**\_SYSKEYUP WM**](/windows/desktop/inputdev/wm-syskeyup)       | Recupera il codice della chiave virtuale.                                                                                                                                                                                                                                                                                                               |



 

 

 