---
title: Considerazioni sulla programmazione delle finestre di dialogo
description: Questa panoramica illustra alcune considerazioni sulla programmazione relative alle finestre di dialogo.
ms.assetid: 49024a0f-ea92-4d56-b063-8e5fcdbd884a
keywords:
- Windows Interfaccia utente,windowing
- Windows Interfaccia utente,finestre di dialogo
- windowing,finestre di dialogo
- finestre di dialogo, informazioni
- procedure della finestra di dialogo
- finestre di dialogo, procedure
- WM_INITDIALOG messaggio
- WM_COMMAND messaggio
- WM_PARENTNOTIFY messaggio
- messaggi control-color
- finestre di dialogo, elaborazione di messaggi
- finestre di dialogo, interfaccia della tastiera
- finestre di dialogo, mnemoiche
- finestre di dialogo, personalizzate
- finestre di dialogo personalizzate
- finestre di dialogo,impostazioni
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 956f700841b0a3d76b7e071f0232382507394879a0253bc4cbcea533fdbb23bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456251"
---
# <a name="dialog-box-programming-considerations"></a>Considerazioni sulla programmazione delle finestre di dialogo

Questa panoramica illustra alcune considerazioni sulla programmazione relative alle finestre di dialogo.

La panoramica include gli argomenti seguenti.

