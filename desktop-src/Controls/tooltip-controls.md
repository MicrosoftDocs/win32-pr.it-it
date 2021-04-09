---
title: Informazioni sui controlli ToolTip
description: Le descrizioni comandi vengono visualizzate automaticamente oppure compaiono quando l'utente posiziona il puntatore del mouse su uno strumento o su un altro elemento dell'interfaccia utente.
ms.assetid: 1020cec7-57b4-4463-9419-f80fd14fa12c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9c1042523c86e794865da5d38fb023ee37d60b4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047441"
---
# <a name="about-tooltip-controls"></a>Informazioni sui controlli ToolTip

Le descrizioni comandi vengono visualizzate automaticamente oppure compaiono quando l'utente posiziona il puntatore del mouse su uno strumento o su un altro elemento dell'interfaccia utente. La descrizione comando viene visualizzata accanto al puntatore e scompare quando l'utente fa clic su un pulsante del mouse, sposta il puntatore fuori dallo strumento o semplicemente attende qualche secondo.

Il controllo ToolTip nell'illustrazione seguente mostra le informazioni su un file sul desktop di Windows. Quando si sposta il puntatore del mouse sull'illustrazione, dovrebbe essere visualizzata anche una descrizione comando in tempo reale contenente testo descrittivo.

![screenshot che mostra il testo in una descrizione comando visualizzata su un file sul desktop](images/tt-desktop.png)

In questa sezione viene descritto il funzionamento del controllo ToolTip e la relativa modalità di creazione.

