---
title: Considerazioni sulla programmazione delle finestre di dialogo
description: In questa panoramica vengono illustrate alcune considerazioni sulla programmazione relative alle finestre di dialogo.
ms.assetid: 49024a0f-ea92-4d56-b063-8e5fcdbd884a
keywords:
- Interfaccia utente di Windows, Windowing
- Interfaccia utente di Windows, finestre di dialogo
- finestre, finestre di dialogo
- finestre di dialogo, informazioni
- routine della finestra di dialogo
- finestre di dialogo, procedure
- Messaggio WM_INITDIALOG
- Messaggio WM_COMMAND
- Messaggio WM_PARENTNOTIFY
- messaggi di colore controllo
- finestre di dialogo, elaborazione dei messaggi
- finestre di dialogo, interfaccia della tastiera
- finestre di dialogo, tasti di scelta
- finestre di dialogo, personalizzate
- finestre di dialogo personalizzate
- finestre di dialogo, impostazioni
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 790abe7c76cdb99f86b2a90a133b15faae721e0e
ms.sourcegitcommit: f7cf41ffc79d1ffead9de2fc61677201f94b423a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2020
ms.locfileid: "106300560"
---
# <a name="dialog-box-programming-considerations"></a>Considerazioni sulla programmazione delle finestre di dialogo

In questa panoramica vengono illustrate alcune considerazioni sulla programmazione relative alle finestre di dialogo.

La panoramica include gli argomenti seguenti.