-   [Procedure della finestra di dialogo](#dialog-box-procedures)
    -   [Messaggio WM \_ INITDIALOG](wm-initdialog.md)
    -   [Messaggio WM \_ COMMAND](/windows/desktop/menurc/wm-command)
    -   [Messaggio WM \_ PARENTNOTIFY](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)
    -   [Messaggi control-color](#control-color-messages)
    -   [Elaborazione dei messaggi predefinita della finestra di dialogo](#dialog-box-default-message-processing)
-   [Interfaccia della tastiera della finestra di dialogo](#dialog-box-keyboard-interface)
    -   [Stile WS \_ TABSTOP](/windows/desktop/winmsg/window-styles)
    -   [Stile gruppo \_ WS](/windows/desktop/winmsg/window-styles)
    -   [Mnemonics](#mnemonics)
-   [Finestra di dialogo Impostazioni](#dialog-box-settings)
    -   [Pulsanti di opzione e caselle di controllo](#radio-buttons-and-check-boxes)
    -   [Controlli di modifica della finestra di dialogo](#dialog-box-edit-controls)
    -   [Caselle di riepilogo, caselle combinate ed elenchi di directory](#list-boxes-combo-boxes-and-directory-listings)
    -   [Messaggi di controllo della finestra di dialogo](#dialog-box-control-messages)
-   [Finestre di dialogo personalizzate](#custom-dialog-boxes)

## <a name="dialog-box-procedures"></a>Procedure della finestra di dialogo

Una routine della finestra di dialogo è simile a una routine finestra in quanto il sistema invia messaggi alla procedura quando dispone di informazioni da assegnare o attività da eseguire. A differenza di una routine finestra, una routine della finestra di dialogo non chiama mai la [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Restituisce invece **TRUE se** elabora un messaggio o **FALSE** in caso contrario.

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

I parametri della routine hanno lo stesso scopo di una routine della finestra, con il parametro *hwndDlg* che riceve l'handle di finestra della finestra di dialogo.

La maggior parte delle procedure della finestra di dialogo elabora il messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) e i [**messaggi WM \_ COMMAND**](/windows/desktop/menurc/wm-command) inviati dai controlli, ma elabora pochi eventuali altri messaggi. Se una routine della finestra di dialogo non elabora un messaggio, deve restituire **FALSE** per indirizzare il sistema a elaborare i messaggi internamente. L'unica eccezione a questa regola è il **messaggio WM \_ INITDIALOG.** La routine della finestra di dialogo deve restituire **TRUE** per indirizzare il sistema all'ulteriore elaborazione **del messaggio WM \_ INITDIALOG.** In ogni caso, la routine non deve chiamare [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

- [Messaggio WM \_ INITDIALOG](#the-wm_initdialog-message)
- [Messaggio WM \_ COMMAND](#the-wm_command-message)
- [Messaggio WM \_ PARENTNOTIFY](#the-wm_parentnotify-message)
- [Messaggi control-color](#control-color-messages)
- [Elaborazione dei messaggi predefinita della finestra di dialogo](#dialog-box-default-message-processing)

### <a name="the-wm_initdialog-message"></a>Messaggio WM \_ INITDIALOG

Il sistema non invia un messaggio [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) alla procedura della finestra di dialogo. Invia invece un messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) quando crea la finestra di dialogo e tutti i relativi controlli, ma prima di visualizzare la finestra di dialogo. La procedura deve eseguire qualsiasi inizializzazione necessaria per garantire che nella finestra di dialogo siano visualizzate le impostazioni correnti associate all'attività. Ad esempio, quando una finestra di dialogo contiene un controllo per visualizzare l'unità e la directory correnti, la procedura deve determinare l'unità e la directory correnti e impostare il controllo su tale valore.

La routine può inizializzare i controlli usando funzioni come [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) e [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx). Poiché i controlli sono finestre, la procedura può anche modificarli usando funzioni di gestione delle finestre, ad esempio [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) [**e SetFocus.**](/windows/desktop/api/winuser/nf-winuser-setfocus) La routine può recuperare l'handle di finestra per un controllo usando la [**funzione GetDlgItem.**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem)

La procedura della finestra di dialogo può modificare il contenuto, lo stato e la posizione di qualsiasi controllo in base alle esigenze. Ad esempio, in una finestra di dialogo contenente  una casella di riepilogo  dei nomi di file e un pulsante Apri, la procedura può disabilitare il pulsante Apri fino a quando l'utente non seleziona un file dall'elenco. In questo esempio, il modello di finestra di  dialogo specifica lo stile [**WS \_ DISABLED**](/windows/desktop/winmsg/window-styles) per il pulsante Apri e il sistema disabilita automaticamente il pulsante durante la creazione. Quando la routine della finestra di dialogo riceve un messaggio di notifica dalla casella di riepilogo che indica che l'utente ha selezionato un file, la procedura chiama la funzione [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) per abilitare il **pulsante** Apri.

Per visualizzare un'icona personalizzata sulla barra del titolo della finestra di dialogo, il gestore [**WM \_ INITDIALOG**](wm-initdialog.md) può inviare il messaggio [**WM \_ SETICON**](/windows/desktop/winmsg/wm-seticon) alla finestra di dialogo.

Se l'applicazione crea la finestra di dialogo usando una delle funzioni [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)o [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), il *parametro lParam* per il messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) contiene il parametro aggiuntivo passato alla funzione. Le applicazioni usano in genere questo parametro aggiuntivo per passare un puntatore a informazioni di inizializzazione aggiuntive alla routine della finestra di dialogo, ma la routine della finestra di dialogo deve determinare il significato del parametro. Se l'applicazione usa un'altra funzione per creare la finestra di dialogo, il sistema imposta il *parametro lParam* su **NULL.**

Prima di restituire il messaggio [**WM \_ INITDIALOG,**](wm-initdialog.md) la procedura deve determinare se deve impostare lo stato attivo per l'input su un controllo specificato. Se la routine della finestra di dialogo restituisce **TRUE,** il sistema imposta automaticamente lo stato attivo per l'input sul controllo il cui handle di finestra si trova nel *parametro wParam.* Se il controllo che riceve lo stato attivo predefinito non è appropriato, può impostare lo stato attivo sul controllo appropriato usando la [**funzione SetFocus.**](/windows/desktop/api/winuser/nf-winuser-setfocus) Se la routine imposta lo stato attivo per l'input, deve restituire **FALSE** per impedire al sistema di impostare lo stato attivo predefinito. Il controllo che riceve lo stato attivo per l'input predefinito è sempre il primo controllo specificato nel modello visibile, non disabilitato e con lo [stile \_ WS TABSTOP.](/windows/desktop/winmsg/window-styles) Se tale controllo non esiste, il sistema imposta lo stato attivo per l'input predefinito sul primo controllo nel modello.

### <a name="the-wm_command-message"></a>Messaggio WM \_ COMMAND

Un controllo può inviare [**un messaggio WM \_ COMMAND**](/windows/desktop/menurc/wm-command) alla routine della finestra di dialogo quando l'utente esegue un'azione nel controllo. Questi messaggi, detti messaggi di notifica, informano la procedura di input dell'utente e consentono di eseguire le risposte appropriate.

Tutti i controlli predefiniti, ad eccezione dei controlli statici, inviano messaggi di notifica per le azioni utente selezionate. Ad esempio, un pulsante push invia il [**messaggio di notifica BN \_ CLICKED**](../controls/bn-clicked.md) ogni volta che l'utente fa clic sul pulsante. In tutti i casi, la parola di ordine basso del parametro *wParam* contiene l'identificatore di controllo, la parola di ordine superiore *di wParam* contiene il codice di notifica e il *parametro lParam* contiene l'handle della finestra di controllo.

La procedura della finestra di dialogo deve monitorare ed elaborare i messaggi di notifica. In particolare, la procedura deve elaborare i messaggi con gli identificatori IDOK o IDCANCEL. questi messaggi rappresentano una richiesta dell'utente di chiudere la finestra di dialogo. La routine deve chiudere la finestra di dialogo usando la [**funzione EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) per le finestre di dialogo modali e [**la funzione DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) per le finestre di dialogo non modali.

Il sistema invia anche messaggi [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) alla routine della finestra di dialogo se nella finestra di dialogo è disponibile un menu, ad esempio il **menu** della finestra, e l'utente fa clic su una voce di menu. In particolare, il sistema invia un messaggio **WM \_ COMMAND** con il parametro  *wParam* impostato su **IDCANCEL** ogni volta che l'utente fa clic su Chiudi nel menu della finestra di dialogo. Il messaggio è quasi identico al messaggio di notifica inviato dal pulsante **Annulla** e deve essere elaborato esattamente nello stesso modo.

### <a name="the-wm_parentnotify-message"></a>Messaggio WM \_ PARENTNOTIFY

Un controllo invia un [**messaggio WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) ogni volta che l'utente preme un pulsante del mouse mentre punta al controllo. Alcune applicazioni interpretano questo messaggio come un segnale per eseguire un'azione correlata al controllo, ad esempio la visualizzazione di una riga di testo che descrive lo scopo del controllo.

Il sistema invia anche [**messaggi WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) quando crea ed elimina una finestra, ma non per i controlli creati da un modello di finestra di dialogo. Il sistema impedisce questi messaggi specificando lo **stile WS \_ EX \_ NOPARENTNOTIFY** durante la creazione dei controlli. Un'applicazione non può eseguire l'override di questo comportamento predefinito a meno che non crei i propri controlli per la finestra di dialogo.

### <a name="control-color-messages"></a>Control-Color messaggi

I controlli e il sistema possono inviare messaggi di colore di controllo quando vogliono che la procedura della finestra di dialogo dipinga lo sfondo di un controllo o di un'altra finestra usando un pennello e colori specifici. Ciò può essere utile quando le applicazioni eseguono l'override dei colori predefiniti usati nelle finestre di dialogo e nei relativi controlli. Di seguito sono riportati i messaggi control-color, che hanno sostituito il **messaggio WM \_ CTLCOLOR.**

-   [**WM \_ CTLCOLORBTN**](../controls/wm-ctlcolorbtn.md)
-   [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md)
-   [**WM \_ CTLCOLOREDIT**](../controls/wm-ctlcoloredit.md)
-   [**WM \_ CTLCOLORLISTBOX**](../controls/wm-ctlcolorlistbox.md)
-   [**WM \_ CTLCOLORSCROLLBAR**](../controls/wm-ctlcolorscrollbar.md)
-   [**WM \_ CTLCOLORSTATIC**](../controls/wm-ctlcolorstatic.md)

Un controllo invia un messaggio di colore di controllo alla routine della finestra di dialogo subito prima di disegnare il proprio sfondo. Il messaggio consente alla procedura di specificare il pennello da usare e di impostare i colori di sfondo e primo piano. La routine specifica un pennello mediante la restituzione dell'handle del pennello. Per impostare i colori di sfondo e primo piano, la procedura usa le funzioni [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) e [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) con il contesto di dispositivo di visualizzazione del controllo. Il messaggio di colore del controllo passa un handle al contesto di dispositivo di visualizzazione alla procedura nel parametro *wParam del* messaggio.

Il sistema invia un [**messaggio WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md) alla routine della finestra di dialogo se la procedura non elabora il [**messaggio WM \_ ERASEBKGND.**](/windows/desktop/winmsg/wm-erasebkgnd) La classe predefinita della finestra di dialogo non dispone di un pennello di sfondo della classe, quindi questo messaggio consente alla procedura di definire il proprio sfondo senza dover includere il codice per eseguire il lavoro.

In ogni caso, quando una routine della finestra di dialogo non elabora un messaggio di colore di controllo, il sistema usa un pennello con il colore predefinito della finestra per disegnare lo sfondo per tutti i controlli e le finestre ad eccezione delle barre di scorrimento. Un'applicazione può recuperare il colore predefinito della finestra passando il **valore COLOR \_ WINDOW** alla [**funzione GetSysColor.**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) Durante il disegno dello sfondo, il colore di primo piano per il contesto di periferica di visualizzazione viene impostato sul colore del testo predefinito (**COLOR \_ WINDOWTEXT**). Per le barre di scorrimento, il sistema usa un pennello con il colore predefinito della barra di scorrimento (**COLOR \_ SCROLLBAR**). In questo caso, i colori di sfondo e primo piano per il contesto di dispositivo di visualizzazione sono impostati rispettivamente su bianco e nero.

### <a name="dialog-box-default-message-processing"></a>Elaborazione dei messaggi predefinita della finestra di dialogo

La routine della finestra per la classe predefinita della finestra di dialogo esegue l'elaborazione predefinita per tutti i messaggi che la routine della finestra di dialogo non elabora. Quando la routine della finestra di dialogo restituisce **FALSE** per qualsiasi messaggio, la routine della finestra predefinita controlla i messaggi ed esegue le azioni predefinite seguenti:



| Message                                            | Azione predefinita                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DM \_ GETDEFID**](dm-getdefid.md)                | È possibile inviare questo messaggio a una finestra di dialogo. La finestra di dialogo restituisce l'identificatore del controllo del pulsante di comando predefinito, se la finestra di dialogo ne ha uno; In caso contrario, restituisce zero.                                                                                                                                                                                                                                                                                                                      |
| [**\_RIPOSIZIONAMENTO DM**](dm-reposition.md)            | È possibile inviare questo messaggio a una finestra di dialogo di primo livello. La finestra di dialogo viene riposizionata in modo che si adatti all'area del desktop.                                                                                                                                                                                                                                                                                                                                                                       |
| [**DM \_ SETDEFID**](dm-setdefid.md)                | È possibile inviare questo messaggio a una finestra di dialogo. La finestra di dialogo imposta il pulsante di comando predefinito sul controllo specificato dall'identificatore di controllo nel *parametro wParam.*                                                                                                                                                                                                                                                                                                                             |
| [**WM \_ ACTIVATE**](/windows/desktop/inputdev/wm-activate)           | Ripristina lo stato attivo per l'input sul controllo identificato dall'handle salvato in precedenza se la finestra di dialogo è attivata. In caso contrario, la routine salva l'handle nel controllo con lo stato attivo per l'input.                                                                                                                                                                                                                                                                                               |
| [**WM \_ CHARTOITEM**](../controls/wm-chartoitem.md)         | Restituisce zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close)                   | Invia il [**messaggio di notifica \_ BN CLICKED**](../controls/bn-clicked.md) nella finestra di dialogo, specificando **IDCANCEL** come identificatore del controllo. Se la finestra di dialogo ha un identificatore di controllo IDCANCEL e il controllo è attualmente disabilitato, la procedura esecuzione di un avviso e non pubblica il messaggio.                                                                                                                                                                                              |
| [**WM \_ COMPAREITEM**](../controls/wm-compareitem.md)       | Restituisce zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)         | Riempie l'area client della finestra di dialogo usando il pennello restituito dal messaggio [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md) o con il colore predefinito della finestra.                                                                                                                                                                                                                                                                                                                                 |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Restituisce un handle per il tipo di carattere della finestra di dialogo definito dall'applicazione.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ INITDIALOG**](wm-initdialog.md)            | Restituisce zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | Invia un [**messaggio CB \_ SHOWDROPDOWN**](../controls/cb-showdropdown.md) alla casella combinata con lo stato attivo per l'input, indicando al controllo di nascondere la casella di riepilogo a discesa. La procedura chiama [**DefWindowProc per**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) completare l'azione predefinita.                                                                                                                                                                                                                                      |
| [**WM \_ NCDESTROY**](/windows/desktop/winmsg/wm-ncdestroy)           | Rilascia la memoria globale allocata per i controlli di modifica nella finestra di dialogo (si applica alle finestre di dialogo che specificano lo stile [**\_ DS LOCALEDIT)**](dialog-box-styles.md) e libera qualsiasi tipo di carattere definito dall'applicazione (si applica alle finestre di dialogo che specificano lo stile [**\_ DS SETFONT**](dialog-box-styles.md) o [**DS \_ SHELLFONT).**](dialog-box-styles.md) La procedura chiama la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per completare l'azione predefinita. |
| [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) | Invia un [**messaggio CB \_ SHOWDROPDOWN**](../controls/cb-showdropdown.md) alla casella combinata con lo stato attivo per l'input, indicando al controllo di nascondere la casella di riepilogo a discesa. La procedura chiama [**DefWindowProc per**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) completare l'azione predefinita.                                                                                                                                                                                                                                      |
| [**WM \_ NEXTDLGCTL**](wm-nextdlgctl.md)            | Imposta lo stato attivo per l'input sul controllo successivo o precedente nella finestra di dialogo, sul controllo identificato dall'handle nel parametro *wParam* o sul primo controllo nella finestra di dialogo visibile, non disabilitato e con lo stile [**WS \_ TABSTOP.**](/windows/desktop/winmsg/window-styles) La procedura ignora questo messaggio se la finestra corrente con lo stato attivo per l'input non è un controllo .                                                                                                                  |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)           | Imposta lo stato attivo per l'input sul controllo identificato da un punto di controllo della finestra di controllo salvato in precedenza. Se tale handle non esiste, la procedura imposta lo stato attivo per l'input sul primo controllo nel modello di finestra di dialogo visibile, non disabilitato e con lo stile [**WS \_ TABSTOP.**](/windows/desktop/winmsg/window-styles) Se tale controllo non esiste, la procedura imposta lo stato attivo per l'input sul primo controllo nel modello.                                                                                          |
| [**WM \_ SHOWWINDOW**](/windows/desktop/winmsg/wm-showwindow)         | Salva un handle per il controllo con lo stato attivo per l'input se la finestra di dialogo è nascosta, quindi chiama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per completare l'azione predefinita.                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)         | Salva un handle per il controllo con lo stato attivo per l'input se la finestra di dialogo viene ridotta a icona, quindi chiama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per completare l'azione predefinita.                                                                                                                                                                                                                                                                                                                  |
| [**WM \_ VKEYTOITEM**](../controls/wm-vkeytoitem.md)         | Restituisce zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

La routine di finestra predefinita passa tutti gli altri messaggi a [**DefWindowProc per**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) l'elaborazione predefinita.

## <a name="dialog-box-keyboard-interface"></a>Interfaccia della tastiera della finestra di dialogo

Il sistema fornisce un'interfaccia della tastiera speciale per le finestre di dialogo che esegue un'elaborazione speciale per diversi tasti. L'interfaccia genera messaggi che corrispondono a determinati pulsanti nella finestra di dialogo o modifica lo stato attivo per l'input da un controllo a un altro. Di seguito sono riportate le chiavi usate in questa interfaccia e le rispettive azioni.


| Chiave            | Azione                                                                                                                                                                    |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALT+*tasto di scelta rapida* | Sposta lo stato attivo per l'input sul primo controllo (con lo stile [**WS \_ TABSTOP)**](/windows/desktop/winmsg/window-styles) dopo il controllo statico contenente il mnemono specificato.        |
| DOWN           | Sposta lo stato attivo per l'input sul controllo successivo nel gruppo.                                                                                                                   |
| INVIO          | Invia un [**messaggio WM \_ COMMAND**](/windows/desktop/menurc/wm-command) alla routine della finestra di dialogo. Il *parametro wParam* è impostato su IDOK o sull'identificatore di controllo del pulsante di comando predefinito. |
| ESC            | Invia un [**messaggio WM \_ COMMAND**](/windows/desktop/menurc/wm-command) alla routine della finestra di dialogo. Il *parametro wParam* è impostato su IDCANCEL.                                              |
| LEFT           | Sposta lo stato attivo per l'input sul controllo precedente nel gruppo.                                                                                                               |
| *Mnemonico*     | Sposta lo stato attivo per l'input sul primo controllo (con lo stile [**WS \_ TABSTOP)**](/windows/desktop/winmsg/window-styles) dopo il controllo statico contenente il mnemono specificato.        |
| RIGHT          | Sposta lo stato attivo per l'input sul controllo successivo nel gruppo.                                                                                                                   |
| MAIUSC+TAB      | Sposta lo stato attivo per l'input sul controllo precedente con [**lo stile WS \_ TABSTOP.**](/windows/desktop/winmsg/window-styles)                                                                |
| TAB            | Sposta lo stato attivo per l'input sul controllo successivo con [**lo stile WS \_ TABSTOP.**](/windows/desktop/winmsg/window-styles)                                                                    |
| UP             | Sposta lo stato attivo per l'input sul controllo precedente nel gruppo.                                                                                                               |

Il sistema fornisce automaticamente l'interfaccia della tastiera per tutte le finestre di dialogo modali. Non fornisce l'interfaccia per le finestre di dialogo non modali, a meno che l'applicazione non chiami la [**funzione IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) per filtrare i messaggi nel ciclo di messaggi principale. Ciò significa che l'applicazione deve passare il messaggio a **IsDialogMessage** immediatamente dopo il recupero del messaggio dalla coda di messaggi. La funzione elabora i messaggi se è per la finestra di dialogo e restituisce un valore diverso da zero per indicare che il messaggio è stato elaborato e non deve essere passato alla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) o [**DispatchMessage.**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)

Poiché l'interfaccia della tastiera della finestra di dialogo usa i tasti di direzione per spostarsi tra i controlli di una finestra di dialogo, un'applicazione non può usare questi tasti per scorrere il contenuto di una finestra di dialogo modale o di una finestra di dialogo non modale per cui viene chiamato [**IsDialogMessage.**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) Quando in una finestra di dialogo sono disponibili barre di scorrimento, l'applicazione deve fornire un'interfaccia della tastiera alternativa per le barre di scorrimento. Si noti che l'interfaccia del mouse per lo scorrimento è disponibile quando il sistema include un mouse.

### <a name="the-ws_tabstop-style"></a>Stile WS \_ TABSTOP

Lo [**stile WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) specifica i controlli su cui l'utente può spostarsi premendo TAB o MAIUSC+TAB.

Quando l'utente preme TAB o MAIUSC+TAB, il sistema determina innanzitutto se questi tasti vengono elaborati dal controllo che attualmente ha lo stato attivo per l'input. Invia al controllo un messaggio [**WM \_ GETDLGCODE**](wm-getdlgcode.md) e, se il controllo restituisce DLGC WANTTAB, il sistema passa \_ i tasti al controllo. In caso contrario, il sistema usa la funzione [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) per individuare il controllo successivo visibile, non disabilitato e con lo [**stile WS \_ TABSTOP.**](/windows/desktop/winmsg/window-styles) La ricerca inizia con il controllo che attualmente ha lo stato attivo per l'input e procede nell'ordine in cui sono stati creati i controlli, ovvero l'ordine in cui sono definiti nel modello di finestra di dialogo. Quando il sistema individua un controllo con le caratteristiche necessarie, sposta lo stato attivo per l'input su di esso.

Se la ricerca del controllo successivo con lo stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) rileva una finestra con lo stile **WS \_ EX \_ CONTROLPARENT,** il sistema cerca in modo ricorsivo gli elementi figlio della finestra.

Un'applicazione può anche usare [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) per individuare i controlli con [**lo stile \_ WS TABSTOP.**](/windows/desktop/winmsg/window-styles) La funzione recupera l'handle della finestra del controllo successivo o precedente con lo stile **WS \_ TABSTOP** senza spostare lo stato attivo per l'input.

### <a name="the-ws_group-style"></a>Stile WS \_ GROUP

Per impostazione predefinita, il sistema sposta lo stato attivo per l'input sul controllo successivo o precedente ogni volta che l'utente preme un tasto di direzione. Se il controllo corrente con lo stato attivo per l'input non elabora questi tasti e il controllo successivo o precedente non è un controllo statico, il sistema continua a spostare lo stato attivo per l'input in tutti i controlli nella finestra di dialogo mentre l'utente continua a premere i tasti di direzione.

Un'applicazione può utilizzare [**lo stile WS \_ GROUP**](/windows/desktop/winmsg/window-styles) per modificare questo comportamento predefinito. Lo stile contrassegna l'inizio di un gruppo di controlli. Se un controllo nel gruppo ha lo stato attivo per l'input quando l'utente inizia a premere i tasti di direzione, lo stato attivo rimane nel gruppo. In generale, il primo controllo di un gruppo deve avere lo stile **WS \_ GROUP** e tutti gli altri controlli nel gruppo non devono avere questo stile. Tutti i controlli nel gruppo devono essere contigui, ovvero devono essere stati creati consecutivamente senza alcun controllo.

Quando l'utente preme un tasto di direzione, il sistema determina innanzitutto se il controllo corrente con lo stato attivo per l'input elabora i tasti di direzione. Il sistema invia un messaggio [**WM \_ GETDLGCODE**](wm-getdlgcode.md) al controllo e, se il controllo restituisce il valore **DLGC \_ WANTARROWS,** passa il tasto al controllo. In caso contrario, il sistema [**usa la funzione GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) per determinare il controllo successivo nel gruppo.

[**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) cerca i controlli nell'ordine (o in ordine inverso) in cui sono stati creati. Se l'utente preme il tasto RIGHT o DOWN, **GetNextDlgGroupItem** restituisce il controllo successivo se tale controllo non ha lo [**stile WS \_ GROUP.**](/windows/desktop/winmsg/window-styles) In caso contrario, la funzione inverte l'ordine della ricerca e restituisce il primo controllo con lo **stile WS \_ GROUP.** Se l'utente preme il tasto LEFT o UP, la funzione restituisce il controllo precedente, a meno che il controllo corrente non abbia già lo **stile WS \_ GROUP.** Se il controllo corrente ha questo stile, la funzione inverte l'ordine della ricerca, individua il primo controllo con lo stile **WS \_ GROUP** e restituisce il controllo che precede immediatamente il controllo individuato.

Se la ricerca del controllo successivo nel gruppo rileva una finestra con lo stile **WS \_ EX \_ CONTROLPARENT,** il sistema cerca in modo ricorsivo gli elementi figlio della finestra.

Quando il sistema ha il controllo successivo o precedente, invia un messaggio [**WM \_ GETDLGCODE**](wm-getdlgcode.md) al controllo per determinare il tipo di controllo. Il sistema sposta quindi lo stato attivo per l'input per controllare se non è un controllo statico. Se il controllo è un pulsante di opzione automatico, il sistema gli invia un [**messaggio \_ BM CLICK.**](../controls/bm-click.md) Un'applicazione può anche usare [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) per individuare i controlli in un gruppo.

In genere, il primo controllo nel gruppo combina gli stili [**WS \_ GROUP**](/windows/desktop/winmsg/window-styles) e [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) in modo che l'utente possa spostarsi da un gruppo all'altro usando il tasto TAB. Se il gruppo contiene pulsanti di opzione, l'applicazione deve applicare lo **stile WS \_ TABSTOP** solo al primo controllo del gruppo. Il sistema sposta automaticamente lo stile quando l'utente si sposta tra i controlli del gruppo. Ciò garantisce che lo stato attivo per l'input sia sempre sul controllo selezionato più di recente quando l'utente passa al gruppo usando tab.

### <a name="mnemonics"></a>Mnemonici

Un tasto di scelta è una lettera o una cifra selezionata nell'etichetta di un pulsante o nel testo di un controllo statico. Il sistema sposta lo stato attivo per l'input sul controllo associato al tasto mnemoico ogni volta che l'utente preme il tasto corrispondente al tasto mnemoico o preme questo tasto e il tasto ALT in combinazione. I tasti di scelta rapida consentono all'utente di passare rapidamente a un controllo specificato usando la tastiera.

Un'applicazione crea un carattere mnemoico per un controllo inserendo la e commerciale (&) immediatamente prima della lettera o della cifra selezionata nell'etichetta o nel testo per il controllo. Nella maggior parte dei casi, la stringa con terminazione Null fornita con il controllo nel modello di finestra di dialogo contiene la e commerciale. Tuttavia, un'applicazione può creare un tasto di scelta in qualsiasi momento sostituendo l'etichetta o il testo esistente di un controllo usando la [**funzione SetDlgItemText.**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) È possibile specificare un solo mnemoico per ogni controllo. Sebbene sia consigliabile, i mnemonici in una finestra di dialogo non devono essere univoci.

Quando l'utente preme una lettera o un tasto cifra, il sistema determina innanzitutto se il controllo corrente con lo stato attivo per l'input elabora il tasto. Il sistema invia un messaggio [**WM \_ GETDLGCODE**](wm-getdlgcode.md) al controllo e, se il controllo restituisce il valore **DLGC \_ WANTALLKEYS** o **DLG \_ WANTMESSAGE,** il sistema passa la chiave al controllo. In caso contrario, cerca un controllo il cui carattere mnemoico corrisponde alla lettera o alla cifra specificata. Continua la ricerca fino a quando non individua un controllo o non ha esaminato tutti i controlli. Durante la ricerca, ignora tutti i controlli statici con lo [**stile SS \_ NOPREFIX.**](../controls/static-control-styles.md)

Se la ricerca di un controllo con un oggetto mnemoico corrispondente rileva una finestra con lo stile **WS \_ EX \_ CONTROLPARENT,** il sistema esegue la ricerca in modo ricorsivo degli elementi figlio della finestra.

Se il sistema individua un controllo statico e il controllo non è disabilitato, sposta lo stato attivo per l'input sul primo controllo dopo il controllo statico visibile, non disabilitato e con lo stile [**WS \_ TABSTOP.**](/windows/desktop/winmsg/window-styles) Se il sistema individua un altro controllo con un oggetto mnemoico corrispondente, sposta lo stato attivo per l'input su tale controllo. Se il controllo è un pulsante di comando predefinito, il sistema invia un messaggio di notifica [**BN \_ CLICKED**](../controls/bn-clicked.md) alla procedura della finestra di dialogo. Se il controllo è un altro stile di pulsante e nella finestra di dialogo non sono presenti altri controlli con lo stesso tasto, il sistema invia il messaggio [**\_ BM CLICK**](../controls/bm-click.md) al controllo.

## <a name="dialog-box-settings"></a>Finestra di dialogo Impostazioni

Le impostazioni della finestra di dialogo sono le selezioni e i valori correnti per i controlli nella finestra di dialogo. La procedura della finestra di dialogo è responsabile dell'inizializzazione dei controlli in base a queste impostazioni durante la creazione della finestra di dialogo. È anche responsabile del recupero delle impostazioni correnti dai controlli prima di eliminare la finestra di dialogo. I metodi usati per inizializzare e recuperare le impostazioni dipendono dal tipo di controllo.

Per altre informazioni, vedere i seguenti argomenti:

-   [Pulsanti di opzione e caselle di controllo](#radio-buttons-and-check-boxes)
-   [Controlli di modifica della finestra di dialogo](#dialog-box-edit-controls)
-   [Caselle di riepilogo, caselle combinate ed elenchi di directory](#list-boxes-combo-boxes-and-directory-listings)
-   [Messaggi di controllo della finestra di dialogo](#dialog-box-control-messages)

### <a name="radio-buttons-and-check-boxes"></a>Pulsanti di opzione e caselle di controllo

Le finestre di dialogo usano pulsanti di opzione e caselle di controllo per consentire all'utente di scegliere da un elenco di opzioni. I pulsanti di opzione consentono all'utente di scegliere tra opzioni che si escludono a vicenda. le caselle di controllo consentono all'utente di selezionare una combinazione di opzioni.

La routine della finestra di dialogo può impostare lo stato iniziale di una casella di controllo usando la [**funzione CheckDlgButton,**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx) che imposta o deseleziona la casella di controllo. Per i pulsanti di opzione in un gruppo di pulsanti di opzione che si escludono a vicenda, la procedura della finestra di dialogo può usare la funzione [**CheckRadioButton**](https://msdn.microsoft.com/library/Cc410654(v=MSDN.10).aspx) per impostare il pulsante di opzione appropriato e cancellare automaticamente qualsiasi altro pulsante di opzione.

Prima del termine di una finestra di dialogo, la routine della finestra di dialogo può controllare lo stato di ogni pulsante di opzione e casella di controllo usando la funzione [**IsDlgButtonChecked,**](https://msdn.microsoft.com/library/Cc364806(v=MSDN.10).aspx) che restituisce lo stato corrente del pulsante. In genere, queste informazioni vengono salvate in una finestra di dialogo per inizializzare i pulsanti alla successiva creazione della finestra di dialogo.

### <a name="dialog-box-edit-controls"></a>Controlli di modifica della finestra di dialogo

Molte finestre di dialogo dispongono di controlli di modifica che consentono all'utente di fornire testo come input. La maggior parte delle procedure della finestra di dialogo inizializza un controllo di modifica al primo avvio della finestra di dialogo. Ad esempio, la procedura della finestra di dialogo può inserire un nome file proposto nel controllo che l'utente può quindi selezionare, modificare o sostituire. La routine della finestra di dialogo può impostare il testo in un controllo di modifica usando la [**funzione SetDlgItemText,**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) che copia il testo da un buffer specificato al controllo di modifica. Quando il controllo di modifica riceve lo stato attivo per l'input, seleziona automaticamente il testo completo per la modifica.

Poiché i controlli di modifica non restituiscono automaticamente il testo alla finestra di dialogo, la routine della finestra di dialogo deve recuperare il testo prima che termini. Può recuperare il testo usando la funzione [**GetDlgItemText,**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) che copia il testo del controllo di modifica in un buffer. La routine della finestra di dialogo in genere salva questo testo per inizializzare il controllo di modifica in un secondo momento o lo passa alla finestra padre per l'elaborazione.

Alcune finestre di dialogo usano controlli di modifica che consentono all'utente di immettere numeri. La routine della finestra di dialogo può recuperare un numero da un controllo di modifica usando la funzione [**GetDlgItemInt,**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) che recupera il testo dal controllo di modifica e converte il testo in un valore decimale. L'utente digiti il numero in cifre decimali. Può essere con o senza segno. La routine della finestra di dialogo può visualizzare un numero intero usando la [**funzione SetDlgItemInt.**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemint) **SetDlgItemInt** converte un intero con o senza segno in una stringa di cifre decimali.

### <a name="list-boxes-combo-boxes-and-directory-listings"></a>Caselle di riepilogo, caselle combinate ed elenchi di directory

Alcune finestre di dialogo visualizzano elenchi di nomi da cui l'utente può selezionare uno o più nomi. Per visualizzare un elenco di nomi file, ad esempio, una finestra di dialogo usa in genere una casella di riepilogo e le funzioni [**DlgDirList**](https://msdn.microsoft.com/library/Cc410788(v=MSDN.10).aspx) [**e DlgDirSelectEx.**](https://msdn.microsoft.com/library/Cc410769(v=MSDN.10).aspx) La **funzione DlgDirList** compila automaticamente una casella di riepilogo con i nomi file nella directory corrente. La **funzione DlgDirSelect** recupera il nome file selezionato dalla casella di riepilogo. Insieme, queste due funzioni consentono a una finestra di dialogo di visualizzare un elenco di directory in modo che l'utente possa selezionare un file senza doverne digitare il nome e il percorso.

Una finestra di dialogo può anche usare una casella combinata per visualizzare un elenco di nomi file. La [**funzione DlgDirListComboBox**](https://msdn.microsoft.com/library/Cc410798(v=MSDN.10).aspx) compila automaticamente una parte della casella di riepilogo della casella combinata con i nomi file nella directory corrente. La [**funzione DlgDirSelectComboBoxEx**](https://msdn.microsoft.com/library/Cc410768(v=MSDN.10).aspx) recupera un nome file selezionato dalla parte della casella di riepilogo.

### <a name="dialog-box-control-messages"></a>Messaggi di controllo della finestra di dialogo

Molti controlli riconoscono i messaggi predefiniti che, quando ricevuti dai controlli, comportano l'azione da parte di questi. Ad esempio, il messaggio [**\_ BM SETCHECK**](../controls/bm-setcheck.md) imposta il segno di spunta in una casella di controllo e il messaggio [**EM \_ GETSEL**](../controls/em-getsel.md) recupera la parte di testo del controllo attualmente selezionata. I messaggi di controllo offrono a una procedura di dialogo un accesso ai controlli maggiore e flessibile rispetto alle funzioni standard, quindi vengono spesso usati quando la finestra di dialogo richiede interazioni complesse con l'utente.

Una routine della finestra di dialogo può inviare un messaggio a un controllo fornendo l'identificatore del controllo e usando la funzione [**SendDlgItemMessage,**](/windows/desktop/api/Winuser/nf-winuser-senddlgitemmessagea) identica alla funzione [**SendMessage,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) ad eccezione del fatto che usa un identificatore di controllo anziché un handle di finestra per identificare il controllo che deve ricevere il messaggio. Un messaggio specificato può richiedere che la procedura di dialogo invii parametri con il messaggio e che il messaggio abbia valori restituiti corrispondenti. L'operazione e i requisiti di ogni messaggio di controllo dipendono dallo scopo del messaggio e dal controllo che lo elabora.

Per altre informazioni sui messaggi di controllo, vedere Windows [Controls](../controls/window-controls.md).

## <a name="custom-dialog-boxes"></a>Finestre di dialogo personalizzate

Un'applicazione può creare finestre di dialogo personalizzate usando una classe finestra definita dall'applicazione per le finestre di dialogo anziché la classe predefinita della finestra di dialogo. Le applicazioni usano in genere questo metodo quando una finestra di dialogo è la finestra principale, ma è utile anche per la creazione di finestre di dialogo modali e non modali per le applicazioni con finestre sovrapposte standard.

La classe della finestra definita dall'applicazione consente all'applicazione di definire una routine finestra per la finestra di dialogo ed elaborare i messaggi prima di inviarli alla routine della finestra di dialogo. Consente inoltre all'applicazione di definire un'icona della classe, un pennello di sfondo della classe e un menu della classe per la finestra di dialogo. L'applicazione deve registrare la classe window prima di tentare di creare una finestra di dialogo e deve fornire al modello di finestra di dialogo il valore atom o il nome della classe della finestra.

Molte applicazioni creano una nuova classe di finestra di dialogo recuperando prima le informazioni sulla classe della finestra di dialogo predefinita e passandoli alla funzione [**GetClassInfo,**](/windows/desktop/api/winuser/nf-winuser-getclassinfoa) che riempie una struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) con le informazioni. L'applicazione modifica i singoli membri della struttura, ad esempio il nome della classe, il pennello e l'icona, quindi registra la nuova classe usando la [**funzione RegisterClass.**](/windows/desktop/api/winuser/nf-winuser-registerclassa) Se un'applicazione riempie la struttura **WNDCLASS** di per sé, deve impostare il membro **cbWndExtra** su **DLGWINDOWEXTRA**, ovvero il numero di byte aggiuntivi necessari al sistema per ogni finestra di dialogo. Se un'applicazione usa anche byte aggiuntivi per ogni finestra di dialogo, devono superare i byte aggiuntivi richiesti dal sistema.

La routine della finestra per la finestra di dialogo personalizzata ha gli stessi parametri e requisiti di qualsiasi altra routine della finestra. A differenza di altre routine della finestra, tuttavia, la routine della finestra per questa finestra di dialogo deve chiamare la [**funzione DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) anziché la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per tutti i messaggi che non elabora. **DefDlgProc** esegue la stessa elaborazione predefinita dei messaggi della routine della finestra per la finestra di dialogo predefinita, che include la chiamata della routine della finestra di dialogo.

Un'applicazione può anche creare finestre di dialogo personalizzate sottoclassando la routine della finestra di dialogo predefinita. La [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) consente a un'applicazione di specificare la routine della finestra per una finestra specificata. L'applicazione può anche tentare di creare una sottoclasse usando la [**funzione SetClassLong,**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) ma questa operazione influisce su tutte le finestre di dialogo del sistema, non solo su quelle appartenenti all'applicazione.

Le applicazioni che creano finestre di dialogo personalizzate talvolta forniscono un'interfaccia da tastiera alternativa per le finestre di dialogo. Per le finestre di dialogo non modali, questo potrebbe significare che l'applicazione non chiama la funzione [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) ed elabora invece tutto l'input da tastiera nella routine della finestra personalizzata. In questi casi, l'applicazione può usare il [**messaggio WM \_ NEXTDLGCTL**](wm-nextdlgctl.md) per ridurre al minimo il codice necessario per spostare lo stato attivo per l'input da un controllo a un altro. Questo messaggio, quando viene passato a [**DefDlgProc,**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)sposta lo stato attivo per l'input su un controllo specificato e aggiorna l'aspetto dei controlli, ad esempio spostando il bordo predefinito del pulsante di pressione o impostando un pulsante di opzione automatico.