-   [Comportamento e aspetto della descrizione comando](#tooltip-behavior-and-appearance)
-   [Creazione di controlli ToolTip](#creating-tooltip-controls)
-   [Attivazione di controlli ToolTip](#activating-tooltip-controls)
-   [Strumenti di supporto](#supporting-tools)
-   [Visualizzazione di testo](#displaying-text)
-   [Messaggistica e notifica](#messaging-and-notification)
-   [Hit Testing](#hit-testing)
-   [Elaborazione del messaggio predefinita](#default-message-processing)

## <a name="tooltip-behavior-and-appearance"></a>Comportamento e aspetto della descrizione comando

I controlli ToolTip possono visualizzare una singola riga di testo o più righe. Gli angoli possono essere arrotondati o quadrati. Potrebbero o meno avere un gambo che punta agli strumenti come un fumetto di riconoscimento vocale. Il testo della descrizione comando può essere stazionario o può essere spostato con il puntatore del mouse, denominato Tracking. Il testo stazionario può essere visualizzato accanto a uno strumento oppure può essere visualizzato su uno strumento, che viene definito sul posto. Le descrizioni comandi standard sono fisse, visualizzano una singola riga di testo, hanno angoli quadrati e non hanno alcun gambo che punta allo strumento.

Le descrizioni comandi di rilevamento, supportate dalla [versione 4,70](common-control-versions.md) dei controlli comuni, modificano la posizione sullo schermo in modo dinamico. Aggiornando rapidamente la posizione, questi controlli della descrizione comando sembrano essere spostati in modo semplice o "Track". Queste informazioni sono utili quando si desidera che il testo della descrizione comando segua la posizione del puntatore del mouse durante lo spostamento. Per ulteriori informazioni sul rilevamento di descrizioni comando e un esempio di codice che illustra come crearle, vedere la pagina relativa alle [descrizioni comandi di rilevamento](using-tooltip-contro.md).

Le descrizioni comando su più righe, anch ' esse supportate dalla versione 4,70 dei controlli comuni, visualizzano il testo su più righe. Sono utili per la visualizzazione di messaggi lunghi. Per ulteriori informazioni e un esempio in cui viene illustrato come creare descrizioni comandi su più righe, vedere [descrizioni comando](using-tooltip-contro.md)su più righe.

Le descrizioni comandi a fumetti vengono visualizzate in una casella con angoli arrotondati e un gambo che punta allo strumento. Possono essere su una sola riga o su più righe. Nella figura seguente viene mostrata una descrizione comando a fumetti con il gambo e il rettangolo nelle posizioni predefinite. Per ulteriori informazioni sulle descrizioni comandi dei fumetti e un esempio in cui viene illustrato come crearle, vedere [utilizzo dei controlli ToolTip](using-tooltip-contro.md).

![screenshot che mostra una descrizione comando contenente una riga di testo, posizionata sopra un pulsante in una finestra di dialogo](images/tt-balloon.png)

Una descrizione comando può avere anche testo del titolo e un'icona, come illustrato nella figura seguente. Si noti che la descrizione comando deve avere testo; Se è presente solo testo del titolo, la descrizione comando non viene visualizzata. Inoltre, l'icona non viene visualizzata a meno che non esista un titolo.

![screenshot che mostra una descrizione comando con un'icona, un titolo e un testo posizionati sotto un pulsante in una finestra di dialogo](images/tt-titled.png)

Talvolta le stringhe di testo vengono ritagliate perché sono troppo lunghe per essere visualizzate completamente in una finestra piccola. Le descrizioni comando sul posto vengono usate per visualizzare le stringhe di testo per gli oggetti che sono stati ritagliati, ad esempio il nome del file nella figura seguente. Per un esempio in cui viene illustrato come creare descrizioni comando sul posto, vedere [descrizioni comando sul posto](using-tooltip-contro.md).

![screenshot che mostra una descrizione comando contenente un nome file posizionato accanto a un'icona di file in un controllo albero](images/tt-inplace.png)

Il cursore deve passare il mouse su uno strumento per un certo periodo di tempo prima che venga visualizzata la descrizione comando. La durata predefinita di questo timeout è controllata dall'ora di doppio clic dell'utente e in genere è di circa un mezzo secondo. Per specificare un valore di timeout non predefinito, inviare la descrizione comando di un messaggio [**TTM \_ SETDELAYTIME**](ttm-setdelaytime.md) .

## <a name="creating-tooltip-controls"></a>Creazione di controlli ToolTip

Per creare un controllo ToolTip, chiamare [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificare la classe della finestra della [**\_ classe Tooltips**](common-control-window-classes.md) . Questa classe viene registrata quando viene caricata la DLL del controllo comune. Per assicurarsi che questa DLL venga caricata, includere la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) nell'applicazione. È necessario definire in modo esplicito un controllo ToolTip come in primo piano. In caso contrario, potrebbe essere coperto dalla finestra padre. Nel frammento di codice seguente viene illustrato come creare un controllo ToolTip.


```
HWND hwndTip = CreateWindowEx(NULL, TOOLTIPS_CLASS, NULL,
                            WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP,
                            CW_USEDEFAULT, CW_USEDEFAULT,
                            CW_USEDEFAULT, CW_USEDEFAULT,
                            hwndParent, NULL, hinstMyDll,
                            NULL);

SetWindowPos(hwndTip, HWND_TOPMOST,0, 0, 0, 0,
             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);
```



La routine della finestra per il controllo ToolTip imposta automaticamente le dimensioni, la posizione e la visibilità del controllo. L'altezza della finestra della descrizione comando è basata sull'altezza del tipo di carattere attualmente selezionato nel contesto di dispositivo per il controllo ToolTip. La larghezza varia in base alla lunghezza della stringa attualmente nella finestra della descrizione comando.

## <a name="activating-tooltip-controls"></a>Attivazione di controlli ToolTip

Un controllo ToolTip può essere attivo o inattivo. Quando è attivo, il testo della descrizione comando viene visualizzato quando il puntatore del mouse si trova su uno strumento. Quando è inattivo, il testo della descrizione comando non viene visualizzato, anche se il puntatore si trova in uno strumento. Il messaggio [**TTM \_ Activate**](ttm-activate.md) attiva e disattiva un controllo ToolTip.

## <a name="supporting-tools"></a>Strumenti di supporto

Un controllo ToolTip può supportare un numero qualsiasi di strumenti. Per supportare un particolare strumento, è necessario registrare lo strumento con il controllo ToolTip inviando il controllo al messaggio [**TTM \_ ADDTOOL**](ttm-addtool.md) . Il messaggio include l'indirizzo di una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , che fornisce le informazioni necessarie al controllo ToolTip per visualizzare il testo per lo strumento. Il membro **uID** della struttura **TOOLINFO** è definito dall'applicazione. Ogni volta che si aggiunge uno strumento, l'applicazione fornisce un identificatore univoco. Il membro **cbSize** della struttura **TOOLINFO** è obbligatorio e deve specificare le dimensioni della struttura.

Un controllo ToolTip supporta gli strumenti implementati come Windows (ad esempio finestre figlio o finestre di controllo) e come aree rettangolari all'interno dell'area client di una finestra. Quando si aggiunge uno strumento implementato come area rettangolare, il membro **HWND** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) deve specificare l'handle per la finestra che contiene l'area e il membro **Rect** deve specificare le coordinate client del rettangolo di delimitazione dell'area. Inoltre, il membro **uID** deve specificare l'identificatore definito dall'applicazione per lo strumento.

Quando si aggiunge uno strumento implementato come finestra, il membro **uID** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) deve contenere l'handle della finestra per lo strumento. Il membro **uFlags** deve inoltre specificare il valore **\_ IDISHWND di ttf** , che indica al controllo ToolTip di interpretare il membro **uID** come handle di finestra.

## <a name="displaying-text"></a>Visualizzazione di testo

Quando si aggiunge uno strumento a un controllo ToolTip, il membro **lpszText** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) deve specificare l'indirizzo della stringa da visualizzare per lo strumento. Dopo l'aggiunta di uno strumento, è possibile modificare il testo utilizzando il messaggio [**TTM \_ UPDATETIPTEXT**](ttm-updatetiptext.md) .

Se la parola più significativa di **lpszText** è zero, la parola di basso livello deve corrispondere all'identificatore di una risorsa di stringa. Quando il controllo ToolTip necessita del testo, il sistema carica la risorsa di stringa specificata dall'istanza dell'applicazione identificata dal membro **hInst** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .

Se si specifica il \_ valore LPSTR TEXTCALLBACK nel membro **lpszText** , il controllo ToolTip notifica la finestra specificata nel membro **HWND** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)ogni volta che il controllo ToolTip deve visualizzare il testo per lo strumento. Il controllo tooltip Invia il codice di notifica [ \_ GETDISPINFO di TTN](ttn-getdispinfo.md) alla finestra di. Il messaggio include l'indirizzo di una struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) , che contiene l'handle della finestra e l'identificatore definito dall'applicazione per lo strumento. La finestra esamina la struttura per determinare lo strumento per il quale è necessario il testo e riempie i membri della struttura appropriati con le informazioni necessarie al controllo ToolTip per visualizzare la stringa.

> [!Note]  
> La lunghezza massima consentita per il testo della descrizione comando standard è 80 caratteri. Per ulteriori informazioni, vedere la struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) . Il testo della descrizione comando su più righe può essere maggiore.

 

Molte applicazioni creano barre degli strumenti che contengono strumenti che corrispondono ai comandi di menu. Per questi strumenti è utile che il controllo ToolTip visualizzi lo stesso testo della voce di menu corrispondente. Il sistema rimuove automaticamente i caratteri dell'acceleratore e commerciale (&) da tutte le stringhe passate a un controllo ToolTip e termina la stringa in corrispondenza del primo carattere di tabulazione ( \\ t), a meno che il controllo non abbia lo stile [**TTS \_ NoPrefix**](tooltip-styles.md) .

Per recuperare il testo per uno strumento, usare il [**messaggio \_ gettext TTM**](ttm-gettext.md) .

## <a name="messaging-and-notification"></a>Messaggistica e notifica

Il testo della descrizione comando viene in genere visualizzato quando il puntatore del mouse viene posizionato su un'area, in genere il rettangolo definito da uno strumento, ad esempio un controllo Button. Tuttavia, Microsoft Windows invia solo messaggi relativi al mouse alla finestra che contiene il puntatore, non al controllo ToolTip stesso. Le informazioni relative al mouse devono essere inoltrate al controllo ToolTip affinché venga visualizzato il testo della descrizione comando al momento e al posizionamento appropriati.

È possibile che i messaggi vengano inoltrati automaticamente se:

-   Lo strumento è un controllo o è definito come un rettangolo nella struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) dello strumento.
-   La finestra associata allo strumento si trova nello stesso thread del controllo ToolTip.

Se queste due condizioni vengono soddisfatte, impostare il flag della **\_ sottoclasse ttf** nel membro **uFlags** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) dello strumento quando si aggiunge lo strumento al controllo ToolTip con [**TTM \_ ADDTOOL**](ttm-addtool.md). I messaggi del mouse necessari verranno inoltrati automaticamente al controllo ToolTip.

Per la maggior parte degli scopi, l'impostazione della **\_ sottoclasse ttf** per l'inoltro dei messaggi del mouse al controllo è sufficiente. Tuttavia, non funzionerà nei casi in cui non esiste una connessione diretta tra il controllo ToolTip e la finestra dello strumento. Se, ad esempio, uno strumento viene implementato come area rettangolare in una finestra definita dall'applicazione, la routine della finestra riceverà i messaggi del mouse. L'impostazione della **\_ sottoclasse ttf** è sufficiente per assicurarsi che vengano passate al controllo. Tuttavia, se uno strumento viene implementato come una finestra definita dal sistema, i messaggi del mouse vengono inviati a tale finestra e non sono direttamente disponibili per l'applicazione. In questo caso, è necessario sottoclassare la finestra o utilizzare un hook di messaggio per accedere ai messaggi del mouse. È necessario inoltrare i messaggi del mouse in modo esplicito al controllo ToolTip con [**TTM \_ RELAYEVENT**](ttm-relayevent.md). Per un esempio di come usare **TTM \_ RELAYEVENT**, vedere la pagina relativa alla [Verifica delle descrizioni comandi](using-tooltip-contro.md).

Quando un controllo ToolTip riceve un messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) , determina se il puntatore del mouse si trova nel rettangolo di delimitazione di uno strumento. In caso contrario, il controllo ToolTip imposta un timer. Al termine dell'intervallo di timeout, il controllo ToolTip controlla la posizione del puntatore per verificare se è stato spostato. In caso contrario, il controllo ToolTip Recupera il testo per lo strumento e visualizza la descrizione comando. Il controllo ToolTip continua a visualizzare la finestra fino a quando non riceve un messaggio di pulsante o di un pulsante inoltrato o fino a quando un messaggio di **WM \_ MOUSEMOVE** indica che l'indicatore di misura è stato spostato all'esterno del rettangolo delimitatore dello strumento.

Un controllo ToolTip dispone effettivamente di tre durate di timeout associate. La durata iniziale indica il momento in cui il puntatore del mouse deve rimanere fermo all'interno del rettangolo di delimitazione di uno strumento prima che venga visualizzata la finestra della descrizione comando. La durata della rivisualizzazione è la lunghezza del ritardo prima che le successive finestre della descrizione comando vengano visualizzate quando il puntatore viene spostato da uno strumento a un altro. La durata del popup è il momento in cui la finestra della descrizione comando rimane visualizzata prima che venga nascosta. Ovvero, se il puntatore rimane fermo all'interno del rettangolo di delimitazione dopo la visualizzazione della finestra della descrizione comando, la finestra della descrizione comando viene nascosta automaticamente alla fine della durata del popup. È possibile modificare tutte le durate di timeout usando il messaggio [**TTM \_ SETDELAYTIME**](ttm-setdelaytime.md) .

Se un'applicazione include uno strumento implementato come area rettangolare e le dimensioni o la posizione del controllo cambiano, l'applicazione può utilizzare il messaggio [**TTM \_ NEWTOOLRECT**](ttm-newtoolrect.md) per segnalare la modifica al controllo ToolTip. Non è necessario che un'applicazione riporti le modifiche delle dimensioni e della posizione per uno strumento implementato come finestra perché il controllo ToolTip usa l'handle della finestra dello strumento per determinare se il puntatore del mouse si trova nello strumento, non nel rettangolo di delimitazione dello strumento.

Quando una descrizione comando sta per essere visualizzata, il controllo tooltip Invia alla finestra proprietaria un [TTN \_ Mostra](ttn-show.md) il codice di notifica. La finestra proprietaria riceve un codice di notifica [ \_ pop TTN](ttn-pop.md) quando una descrizione comando sta per essere nascosta. Ogni codice di notifica viene inviato nel contesto di un messaggio di [**\_ notifica WM**](wm-notify.md) .

## <a name="hit-testing"></a>Hit Testing

Il messaggio [**TTM \_ HITTEST**](ttm-hittest.md) consente di recuperare informazioni che un controllo ToolTip gestisce sullo strumento che occupa un particolare punto. Il messaggio include una struttura [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) che contiene un handle di finestra, le coordinate di un punto e l'indirizzo di una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Il controllo ToolTip determina se uno strumento occupa il punto e, in caso contrario, Compila **TOOLINFO** con le informazioni sullo strumento.

## <a name="default-message-processing"></a>Elaborazione del messaggio predefinita

Nella tabella seguente vengono descritti i messaggi gestiti dalla routine della finestra per il controllo ToolTip.



| Message                                        | Descrizione                                                                                                                                                                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**creazione di WM \_**](/windows/desktop/winmsg/wm-create)             | Assicura che il controllo ToolTip disponga degli stili [**WS- \_ \_ TOOLWINDOW**](/windows/desktop/winmsg/window-styles) e [**WS \_ popup**](/windows/desktop/winmsg/window-styles) Window. Alloca inoltre memoria e inizializza le variabili interne. |
| [**eliminazione di WM \_**](/windows/desktop/winmsg/wm-destroy)           | Libera le risorse allocate per il controllo ToolTip.                                                                                                                                                                                                                |
| [**\_tipo di carattere WM GetFont**](/windows/desktop/winmsg/wm-getfont)           | Restituisce l'handle del tipo di carattere che il controllo ToolTip utilizzerà per creare il testo.                                                                                                                                                                                    |
| [**MOUSEMOVE di WM \_**](/windows/desktop/inputdev/wm-mousemove)     | Nasconde la finestra della descrizione comando.                                                                                                                                                                                                                                         |
| [**\_disegno WM**](/windows/desktop/gdi/wm-paint)                  | Disegna la finestra della descrizione comando.                                                                                                                                                                                                                                         |
| [**\_tipo di carattere WM**](/windows/desktop/winmsg/wm-setfont)           | Imposta l'handle del tipo di carattere che il controllo ToolTip utilizzerà per creare il testo.                                                                                                                                                                                       |
| [**\_timer WM**](/windows/desktop/winmsg/wm-timer)               | Nasconde la finestra della descrizione comando se lo strumento è stato modificato o se il puntatore del mouse è stato spostato all'esterno dello strumento. In caso contrario, viene visualizzata la finestra descrizione comando.                                                                                                             |
| [**\_WININICHANGE WM**](/windows/desktop/winmsg/wm-wininichange) | Reimposta le variabili interne basate sulle metriche di sistema.                                                                                                                                                                                                       |



 

 

 