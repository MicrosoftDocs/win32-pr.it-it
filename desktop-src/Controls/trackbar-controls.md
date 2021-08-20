---
title: Informazioni sui controlli Trackbar
description: Un trackbar è una finestra che contiene un dispositivo di scorrimento (talvolta denominato pollice) in un canale e segni di graduazione facoltativi. Quando l'utente sposta il dispositivo di scorrimento usando il mouse o i tasti di direzione, il trackbar invia messaggi di notifica per indicare la modifica.
ms.assetid: 9fc7bef8-da1d-493b-9a9a-3770873713f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450fba1c9b41cf5789bcda08263ff7a0b8b2d2d17db3746cf5d47bdc5d0b6a4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967943"
---
# <a name="about-trackbar-controls"></a>Informazioni sui controlli Trackbar

Un trackbar è una finestra che contiene un dispositivo di scorrimento (talvolta denominato pollice) in un canale e segni di graduazione facoltativi. Quando l'utente sposta il dispositivo di scorrimento usando il mouse o i tasti di direzione, il trackbar invia messaggi di notifica per indicare la modifica.

-   [Intervallo di selezione](#selection-range)
-   [Messaggi trackbar](#trackbar-messages)
-   [Messaggi di notifica trackbar](#trackbar-notification-messages)
-   [Elaborazione predefinita dei messaggi trackbar](#default-trackbar-message-processing)
-   [Descrizioni comando trackbar](#trackbar-tooltips)

I trackbar sono utili quando si vuole che l'utente seleziona un valore intero senza segno discreto o un set di valori interi senza segno consecutivi in un intervallo. Ad esempio, è possibile usare un trackbar per consentire all'utente di impostare la velocità di ripetizione della tastiera spostando il dispositivo di scorrimento su un determinato segno di graduazione. La figura seguente mostra un trackbar tipico.

![Screenshot di un trackbar con etichette alle estremità per un'attività lenta e veloce](images/tkb-simple.png)

Il dispositivo di scorrimento in un trackbar si sposta in incrementi specificati al momento della creazione. I valori in questo intervallo vengono definiti unità logiche. Ad esempio, se si specifica che il trackbar deve avere unità logiche che vanno da 0 a 5, il dispositivo di scorrimento può occupare solo sei posizioni: una posizione sul lato sinistro del trackbar e una posizione per ogni incremento nell'intervallo. In genere, ognuna di queste posizioni è identificata da un segno di graduazione. Tuttavia, il numero di segni di graduazione è arbitrario e può essere inferiore al numero di posizioni logiche.

Per creare un trackbar, usare la [**funzione CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) specificando la [**classe finestra TRACKBAR \_ CLASS.**](common-control-window-classes.md) Dopo aver creato un trackbar, è possibile usare i messaggi trackbar per impostare e recuperare molte delle relative proprietà. Le modifiche effettuabili includono l'impostazione delle posizioni minima e massima per il dispositivo di scorrimento, il disegno di segni di graduazione, l'impostazione di un intervallo di selezione e il riposizionamento del dispositivo di scorrimento.

## <a name="selection-range"></a>Intervallo di selezione

Se si crea un trackbar con lo [**stile \_ TBS ENABLESELRANGE,**](trackbar-control-styles.md) è possibile specificare un intervallo di selezione. Il trackbar evidenzia l'intervallo di selezione e visualizza i segni di graduazione triangolari all'inizio e alla fine, come illustrato nella figura seguente.

![Screenshot di un trackbar con un intervallo evidenziato](images/tkb-selrange.png)

L'intervallo di selezione del trackbar non influisce in alcun modo sulle relative funzionalità. L'applicazione deve implementare l'intervallo. È possibile eseguire questa operazione in uno dei modi seguenti:

-   Usare un intervallo di selezione per consentire all'utente di impostare i valori massimo e minimo per un parametro. Ad esempio, l'utente può spostare il dispositivo di scorrimento in una posizione e quindi fare clic su un pulsante con etichetta "Max". L'applicazione imposta quindi l'intervallo di selezione per visualizzare i valori scelti dall'utente.
-   Limitare lo spostamento del dispositivo di scorrimento a un intervallo secondario predeterminato all'interno del controllo, gestendo la notifica [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) e non consentire alcun movimento esterno all'intervallo di selezione. Questa operazione può essere effettuata, ad esempio, se l'intervallo di valori disponibili per l'utente può cambiare a causa di altre scelte effettuate dall'utente o in base alle risorse disponibili.

## <a name="trackbar-messages"></a>Messaggi trackbar

Le unità logiche di un trackbar sono il set di valori contigui che il trackbar può rappresentare. Vengono in genere definiti specificando l'intervallo di valori possibili con un messaggio [**\_ SETRANGE TBM**](tbm-setrange.md) non appena il trackbar è stato creato. Le applicazioni possono modificare dinamicamente l'intervallo **usando TBM \_ SETRANGE,** [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)o [**TBM \_ SETRANGEMIN.**](tbm-setrangemin.md)

Per recuperare la posizione del dispositivo di scorrimento, ovvero il valore scelto dall'utente, usare il [**messaggio \_ GETPOS TBM.**](tbm-getpos.md) Per impostare la posizione del dispositivo di scorrimento, usare il [**messaggio \_ TBM SETPOS.**](tbm-setpos.md)

Un trackbar visualizza automaticamente i segni di graduazione all'inizio e alla fine, a meno che non si specifica lo [**stile TBS \_ NOTICKS.**](trackbar-control-styles.md) Nell'editor Microsoft Visual Studio risorse, ciò significa impostare la proprietà Tick Marks su False. È possibile usare lo [**stile TBS \_ AUTOTICKS**](trackbar-control-styles.md) per visualizzare automaticamente segni di graduazione aggiuntivi a intervalli regolari lungo il trackbar. Per impostazione predefinita, un trackbar **TBS \_ AUTOTICKS** visualizza un segno di graduazione a ogni incremento dell'intervallo del trackbar. Per specificare un intervallo diverso per i segni di graduazione automatici, inviare il messaggio [**\_ TBM SETTICFREQ**](tbm-setticfreq.md) al trackbar. Ad esempio, è possibile usare questo messaggio per visualizzare solo 10 segni di graduazione in un intervallo compreso tra 1 e 100.

Per impostare la posizione di un singolo segno di graduazione, inviare il [**messaggio \_ TBM SETTIC.**](tbm-settic.md) Un trackbar mantiene una matrice di valori DWORD che archivia la posizione di ogni segno di graduazione. La matrice non include il primo e l'ultimo segno di graduazione, creati automaticamente dal trackbar. È possibile specificare un indice in questa matrice quando si invia il messaggio [**\_ GETTIC TBM**](tbm-gettic.md) per recuperare la posizione del segno di graduazione corrispondente. In alternativa, è possibile inviare il [**messaggio \_ GETPTICS TBM**](tbm-getptics.md) per recuperare un puntatore alla matrice. Il numero di elementi nella matrice è uguale a due meno del numero di tick restituito dal messaggio [**\_ GETNUMTICS di TBM.**](tbm-getnumtics.md) Questo perché il conteggio restituito da **TBM \_ GETNUMTICS** include il primo e l'ultimo segno di graduazione, che non sono inclusi nella matrice. Per recuperare la posizione fisica di un segno di graduazione, nelle coordinate client della finestra del trackbar inviare il [**messaggio \_ TBM GETTICPOS.**](tbm-getticpos.md) Il [**messaggio TBM \_ CLEARTICS**](tbm-cleartics.md) rimuove tutti i segni di graduazione di un trackbar, ma solo il primo e l'ultimo.

Le dimensioni della linea di un trackbar determinano la distanza di spostamento del dispositivo di scorrimento in risposta all'input da tastiera dei tasti di direzione, ad esempio freccia DESTRA o FRECCIA GIÙ. Per recuperare o impostare le dimensioni della riga, inviare i messaggi [**TBM \_ GETLINESIZE**](tbm-getlinesize.md) e [**TBM \_ SETLINESIZE.**](tbm-setlinesize.md) Il trackbar invia anche i codici di notifica TB LINEUP e TB LINEDOWN alla finestra padre quando l'utente \_ preme i tasti di \_ direzione.

Le dimensioni della pagina di un trackbar determinano la distanza di spostamento del dispositivo di scorrimento in risposta all'input da tastiera, ad esempio il tasto PGGIS o PGGIUTO, o l'input del mouse, ad esempio i clic nel canale del trackbar. Per recuperare o impostare le dimensioni della pagina, inviare i messaggi [**\_ TBM GETPAGESIZE**](tbm-getpagesize.md) e [**TBM \_ SETPAGESIZE.**](tbm-setpagesize.md) Il trackbar invia anche i codici di notifica TB PAGEUP e TB PAGEDOWN alla finestra padre quando riceve input da tastiera o \_ mouse che scorre la \_ pagina. Per altre informazioni, vedere [Trackbar Notification Messages](#trackbar-notification-messages).

Un'applicazione può inviare messaggi per recuperare le dimensioni di un trackbar. Il [**messaggio TBM \_ GETTHUMBRECT**](tbm-getthumbrect.md) recupera il rettangolo di delimitazione per il dispositivo di scorrimento. Il [**messaggio TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md) recupera la lunghezza del dispositivo di scorrimento. Il [**messaggio TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md) recupera il rettangolo di delimitazione per il canale del trackbar, ovvero l'area su cui si sposta il dispositivo di scorrimento. Contiene l'evidenziazione quando viene selezionato un intervallo. Se un trackbar ha lo stile [**TBS \_ FIXEDLENGTH,**](trackbar-control-styles.md) è possibile inviare il messaggio [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md) per modificare la lunghezza del dispositivo di scorrimento.

È possibile recuperare o impostare l'intervallo di selezione inviando messaggi al trackbar. Usare il [**messaggio \_ TBM SETSEL**](tbm-setsel.md) per impostare le posizioni iniziale e finale di una selezione. Per impostare solo la posizione iniziale o solo la posizione finale di una selezione, inviare un messaggio [**TBM \_ SETSELSTART**](tbm-setselstart.md) o [**TBM \_ SETSELEND.**](tbm-setselend.md) Per recuperare le posizioni iniziale o finale di un intervallo di selezione, inviare un [**messaggio TBM \_ GETSELSTART**](tbm-getselstart.md) o [**TBM \_ GETSELEND.**](tbm-getselend.md) Per cancellare un intervallo di selezione e ripristinare l'intervallo originale del trackbar, inviare il [**messaggio \_ TBM CLEARSEL.**](tbm-clearsel.md)

> [!Note]  
> È responsabilità dell'applicazione assicurarsi che l'utente non possa selezionare valori esterni all'intervallo di selezione. Il controllo stesso non impedisce all'utente di spostare il dispositivo di scorrimento al di fuori dell'intervallo.

 

## <a name="trackbar-notification-messages"></a>Messaggi di notifica trackbar

Un trackbar notifica alla finestra padre le azioni dell'utente inviando all'elemento padre un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL.**](wm-vscroll.md) Un trackbar con lo stile [**TBS \_ HORZ**](trackbar-control-styles.md) invia **messaggi WM \_ HSCROLL.** Un trackbar con lo stile [**TBS \_ VERT**](trackbar-control-styles.md) invia **messaggi \_ VSCROLL WM.** La parola meno ordinata del *parametro wParam* di **WM \_ HSCROLL** o **WM \_ VSCROLL** contiene il codice di notifica. Per i codici di notifica TB THUMBPOSITION e TB THUMBTRACK, la parola più alta del \_ \_ parametro *wParam* specifica la posizione del dispositivo di scorrimento. Per tutti gli altri codici di notifica, la parola di ordine elevato è zero. inviare il [**messaggio \_ GETPOS TBM**](tbm-getpos.md) per determinare la posizione del dispositivo di scorrimento. Il *parametro lParam* è l'handle per il trackbar.

Il sistema invia i codici di notifica TB \_ BOTTOM, TB LINEDOWN, TB LINEUP e TB TOP solo quando l'utente interagisce con un \_ \_ \_ trackbar usando la tastiera. I codici di notifica TB THUMBPOSITION e TB THUMBTRACK vengono \_ inviati solo quando \_ l'utente usa il mouse. I codici \_ di notifica TB ENDTRACK, TB PAGEDOWN e \_ TB \_ PAGEUP vengono inviati in entrambi i casi. Nella tabella seguente sono elencati i codici di notifica del trackbar [](/windows/desktop/inputdev/virtual-key-codes)e gli eventi (codici tasto virtuale o eventi del mouse) che determinano l'invio delle notifiche dei codici chiave virtuale.



| Codice di notifica | Motivo inviato                                                                                                                     |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| TB \_ INFERIORE        | [**VK \_ END**](/windows/desktop/inputdev/virtual-key-codes)                                                                         |
| TB \_ ENDTRACK      | [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) (l'utente ha rilasciato una chiave che ha inviato un codice chiave virtuale pertinente)                              |
| TB \_ LINEDOWN      | [**VK \_ RIGHT**](/windows/desktop/inputdev/virtual-key-codes) o [ **VK \_ DOWN**](/windows/desktop/inputdev/virtual-key-codes)     |
| TB \_ LINEUP        | [**VK \_ LEFT**](/windows/desktop/inputdev/virtual-key-codes) o [ **VK \_ UP**](/windows/desktop/inputdev/virtual-key-codes)              |
| TB \_ PAGEDOWN      | [**VK \_ NEXT**](/windows/desktop/inputdev/virtual-key-codes) (l'utente ha fatto clic sul canale sotto o a destra del dispositivo di scorrimento)   |
| TB \_ PAGEUP        | [**VK \_ PRIOR**](/windows/desktop/inputdev/virtual-key-codes) (l'utente ha fatto clic sul canale sopra o a sinistra del dispositivo di scorrimento) |
| TB \_ THUMBPOSITION | [**WM \_ LBUTTONUP dopo**](/windows/desktop/inputdev/wm-lbuttonup) un codice di notifica THUMBTRACK da \_ TB                                         |
| TB \_ THUMBTRACK    | Spostamento del dispositivo di scorrimento (l'utente ha trascinato il dispositivo di scorrimento)                                                                                   |
| TB \_ TOP           | [**VK \_ HOME**](/windows/desktop/inputdev/virtual-key-codes)                                                                      |



 

## <a name="default-trackbar-message-processing"></a>Elaborazione predefinita dei messaggi trackbar

Questa sezione descrive l'elaborazione dei messaggi della finestra eseguita da un trackbar.



| Message                                              | Elaborazione eseguita                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAPTURECHANGED**](/windows/desktop/inputdev/wm-capturechanged) | Kills the timer if one was set during [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) processing and sends the TB \_ THUMBPOSITION notification code, if necessary. Invia sempre il codice di notifica \_ ENDTRACK TB.                                     |
| [**CREAZIONE DI WM \_**](/windows/desktop/winmsg/wm-create)                   | Esegue un'inizializzazione aggiuntiva, ad esempio impostando le dimensioni della riga, le dimensioni della pagina e la frequenza dei segni di graduazione su valori predefiniti.                                                                                                                                 |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)                 | Libera le risorse.                                                                                                                                                                                                                                         |
| [**ABILITAZIONE DI \_ WM**](/windows/desktop/winmsg/wm-enable)                   | Ridisegna la finestra del trackbar.                                                                                                                                                                                                                            |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)           | Cancella lo sfondo della finestra, usando il colore di sfondo corrente per il trackbar.                                                                                                                                                                       |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)           | Restituisce il valore DLGC \_ WANTARROWS.                                                                                                                                                                                                                      |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)               | Elabora le chiavi di direzione e invia i codici di notifica TB \_ TOP, TB \_ BOTTOM, TB \_ PAGEUP, TB \_ PAGEDOWN, TB LINEUP e \_ TB \_ LINEDOWN, in base alle esigenze.                                                                                               |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)                   | Invia il codice \_ di notifica ENDTRACK tb se la chiave era una delle chiavi di direzione.                                                                                                                                                                       |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)           | Ridisegna la finestra del trackbar.                                                                                                                                                                                                                            |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)       | Imposta lo stato attivo e l'acquisizione del mouse sul trackbar. Se necessario, imposta un timer che determina la velocità con cui il dispositivo di scorrimento si sposta verso il cursore del mouse quando l'utente tiene premuto il pulsante del mouse nella finestra.                                      |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)           | Rilascia il mouse capture e termina il timer se ne è stato impostato uno durante l'elaborazione [**di WM \_ LBUTTONDOWN.**](/windows/desktop/inputdev/wm-lbuttondown) Invia il codice di notifica \_ THUMBPOSITION tb, se necessario. Invia sempre il codice di notifica \_ ENDTRACK TB. |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)           | Sposta il dispositivo di scorrimento e invia il codice di notifica THUMBTRACK tb \_ durante il rilevamento del mouse (vedere WM [**\_ TIMER**](/windows/desktop/winmsg/wm-timer)).                                                                                                                          |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                        | Disegna il trackbar. Se il parametro wParam è diverso da NULL, il controllo presuppone che il valore sia hdc e dipinge usando tale contesto di dispositivo.                                                                                                             |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)             | Ridisegna la finestra del trackbar.                                                                                                                                                                                                                            |
| [**DIMENSIONI \_ WM**](/windows/desktop/winmsg/wm-size)                       | Imposta le dimensioni del trackbar, rimuovendo il dispositivo di scorrimento se non c'è spazio sufficiente per visualizzarlo.                                                                                                                                                      |
| [**WM \_ TIMER**](/windows/desktop/winmsg/wm-timer)                     | Recupera la posizione del mouse e aggiorna la posizione del dispositivo di scorrimento. Viene ricevuto solo quando l'utente trascina il dispositivo di scorrimento.                                                                                                                         |
| [**WM \_ WININICHANGE**](/windows/desktop/winmsg/wm-wininichange)       | Inizializza le dimensioni del dispositivo di scorrimento.                                                                                                                                                                                                                           |



 

## <a name="trackbar-tooltips"></a>Descrizioni comando trackbar

Un trackbar creato con lo stile [**TBS \_ TOOLTIPS**](trackbar-control-styles.md) ha un controllo descrizione comando predefinito. La descrizione comando rimane visibile e visualizza il valore corrente mentre l'utente trascina il dispositivo di scorrimento usando il mouse.

È possibile assegnare un nuovo controllo descrizione comando a un trackbar inviando il [**messaggio \_ TBM SETTOOLTIPS.**](tbm-settooltips.md) Per recuperare l'handle per un controllo descrizione comando assegnato, usare il [**messaggio \_ TBM GETTOOLTIPS.**](tbm-gettooltips.md)

 

 