-   [Routine della finestra di dialogo](#dialog-box-procedures)
    -   [Messaggio WM \_ INITDIALOG](wm-initdialog.md)
    -   [Messaggio del \_ comando WM](/windows/desktop/menurc/wm-command)
    -   [Messaggio WM \_ PARENTNOTIFY](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)
    -   [Messaggi di colore controllo](#control-color-messages)
    -   [Elaborazione dei messaggi predefiniti della finestra di dialogo](#dialog-box-default-message-processing)
-   [Interfaccia della tastiera della finestra di dialogo](#dialog-box-keyboard-interface)
    -   [Stile di WS \_ TABSTOP](/windows/desktop/winmsg/window-styles)
    -   [Stile del \_ gruppo WS](/windows/desktop/winmsg/window-styles)
    -   [Tasti](#mnemonics)
-   [Impostazioni della finestra di dialogo](#dialog-box-settings)
    -   [Pulsanti di opzione e caselle di controllo](#radio-buttons-and-check-boxes)
    -   [Controlli di modifica della finestra di dialogo](#dialog-box-edit-controls)
    -   [Caselle di riepilogo, caselle combinate e elenchi di directory](#list-boxes-combo-boxes-and-directory-listings)
    -   [Messaggi di controllo della finestra di dialogo](#dialog-box-control-messages)
-   [Finestre di dialogo personalizzate](#custom-dialog-boxes)

## <a name="dialog-box-procedures"></a>Routine della finestra di dialogo

Una procedura della finestra di dialogo è simile a una procedura della finestra in quanto il sistema invia messaggi alla procedura quando dispone di informazioni da assegnare o attività da eseguire. A differenza di una routine di finestra, una routine della finestra di dialogo non chiama mai la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Restituisce invece **true** se elabora un messaggio o **false** in caso contrario.

Ogni routine della finestra di dialogo ha il formato seguente:

```cpp
BOOL CALLBACK DlgProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    switch (message) 
    { 
 
        // Place message cases here. 
 
        default: 
            return FALSE; 
    } 
}
```

I parametri della procedura hanno lo stesso scopo di una routine di finestra, con il parametro *hwndDlg* che riceve l'handle della finestra di dialogo.

La maggior parte delle routine della finestra di dialogo elabora il messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) e i messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) inviati dai controlli, ma elabora pochi se sono presenti altri messaggi. Se una routine della finestra di dialogo non elabora un messaggio, deve restituire **false** per indicare al sistema di elaborare internamente i messaggi. L'unica eccezione a questa regola è il messaggio **WM \_ INITDIALOG** . La routine della finestra di dialogo deve restituire **true** per indicare al sistema di elaborare ulteriormente il messaggio **WM \_ INITDIALOG** . In ogni caso, la stored procedure non deve chiamare [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

- [Messaggio WM \_ INITDIALOG](#the-wm_initdialog-message)
- [Messaggio del \_ comando WM](#the-wm_command-message)
- [Messaggio WM \_ PARENTNOTIFY](#the-wm_parentnotify-message)
- [Messaggi di colore controllo](#control-color-messages)
- [Elaborazione dei messaggi predefiniti della finestra di dialogo](#dialog-box-default-message-processing)

### <a name="the-wm_initdialog-message"></a>Messaggio WM \_ INITDIALOG

Il sistema non invia un messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) alla routine della finestra di dialogo. Invia invece un messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) quando crea la finestra di dialogo e tutti i relativi controlli, ma prima di visualizzare la finestra di dialogo. La procedura deve eseguire tutte le inizializzazioni necessarie per assicurarsi che nella finestra di dialogo vengano visualizzate le impostazioni correnti associate all'attività. Ad esempio, quando una finestra di dialogo contiene un controllo per visualizzare l'unità e la directory correnti, la procedura deve determinare l'unità e la directory correnti e impostare il controllo su tale valore.

La procedura può inizializzare i controlli usando funzioni quali [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) e [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx). Poiché i controlli sono Windows, la procedura può anche manipolarli usando funzioni di gestione della finestra, ad esempio [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) e [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus). La procedura può recuperare l'handle della finestra per un controllo tramite la funzione [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) .

La routine della finestra di dialogo può modificare il contenuto, lo stato e la posizione di qualsiasi controllo in base alle esigenze. Ad esempio, in una finestra di dialogo che contiene una casella di riepilogo di nomi file e un pulsante **Apri** , la procedura può disabilitare il pulsante **Apri** fino a quando l'utente non seleziona un file dall'elenco. In questo esempio, il modello di finestra di dialogo Specifica lo stile [**WS \_ disabled**](/windows/desktop/winmsg/window-styles) per il pulsante **Apri** e il sistema Disabilita automaticamente il pulsante al momento della creazione. Quando la routine della finestra di dialogo riceve un messaggio di notifica dalla casella di riepilogo che indica che l'utente ha selezionato un file, la procedura chiama la funzione [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) per abilitare il pulsante **Apri** .

Per visualizzare un'icona personalizzata sulla barra del titolo della finestra di dialogo, il gestore [**WM \_ INITDIALOG**](wm-initdialog.md) può inviare il messaggio di [**\_ icona WM**](/windows/desktop/winmsg/wm-seticon) alla finestra di dialogo.

Se l'applicazione crea la finestra di dialogo utilizzando una delle funzioni [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)o [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), il parametro *lParam* per il messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) contiene il parametro aggiuntivo passato alla funzione. Le applicazioni utilizzano in genere questo parametro aggiuntivo per passare un puntatore a informazioni di inizializzazione aggiuntive alla routine della finestra di dialogo, ma la routine della finestra di dialogo deve determinare il significato del parametro. Se l'applicazione utilizza un'altra funzione per creare la finestra di dialogo, il parametro *lParam* viene impostato su **null**.

Prima di restituire il messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) , la procedura deve determinare se è necessario impostare lo stato attivo per l'input su un controllo specificato. Se la routine della finestra di dialogo restituisce **true**, il sistema imposta automaticamente lo stato attivo per l'input sul controllo il cui handle di finestra si trova nel parametro *wParam* . Se il controllo che riceve lo stato attivo predefinito non è appropriato, può impostare lo stato attivo sul controllo appropriato utilizzando la funzione [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) . Se la procedura imposta lo stato attivo per l'input, deve restituire **false** per impedire che il sistema imposti lo stato attivo predefinito. Il controllo che riceve lo stato attivo per l'input predefinito è sempre il primo controllo specificato nel modello visibile, non disabilitato e con lo stile [WS \_ TABSTOP](/windows/desktop/winmsg/window-styles) . Se non esiste alcun controllo di questo tipo, il sistema imposta lo stato attivo per l'input predefinito sul primo controllo del modello.

### <a name="the-wm_command-message"></a>Messaggio del \_ comando WM

Un controllo può inviare un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) alla routine della finestra di dialogo quando l'utente esegue un'azione nel controllo. Questi messaggi, detti messaggi di notifica, informano la procedura di input dell'utente e consentono di eseguire le risposte appropriate.

Tutti i controlli predefiniti, eccetto i controlli statici, inviano messaggi di notifica per le azioni utente selezionate. Ad esempio, un pulsante di push invia il messaggio di notifica [**\_ fatto clic su BN**](../controls/bn-clicked.md) ogni volta che l'utente fa clic sul pulsante. In tutti i casi, la parola più bassa del parametro *wParam* contiene l'identificatore di controllo, la parola più significativa di *wParam* contiene il codice di notifica e il parametro *lParam* contiene l'handle della finestra di controllo.

La routine della finestra di dialogo deve monitorare ed elaborare i messaggi di notifica. In particolare, la procedura deve elaborare i messaggi con gli identificatori IDOK o IDCANCEL. questi messaggi rappresentano una richiesta da parte dell'utente di chiudere la finestra di dialogo. La procedura deve chiudere la finestra di dialogo utilizzando la funzione [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) per le finestre di dialogo modali e la funzione [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) per le finestre di dialogo non modali.

Il sistema invia anche i messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) alla routine della finestra di dialogo se nella finestra di dialogo è presente un menu, ad esempio il menu **finestra** , e l'utente fa clic su una voce di menu. In particolare, il sistema invia un messaggio di **\_ comando WM** con il parametro *wParam* impostato su **IDCANCEL** ogni volta che l'utente fa clic su **Chiudi** nel menu finestra della finestra di dialogo. Il messaggio è quasi identico al messaggio di notifica inviato dal pulsante **Annulla** e deve essere elaborato esattamente allo stesso modo.

### <a name="the-wm_parentnotify-message"></a>Messaggio WM \_ PARENTNOTIFY

Un controllo Invia un messaggio [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) ogni volta che l'utente preme un pulsante del mouse puntando al controllo. Alcune applicazioni interpretano questo messaggio come un segnale per eseguire un'azione correlata al controllo, ad esempio la visualizzazione di una riga di testo che descrive lo scopo del controllo.

Il sistema invia anche messaggi [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) quando crea ed Elimina definitivamente una finestra, ma non per i controlli creati da un modello di finestra di dialogo. Il sistema impedisce questi messaggi specificando lo stile **WS \_ ex \_ NOPARENTNOTIFY** durante la creazione dei controlli. Un'applicazione non può eseguire l'override di questo comportamento predefinito a meno che non crei controlli personalizzati per la finestra di dialogo.

### <a name="control-color-messages"></a>Messaggi di Control-Color

I controlli e il sistema possono inviare messaggi con colore di controllo quando desiderano che la routine della finestra di dialogo disegni lo sfondo di un controllo o di un'altra finestra utilizzando un pennello e colori specifici. Questa operazione può essere utile quando le applicazioni eseguono l'override dei colori predefiniti utilizzati nelle finestre di dialogo e nei relativi controlli. Di seguito sono riportati i messaggi a colori del controllo, che hanno sostituito il messaggio **WM \_ CTLCOLOR** .

-   [**\_CTLCOLORBTN WM**](../controls/wm-ctlcolorbtn.md)
-   [**\_CTLCOLORDLG WM**](wm-ctlcolordlg.md)
-   [**\_CTLCOLOREDIT WM**](../controls/wm-ctlcoloredit.md)
-   [**\_CTLCOLORLISTBOX WM**](../controls/wm-ctlcolorlistbox.md)
-   [**\_CTLCOLORSCROLLBAR WM**](../controls/wm-ctlcolorscrollbar.md)
-   [**\_CTLCOLORSTATIC WM**](../controls/wm-ctlcolorstatic.md)

Un controllo Invia un messaggio di colore del controllo alla routine della finestra di dialogo immediatamente prima di disegnare il proprio sfondo. Il messaggio consente alla procedura di specificare il pennello da utilizzare e di impostare i colori di sfondo e di primo piano. La stored procedure specifica un pennello restituendo l'handle del pennello. Per impostare i colori di sfondo e di primo piano, la procedura usa le funzioni [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) e [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) con il contesto del dispositivo di visualizzazione del controllo. Il messaggio del colore di controllo passa un handle al contesto del dispositivo di visualizzazione alla procedura nel parametro *wParam* del messaggio.

Il sistema invia un messaggio [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md) alla routine della finestra di dialogo se la procedura non elabora il messaggio [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd) . La classe della finestra di dialogo predefinita non dispone di un pennello per lo sfondo della classe, pertanto questo messaggio consente alla routine di definire il proprio sfondo senza dover includere il codice per eseguire il lavoro.

In ogni caso, quando una routine della finestra di dialogo non elabora un messaggio di colore di controllo, il sistema utilizza un pennello con il colore predefinito della finestra per disegnare lo sfondo per tutti i controlli e le finestre eccetto le barre di scorrimento. Un'applicazione può recuperare il colore predefinito della finestra passando il valore della **\_ finestra dei colori** alla funzione [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) . Mentre lo sfondo viene disegnato, il colore di primo piano per il contesto del dispositivo di visualizzazione è impostato sul colore del testo predefinito (**colore \_ WINDOWTEXT**). Per le barre di scorrimento, il sistema utilizza un pennello con il colore della barra di scorrimento predefinito (barra di scorrimento dei **colori \_**). In questo caso, i colori di sfondo e di primo piano per il contesto del dispositivo di visualizzazione sono impostati rispettivamente su bianco e nero.

### <a name="dialog-box-default-message-processing"></a>Elaborazione dei messaggi predefiniti della finestra di dialogo

La routine della finestra per la classe della finestra di dialogo predefinita esegue l'elaborazione predefinita per tutti i messaggi che la routine della finestra di dialogo non elabora. Quando la routine della finestra di dialogo restituisce **false** per qualsiasi messaggio, la routine della finestra predefinita controlla i messaggi ed esegue le azioni predefinite seguenti:



| Message                                            | Azione predefinita                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_GETDEFID DM**](dm-getdefid.md)                | È possibile inviare questo messaggio a una finestra di dialogo. La finestra di dialogo restituisce l'identificatore del controllo del pulsante di push predefinito, se la finestra di dialogo ne contiene uno. in caso contrario, restituisce zero.                                                                                                                                                                                                                                                                                                                      |
| [**riposizionamento DM \_**](dm-reposition.md)            | È possibile inviare questo messaggio a una finestra di dialogo di primo livello. La finestra di dialogo viene riposizionata in modo da rientrare nell'area del desktop.                                                                                                                                                                                                                                                                                                                                                                       |
| [**\_SETDEFID DM**](dm-setdefid.md)                | È possibile inviare questo messaggio a una finestra di dialogo. La finestra di dialogo Imposta il pulsante di push predefinito sul controllo specificato dall'identificatore del controllo nel parametro *wParam* .                                                                                                                                                                                                                                                                                                                             |
| [**\_attivazione WM**](/windows/desktop/inputdev/wm-activate)           | Ripristina lo stato attivo per l'input del controllo identificato dall'handle salvato in precedenza se la finestra di dialogo è attivata. In caso contrario, la stored procedure Salva l'handle per il controllo con lo stato attivo per l'input.                                                                                                                                                                                                                                                                                               |
| [**\_CHARTOITEM WM**](../controls/wm-chartoitem.md)         | Restituisce zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_chiusura WM**](/windows/desktop/winmsg/wm-close)                   | Invia il messaggio di notifica [**\_ fatto clic su BN**](../controls/bn-clicked.md) alla finestra di dialogo, specificando **IDCANCEL** come identificatore del controllo. Se la finestra di dialogo contiene un identificatore di controllo IDCANCEL e il controllo è attualmente disabilitato, la procedura emette un avviso e non invia il messaggio.                                                                                                                                                                                              |
| [**\_COMPAREITEM WM**](../controls/wm-compareitem.md)       | Restituisce zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd)         | Riempie l'area client della finestra di dialogo utilizzando il pennello restituito dal messaggio [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md) o con il colore predefinito della finestra.                                                                                                                                                                                                                                                                                                                                 |
| [**\_tipo di carattere WM GetFont**](/windows/desktop/winmsg/wm-getfont)               | Restituisce un handle per il tipo di carattere della finestra di dialogo definito dall'applicazione.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**\_INITDIALOG WM**](wm-initdialog.md)            | Restituisce zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)     | Invia un [**messaggio \_ SHOWDROPDOWN CB**](../controls/cb-showdropdown.md) alla casella combinata con lo stato attivo per l'input, indirizzando il controllo per nascondere la relativa casella di riepilogo a discesa. La procedura chiama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per completare l'azione predefinita.                                                                                                                                                                                                                                      |
| [**\_NCDESTROY WM**](/windows/desktop/winmsg/wm-ncdestroy)           | Rilascia la memoria globale allocata per i controlli di modifica nella finestra di dialogo (si applica alle finestre di dialogo che specificano lo stile [**DS \_ LOCALEDIT**](dialog-box-styles.md) ) e libera qualsiasi tipo di carattere definito dall'applicazione (si applica alle finestre di dialogo che specificano lo stile DS [**\_ sefont**](dialog-box-styles.md) o [**DS \_ SHELLFONT**](dialog-box-styles.md) ). La procedura chiama la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per completare l'azione predefinita. |
| [**\_NCLBUTTONDOWN WM**](/windows/desktop/inputdev/wm-nclbuttondown) | Invia un [**messaggio \_ SHOWDROPDOWN CB**](../controls/cb-showdropdown.md) alla casella combinata con lo stato attivo per l'input, indirizzando il controllo per nascondere la relativa casella di riepilogo a discesa. La procedura chiama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per completare l'azione predefinita.                                                                                                                                                                                                                                      |
| [**\_NEXTDLGCTL WM**](wm-nextdlgctl.md)            | Imposta lo stato attivo per l'input sul controllo successivo o precedente nella finestra di dialogo, sul controllo identificato dall'handle nel parametro *wParam* oppure sul primo controllo nella finestra di dialogo visibile, non disabilitato e con lo stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . La procedura ignora questo messaggio se la finestra corrente con lo stato attivo per l'input non è un controllo.                                                                                                                  |
| [**\_stato attivo WM**](/windows/desktop/inputdev/wm-setfocus)           | Imposta lo stato attivo per l'input sul controllo identificato da un handle della finestra di controllo salvato in precedenza. Se non esiste alcun handle di questo tipo, la procedura imposta lo stato attivo per l'input sul primo controllo nel modello di finestra di dialogo visibile, non disabilitato e con lo stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . Se non esiste alcun controllo di questo tipo, la procedura imposta lo stato attivo per l'input sul primo controllo del modello.                                                                                          |
| [**\_ShowWindow WM**](/windows/desktop/winmsg/wm-showwindow)         | Salva un handle per il controllo con lo stato attivo per l'input se la finestra di dialogo viene nascosta, quindi chiama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per completare l'azione predefinita.                                                                                                                                                                                                                                                                                                                     |
| [**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)         | Salva un handle per il controllo con lo stato attivo per l'input se la finestra di dialogo viene ridotta a icona, quindi chiama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per completare l'azione predefinita.                                                                                                                                                                                                                                                                                                                  |
| [**\_VKEYTOITEM WM**](../controls/wm-vkeytoitem.md)         | Restituisce zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

La routine della finestra predefinita passa tutti gli altri messaggi a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per l'elaborazione predefinita.

## <a name="dialog-box-keyboard-interface"></a>Interfaccia della tastiera della finestra di dialogo

Il sistema fornisce un'interfaccia di tastiera speciale per le finestre di dialogo che esegue un'elaborazione speciale per diverse chiavi. L'interfaccia genera messaggi che corrispondono a determinati pulsanti nella finestra di dialogo o modifica lo stato attivo per l'input da un controllo a un altro. Di seguito sono riportate le chiavi usate in questa interfaccia e le rispettive azioni.


| Chiave            | Azione                                                                                                                                                                    |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALT +*tasto* di scelta | Sposta lo stato attivo per l'input sul primo controllo (con lo stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) ) dopo il controllo statico contenente il tasto di scelta specificato.        |
| DOWN           | Sposta lo stato attivo per l'input sul controllo successivo nel gruppo.                                                                                                                   |
| INVIO          | Invia un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) alla routine della finestra di dialogo. Il parametro *wParam* è impostato su IDOK o sull'identificatore del controllo del pulsante di push predefinito. |
| ESC            | Invia un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) alla routine della finestra di dialogo. Il parametro *wParam* è impostato su IDCANCEL.                                              |
| LEFT           | Sposta lo stato attivo per l'input sul controllo precedente nel gruppo.                                                                                                               |
| *mnemonico*     | Sposta lo stato attivo per l'input sul primo controllo (con lo stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) ) dopo il controllo statico contenente il tasto di scelta specificato.        |
| RIGHT          | Sposta lo stato attivo per l'input sul controllo successivo nel gruppo.                                                                                                                   |
| MAIUSC+TAB      | Sposta lo stato attivo per l'input sul controllo precedente con stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) .                                                                |
| TAB            | Sposta lo stato attivo per l'input sul controllo successivo con stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) .                                                                    |
| UP             | Sposta lo stato attivo per l'input sul controllo precedente nel gruppo.                                                                                                               |

Il sistema fornisce automaticamente l'interfaccia della tastiera per tutte le finestre di dialogo modali. Non fornisce l'interfaccia per le finestre di dialogo non modali, a meno che l'applicazione non chiami la funzione [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) per filtrare i messaggi nel relativo ciclo di messaggi principale. Ciò significa che l'applicazione deve passare il messaggio a **IsDialogMessage** subito dopo il recupero del messaggio dalla coda di messaggi. La funzione elabora i messaggi se è per la finestra di dialogo e restituisce un valore diverso da zero per indicare che il messaggio è stato elaborato e non deve essere passato alla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) o [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .

Poiché l'interfaccia della tastiera della finestra di dialogo USA i tasti di direzione per spostarsi tra i controlli in una finestra di dialogo, un'applicazione non può usare queste chiavi per scorrere il contenuto di una finestra di dialogo modale o di qualsiasi finestra di dialogo non modale per cui viene chiamato [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) . Quando una finestra di dialogo include barre di scorrimento, l'applicazione deve fornire un'interfaccia di tastiera alternativa per le barre di scorrimento. Si noti che l'interfaccia del mouse per lo scorrimento è disponibile quando il sistema include un mouse.

### <a name="the-ws_tabstop-style"></a>Stile di WS \_ TABSTOP

Lo stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) specifica i controlli che possono essere spostati dall'utente premendo TAB o MAIUSC + TAB.

Quando l'utente preme TAB o MAIUSC + TAB, il sistema determina innanzitutto se queste chiavi vengono elaborate dal controllo che ha attualmente lo stato attivo per l'input. Invia il controllo a un messaggio [**WM \_ GETDLGCODE**](wm-getdlgcode.md) e se il controllo restituisce DLGC \_ WANTTAB, il sistema passa le chiavi al controllo. In caso contrario, il sistema utilizza la funzione [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) per individuare il controllo successivo visibile, non disabilitato e con lo stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . La ricerca inizia con il controllo che ha attualmente lo stato attivo per l'input e procede nell'ordine in cui sono stati creati i controlli, ovvero l'ordine in cui sono definiti nel modello della finestra di dialogo. Quando il sistema individua un controllo con le caratteristiche richieste, il sistema sposta lo stato attivo per l'input.

Se la ricerca del controllo successivo con lo stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) rileva una finestra con lo stile **WS \_ ex \_ CONTROLPARENT** , il sistema esegue una ricerca ricorsiva negli elementi figlio della finestra.

Un'applicazione può anche usare [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) per individuare i controlli con lo stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . La funzione recupera l'handle della finestra del controllo successivo o precedente con lo stile **WS \_ TABSTOP** senza spostare lo stato attivo per l'input.

### <a name="the-ws_group-style"></a>Stile del \_ gruppo WS

Per impostazione predefinita, il sistema sposta lo stato attivo per l'input sul controllo successivo o precedente ogni volta che l'utente preme un tasto di direzione. Fino a quando il controllo corrente con lo stato attivo per l'input non elabora queste chiavi e il controllo successivo o precedente non è un controllo statico, il sistema continua a spostare lo stato attivo per l'input attraverso tutti i controlli della finestra di dialogo quando l'utente continua a premere i tasti di direzione.

Un'applicazione può utilizzare lo stile del [**\_ gruppo WS**](/windows/desktop/winmsg/window-styles) per modificare questo comportamento predefinito. Lo stile contrassegna l'inizio di un gruppo di controlli. Se un controllo del gruppo dispone dello stato attivo per l'input quando l'utente inizia a premere i tasti di direzione, lo stato attivo rimane nel gruppo. In generale, il primo controllo in un gruppo deve avere lo stile del **\_ gruppo WS** e tutti gli altri controlli nel gruppo non devono avere questo stile. Tutti i controlli del gruppo devono essere contigui, ovvero devono essere stati creati consecutivamente senza alcun controllo corrispondente.

Quando l'utente preme un tasto di direzione, il sistema determina innanzitutto se il controllo corrente con lo stato attivo per l'input elabora i tasti di direzione. Il sistema invia un messaggio [**WM \_ GETDLGCODE**](wm-getdlgcode.md) al controllo e se il controllo restituisce il valore **\_ WANTARROWS di DLGC** , passa la chiave al controllo. In caso contrario, il sistema utilizza la funzione [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) per determinare il controllo successivo nel gruppo.

[**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) Cerca i controlli nell'ordine (o nell'ordine inverso) in cui sono stati creati. Se l'utente preme il tasto destro o giù, **GetNextDlgGroupItem** restituisce il controllo successivo se il controllo non ha lo stile del [**\_ gruppo WS**](/windows/desktop/winmsg/window-styles) . In caso contrario, la funzione inverte l'ordine della ricerca e restituisce il primo controllo con lo stile **del \_ gruppo WS** . Se l'utente preme il tasto sinistro o alto, la funzione restituisce il controllo precedente, a meno che il controllo corrente non disponga già dello stile del **\_ gruppo WS** . Se il controllo corrente presenta questo stile, la funzione inverte l'ordine della ricerca, individua il primo controllo con lo stile del **\_ gruppo WS** e restituisce il controllo che precede immediatamente il controllo individuato.

Se la ricerca del controllo successivo nel gruppo rileva una finestra con lo stile **WS \_ ex \_ CONTROLPARENT** , il sistema cerca in modo ricorsivo gli elementi figlio della finestra.

Quando il sistema dispone del controllo successivo o precedente, invia un messaggio [**WM \_ GETDLGCODE**](wm-getdlgcode.md) al controllo per determinare il tipo di controllo. Il sistema sposta lo stato attivo per l'input in modo da controllare se non è un controllo statico. Se il controllo è un pulsante di opzione automatico, il sistema invia un messaggio di [**\_ clic BM**](../controls/bm-click.md) . Un'applicazione può anche usare [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) per individuare i controlli in un gruppo.

In genere, il primo controllo del gruppo combina gli stili [**WS \_ Group**](/windows/desktop/winmsg/window-styles) e [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) in modo che l'utente possa spostarsi da un gruppo a un gruppo utilizzando il tasto TAB. Se il gruppo contiene pulsanti di opzione, l'applicazione deve applicare lo stile **WS \_ TABSTOP** solo al primo controllo del gruppo. Il sistema sposta automaticamente lo stile quando l'utente si sposta tra i controlli del gruppo. In questo modo si garantisce che lo stato attivo per l'input sia sempre sul controllo selezionato più di recente quando l'utente passa al gruppo utilizzando il tasto TAB.

### <a name="mnemonics"></a>Tasti

Un tasto di scelta è una lettera o una cifra selezionata nell'etichetta di un pulsante o nel testo di un controllo statico. Il sistema sposta lo stato attivo per l'input sul controllo associato al tasto di scelta ogni volta che l'utente preme il tasto che corrisponde al tasto di scelta o preme questo tasto e il tasto ALT in combinazione. I tasti di scelta consentono all'utente di passare rapidamente a un controllo specificato utilizzando la tastiera.

Un'applicazione crea un tasto di scelta per un controllo inserendo la e commerciale (&) immediatamente prima della lettera o della cifra selezionata nell'etichetta o nel testo del controllo. Nella maggior parte dei casi, la stringa con terminazione null fornita con il controllo nel modello di finestra di dialogo contiene la e commerciale. Tuttavia, un'applicazione può creare un tasto di scelta in qualsiasi momento sostituendo l'etichetta o il testo esistente di un controllo tramite la funzione [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) . Per ogni controllo è possibile specificare solo un tasto di scelta. Sebbene sia consigliabile, i tasti di scelta in una finestra di dialogo non devono essere univoci.

Quando l'utente preme una lettera o un tasto numerico, il sistema determina innanzitutto se il controllo corrente con lo stato attivo per l'input elabora la chiave. Il sistema invia un messaggio [**WM \_ GETDLGCODE**](wm-getdlgcode.md) al controllo e, se il controllo restituisce il valore **DLGC \_ WANTALLKEYS** o **DLG \_ WANTMESSAGE** , il sistema passa la chiave al controllo. In caso contrario, Cerca un controllo il cui tasto di scelta corrisponde alla lettera o alla cifra specificata. Continua la ricerca fino a quando non individua un controllo o ha esaminato tutti i controlli. Durante la ricerca, ignora tutti i controlli statici con stile [**\_ NoPrefix SS**](../controls/static-control-styles.md) .

Se la ricerca di un controllo con un tasto di scelta corrispondente rileva una finestra con lo stile **WS \_ ex \_ CONTROLPARENT** , il sistema cerca in modo ricorsivo gli elementi figlio della finestra.

Se il sistema individua un controllo statico e il controllo non è disabilitato, il sistema sposta lo stato attivo per l'input sul primo controllo dopo che il controllo statico è visibile, non disabilitato e con lo stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . Se il sistema individua un altro controllo con un tasto di scelta corrispondente, sposta lo stato attivo per l'input su tale controllo. Se il controllo è un pulsante di push predefinito, il sistema invia un messaggio di notifica [**\_ fatto clic su BN**](../controls/bn-clicked.md) alla routine della finestra di dialogo. Se il controllo è un altro stile di pulsante e nessun altro controllo nella finestra di dialogo ha lo stesso tasto di scelta, il sistema invia il messaggio di [**\_ clic BM**](../controls/bm-click.md) al controllo.

## <a name="dialog-box-settings"></a>Impostazioni della finestra di dialogo

Le impostazioni della finestra di dialogo sono le selezioni correnti e i valori per i controlli nella finestra di dialogo. La procedura della finestra di dialogo è responsabile dell'inizializzazione dei controlli per queste impostazioni durante la creazione della finestra di dialogo. È inoltre responsabile del recupero delle impostazioni correnti dai controlli prima dell'eliminazione della finestra di dialogo. I metodi utilizzati per inizializzare e recuperare le impostazioni dipendono dal tipo di controllo.

Per altre informazioni, vedere i seguenti argomenti:

-   [Pulsanti di opzione e caselle di controllo](#radio-buttons-and-check-boxes)
-   [Controlli di modifica della finestra di dialogo](#dialog-box-edit-controls)
-   [Caselle di riepilogo, caselle combinate e elenchi di directory](#list-boxes-combo-boxes-and-directory-listings)
-   [Messaggi di controllo della finestra di dialogo](#dialog-box-control-messages)

### <a name="radio-buttons-and-check-boxes"></a>Pulsanti di opzione e caselle di controllo

Le finestre di dialogo utilizzano pulsanti di opzione e caselle di controllo per consentire all'utente di scegliere da un elenco di opzioni. I pulsanti di opzione consentono all'utente di scegliere tra opzioni che si escludono a vicenda. le caselle di controllo consentono all'utente di scegliere una combinazione di opzioni.

La routine della finestra di dialogo può impostare lo stato iniziale di una casella di controllo utilizzando la funzione [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx) , che consente di impostare o deselezionare la casella di controllo. Per i pulsanti di opzione in un gruppo di pulsanti di opzione che si escludono a vicenda, la routine della finestra di dialogo può utilizzare la funzione [**CheckRadioButton**](https://msdn.microsoft.com/library/Cc410654(v=MSDN.10).aspx) per impostare il pulsante di opzione appropriato e deselezionare automaticamente qualsiasi altro pulsante di opzione.

Prima che venga terminata una finestra di dialogo, la routine della finestra di dialogo può controllare lo stato di ogni pulsante di opzione e casella di controllo utilizzando la funzione [**IsDlgButtonChecked**](https://msdn.microsoft.com/library/Cc364806(v=MSDN.10).aspx) , che restituisce lo stato corrente del pulsante. In genere, una finestra di dialogo Salva queste informazioni per inizializzare i pulsanti alla successiva creazione della finestra di dialogo.

### <a name="dialog-box-edit-controls"></a>Controlli di modifica della finestra di dialogo

In molte finestre di dialogo sono presenti controlli di modifica che consentono all'utente di specificare testo come input. La maggior parte delle routine della finestra di dialogo Inizializza un controllo di modifica all'avvio della finestra di dialogo. Ad esempio, la routine della finestra di dialogo può inserire un nome file proposto nel controllo che l'utente può selezionare, modificare o sostituire. La routine della finestra di dialogo può impostare il testo in un controllo di modifica tramite la funzione [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) , che copia il testo da un buffer specificato al controllo di modifica. Quando il controllo di modifica riceve lo stato attivo per l'input, seleziona automaticamente il testo completo per la modifica.

Poiché i controlli di modifica non restituiscono automaticamente il testo alla finestra di dialogo, la routine della finestra di dialogo deve recuperare il testo prima di terminare. Può recuperare il testo usando la funzione [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) , che copia il testo del controllo di modifica in un buffer. La routine della finestra di dialogo Salva in genere il testo per inizializzare il controllo di modifica in un secondo momento o lo passa alla finestra padre per l'elaborazione.

Alcune finestre di dialogo utilizzano i controlli di modifica che consentono all'utente di immettere numeri. La routine della finestra di dialogo può recuperare un numero da un controllo di modifica usando la funzione [**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) , che recupera il testo dal controllo di modifica e lo converte in un valore decimale. L'utente digita il numero in cifre decimali. Può essere con segno o senza segno. La routine della finestra di dialogo può visualizzare un numero intero tramite la funzione [**SetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemint) . **SetDlgItemInt** converte un oggetto firmato o Unsigned Integer in una stringa di cifre decimali.

### <a name="list-boxes-combo-boxes-and-directory-listings"></a>Caselle di riepilogo, caselle combinate e elenchi di directory

In alcune finestre di dialogo vengono visualizzati elenchi di nomi da cui l'utente può selezionare uno o più nomi. Per visualizzare un elenco di nomi di file, ad esempio, in una finestra di dialogo vengono in genere utilizzate una casella di riepilogo e le funzioni [**DlgDirList**](https://msdn.microsoft.com/library/Cc410788(v=MSDN.10).aspx) e [**DlgDirSelectEx**](https://msdn.microsoft.com/library/Cc410769(v=MSDN.10).aspx) . La funzione **DlgDirList** riempie automaticamente una casella di riepilogo con i nomi dei file nella directory corrente. La funzione **DlgDirSelect** Recupera il nome file selezionato dalla casella di riepilogo. Insieme, queste due funzioni consentono a una finestra di dialogo di visualizzare un elenco di directory, in modo che l'utente possa selezionare un file senza che sia necessario digitarne il nome e il percorso.

Una finestra di dialogo può inoltre utilizzare una casella combinata per visualizzare un elenco di nomi file. La funzione [**DlgDirListComboBox**](https://msdn.microsoft.com/library/Cc410798(v=MSDN.10).aspx) riempie automaticamente una parte di casella di riepilogo della casella combinata con i nomi di file nella directory corrente. La funzione [**DlgDirSelectComboBoxEx**](https://msdn.microsoft.com/library/Cc410768(v=MSDN.10).aspx) recupera un nome di file selezionato dalla parte della casella di riepilogo.

### <a name="dialog-box-control-messages"></a>Messaggi di controllo della finestra di dialogo

Molti controlli riconoscono i messaggi predefiniti che, quando ricevuti dai controlli, causano l'esecuzione di un'azione. Ad esempio, il [**messaggio \_ di controllo BM**](../controls/bm-setcheck.md) imposta il segno di spunta in una casella di controllo e il messaggio [**\_ GETSEL em**](../controls/em-getsel.md) recupera la parte del testo del controllo attualmente selezionato. I messaggi di controllo consentono a una routine di dialogo di accedere in modo più flessibile ai controlli rispetto alle funzioni standard, quindi vengono spesso utilizzati quando la finestra di dialogo richiede interazioni complesse con l'utente.

Una routine della finestra di dialogo può inviare un messaggio a un controllo fornendo l'identificatore del controllo e utilizzando la funzione [**SendDlgItemMessage**](/windows/desktop/api/Winuser/nf-winuser-senddlgitemmessagea) , che è identica alla funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , ad eccezione del fatto che usa un identificatore di controllo anziché un handle di finestra per identificare il controllo che riceverà il messaggio. Un messaggio specificato potrebbe richiedere che la routine della finestra di dialogo invii parametri con il messaggio e che il messaggio contenga valori restituiti corrispondenti. L'operazione e i requisiti di ogni messaggio di controllo dipendono dallo scopo del messaggio e dal controllo che lo elabora.

Per ulteriori informazioni sui messaggi di controllo, vedere [controlli Windows](../controls/window-controls.md).

## <a name="custom-dialog-boxes"></a>Finestre di dialogo personalizzate

Un'applicazione può creare finestre di dialogo personalizzate utilizzando una classe di finestra definita dall'applicazione per le finestre di dialogo anziché utilizzare la classe della finestra di dialogo predefinita. Le applicazioni in genere usano questo metodo quando una finestra di dialogo è la finestra principale, ma è utile anche per creare finestre di dialogo modali e non modali per le applicazioni con finestre sovrapposte standard.

La classe della finestra definita dall'applicazione consente all'applicazione di definire una procedura di finestra per la finestra di dialogo ed elaborare i messaggi prima di inviarli alla routine della finestra di dialogo. Consente inoltre all'applicazione di definire un'icona di classe, un pennello per lo sfondo della classe e un menu di classe per la finestra di dialogo. L'applicazione deve registrare la classe della finestra prima di provare a creare una finestra di dialogo e deve fornire il modello di finestra di dialogo con il valore Atom o il nome della classe di finestra.

Molte applicazioni creano una nuova classe di finestre di dialogo recuperando prima le informazioni sulla classe per la classe della finestra di dialogo predefinita e passandola alla funzione [**GetClassInfo**](/windows/desktop/api/winuser/nf-winuser-getclassinfoa) , che compila una struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) con le informazioni. L'applicazione modifica i singoli membri della struttura, ad esempio il nome della classe, il pennello e l'icona, quindi registra la nuova classe tramite la funzione [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) . Se un'applicazione compila autonomamente la struttura **WNDCLASS** , deve impostare il membro **cbWndExtra** su **DLGWINDOWEXTRA**, ovvero il numero di byte aggiuntivi richiesti dal sistema per ogni finestra di dialogo. Se un'applicazione usa anche byte aggiuntivi per ogni finestra di dialogo, questi devono essere oltre i byte aggiuntivi richiesti dal sistema.

La procedura della finestra per la finestra di dialogo personalizzata presenta gli stessi parametri e requisiti di qualsiasi altra routine della finestra. Diversamente da altre routine della finestra, tuttavia, la routine della finestra per questa finestra di dialogo deve chiamare la funzione [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) anziché la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per tutti i messaggi non elaborati. **DefDlgProc** esegue la stessa elaborazione predefinita del messaggio come procedura della finestra di dialogo predefinita, che include la chiamata della routine della finestra di dialogo.

Un'applicazione può inoltre creare finestre di dialogo personalizzate mediante la creazione di una sottoclasse della routine della finestra di dialogo predefinita. La funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) consente a un'applicazione di specificare la routine della finestra per una finestra specificata. L'applicazione può anche tentare di eseguire una sottoclasse usando la funzione [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) , ma questa operazione influisca su tutte le finestre di dialogo del sistema, non solo quelle che appartengono all'applicazione.

Le applicazioni che creano finestre di dialogo personalizzate talvolta forniscono un'interfaccia di tastiera alternativa per le finestre di dialogo. Per le finestre di dialogo non modali, questo può significare che l'applicazione non chiama la funzione [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) e elabora invece tutti gli input da tastiera nella routine della finestra personalizzata. In questi casi, l'applicazione può usare il messaggio [**WM \_ NEXTDLGCTL**](wm-nextdlgctl.md) per ridurre al minimo il codice necessario per spostare lo stato attivo di input da un controllo a un altro. Questo messaggio, quando viene passato a [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw), sposta lo stato attivo per l'input su un controllo specificato e aggiorna l'aspetto dei controlli, ad esempio spostando il bordo predefinito del pulsante di push o impostando un pulsante di opzione automatico.
