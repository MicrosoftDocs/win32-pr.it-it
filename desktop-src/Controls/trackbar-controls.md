---
title: Informazioni sui controlli TrackBar
description: Un TrackBar è una finestra che contiene un dispositivo di scorrimento (talvolta denominato Thumb) in un canale e segni di graduazione facoltativi. Quando l'utente sposta il dispositivo di scorrimento usando il mouse o i tasti di direzione, il TrackBar invia messaggi di notifica per indicare la modifica.
ms.assetid: 9fc7bef8-da1d-493b-9a9a-3770873713f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e364f57a094ed5a29369a00a112150d0282f24
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730490"
---
# <a name="about-trackbar-controls"></a>Informazioni sui controlli TrackBar

Un TrackBar è una finestra che contiene un dispositivo di scorrimento (talvolta denominato Thumb) in un canale e segni di graduazione facoltativi. Quando l'utente sposta il dispositivo di scorrimento usando il mouse o i tasti di direzione, il TrackBar invia messaggi di notifica per indicare la modifica.

-   [Intervallo di selezione](#selection-range)
-   [Messaggi TrackBar](#trackbar-messages)
-   [Messaggi di notifica TrackBar](#trackbar-notification-messages)
-   [Elaborazione del messaggio TrackBar predefinita](#default-trackbar-message-processing)
-   [Descrizioni comandi di TrackBar](#trackbar-tooltips)

Gli TrackBar sono utili quando si desidera che l'utente selezioni un valore Unsigned Integer discreto o un set di valori Unsigned Integer consecutivi in un intervallo. Ad esempio, è possibile utilizzare un TrackBar per consentire all'utente di impostare la frequenza di ripetizione della tastiera spostando il dispositivo di scorrimento su un segno di graduazione specificato. Nella figura seguente viene illustrato un TrackBar tipico.

![Screenshot di un TrackBar con etichette alle estremità per lenti e veloci](images/tkb-simple.png)

Il dispositivo di scorrimento in un TrackBar si sposta in incrementi specificati al momento della creazione. I valori in questo intervallo sono detti unità logiche. Se, ad esempio, si specifica che l'oggetto TrackBar deve avere unità logiche che variano da 0 a 5, il dispositivo di scorrimento può occupare solo sei posizioni: una posizione sul lato sinistro del TrackBar e una posizione per ogni incremento nell'intervallo. In genere, ciascuna di queste posizioni è identificata da un segno di graduazione. Tuttavia, il numero di segni di graduazione è arbitrario e può essere inferiore al numero di posizioni logiche.

Per creare un TrackBar, utilizzare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra della [**\_ classe TrackBar**](common-control-window-classes.md) . Dopo aver creato un TrackBar, è possibile utilizzare i messaggi TrackBar per impostare e recuperare molte delle relative proprietà. Le modifiche effettuabili includono l'impostazione delle posizioni minima e massima per il dispositivo di scorrimento, il disegno di segni di graduazione, l'impostazione di un intervallo di selezione e il riposizionamento del dispositivo di scorrimento.

## <a name="selection-range"></a>Intervallo di selezione

Se si crea un TrackBar con lo stile [**TBS \_ ENABLESELRANGE**](trackbar-control-styles.md) , è possibile specificare un intervallo di selezione. Il TrackBar evidenzia l'intervallo di selezione e Visualizza i segni di graduazione triangolari all'inizio e alla fine, come illustrato nella figura seguente.

![Screenshot di un TrackBar con un intervallo evidenziato](images/tkb-selrange.png)

L'intervallo di selezione del TrackBar non influisce in alcun modo sulle relative funzionalità. Spetta all'applicazione implementare l'intervallo. Questa operazione può essere eseguita in uno dei modi seguenti:

-   Utilizzare un intervallo di selezione per consentire all'utente di impostare i valori massimo e minimo per alcuni parametri. Ad esempio, l'utente potrebbe spostare il dispositivo di scorrimento in una posizione e quindi fare clic su un pulsante con etichetta "Max". L'applicazione imposta quindi l'intervallo di selezione per visualizzare i valori scelti dall'utente.
-   Limitare lo spostamento del dispositivo di scorrimento a un intervallo secondario predeterminato all'interno del controllo, gestendo la notifica [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) e non consentire lo spostamento al di fuori dell'intervallo di selezione. Questa operazione può essere eseguita, ad esempio, se l'intervallo di valori disponibili per l'utente può cambiare a causa di altre scelte effettuate dall'utente o in base alle risorse disponibili.

## <a name="trackbar-messages"></a>Messaggi TrackBar

Le unità logiche di un TrackBar sono il set di valori contigui che possono essere rappresentati da TrackBar. Vengono in genere definite specificando l'intervallo di valori possibili con un messaggio di [**\_ SetRange TBM**](tbm-setrange.md) non appena il TrackBar è stato creato. Le applicazioni possono modificare dinamicamente l'intervallo usando **TBM \_ SetRange**, [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)o [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md).

Per recuperare la posizione del dispositivo di scorrimento (ovvero il valore scelto dall'utente), usare il messaggio [**TBM \_ GETPOS**](tbm-getpos.md) . Per impostare la posizione del dispositivo di scorrimento, utilizzare il messaggio [**TBM \_ SETPOS**](tbm-setpos.md) .

Un TrackBar Visualizza automaticamente i segni di graduazione all'inizio e alla fine, a meno che non si specifichi lo stile TBS nosegni di [**\_ spunta**](trackbar-control-styles.md) . Nell'editor di risorse Microsoft Visual Studio questo significa impostare la proprietà dei segni di graduazione su false. Per visualizzare automaticamente segni di graduazione aggiuntivi a intervalli regolari lungo il TrackBar, è possibile usare lo stile [**TBS \_ autograduates**](trackbar-control-styles.md) . Per impostazione predefinita, un indicatore di scorrimento automatico di TBS Visualizza un segno di graduazione a ogni incremento dell'intervallo del TrackBar. **\_** Per specificare un intervallo diverso per i segni di graduazione automatici, inviare il messaggio [**\_ SETTICFREQ TBM**](tbm-setticfreq.md) al TrackBar. Ad esempio, è possibile usare questo messaggio per visualizzare solo 10 segni di graduazione in un intervallo compreso tra 1 e 100.

Per impostare la posizione di un segno di graduazione singolo, inviare il messaggio [**\_ SETTIC TBM**](tbm-settic.md) . Un TrackBar mantiene una matrice di valori DWORD che archivia la posizione di ogni segno di graduazione. La matrice non include il primo e l'ultimo segno di graduazione, che il TrackBar crea automaticamente. È possibile specificare un indice in questa matrice quando si invia il [**messaggio \_ Getter TBM**](tbm-gettic.md) per recuperare la posizione del segno di graduazione corrispondente. In alternativa, è possibile inviare il [**messaggio \_ GETPTICS TBM**](tbm-getptics.md) per recuperare un puntatore alla matrice. Il numero di elementi nella matrice è uguale a due minori rispetto al conteggio restituito dal messaggio [**\_ GETNUMTICS TBM**](tbm-getnumtics.md) . Questo perché il numero restituito da **TBM \_ GETNUMTICS** include il primo e l'ultimo segno di graduazione, che non sono inclusi nella matrice. Per recuperare la posizione fisica di un segno di graduazione, in coordinate client della finestra del TrackBar, inviare il messaggio [**\_ GETTICPOS TBM**](tbm-getticpos.md) . Il messaggio [**TBM \_ CLEARTICS**](tbm-cleartics.md) rimuove tutti i segni di graduazione di un TrackBar, tranne il primo e l'ultimo.

Le dimensioni di riga di un TrackBar determinano la distanza di spostamento del dispositivo di scorrimento in risposta all'input da tastiera dei tasti di direzione, ad esempio la freccia destra o il tasto freccia giù. Per recuperare o impostare le dimensioni della riga, inviare i messaggi [**TBM \_ GETLINESIZE**](tbm-getlinesize.md) e [**TBM \_ SETLINESIZE**](tbm-setlinesize.md) . TrackBar invia inoltre i \_ codici di notifica TB TB e TB \_ LINEDOWN alla finestra padre quando l'utente preme i tasti di direzione.

Le dimensioni di pagina di un TrackBar determinano la distanza di spostamento del dispositivo di scorrimento in risposta a input da tastiera, ad esempio il tasto PGSU o PGGIÙ o l'input del mouse, ad esempio i clic nel canale TrackBar. Per recuperare o impostare le dimensioni della pagina, inviare i messaggi [**TBM \_ GetPageSize**](tbm-getpagesize.md) e [**TBM \_**](tbm-setpagesize.md) di. TrackBar invia inoltre i \_ codici di notifica TB PAGEUP e TB \_ PGGIÙ alla finestra padre quando riceve l'input della tastiera o del mouse che scorre la pagina. Per ulteriori informazioni, vedere la pagina relativa ai [messaggi di notifica TrackBar](#trackbar-notification-messages).

Un'applicazione può inviare messaggi per recuperare le dimensioni di un TrackBar. Il messaggio [**TBM \_ GETTHUMBRECT**](tbm-getthumbrect.md) Recupera il rettangolo di delimitazione per il dispositivo di scorrimento. Il messaggio [**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md) recupera la lunghezza del dispositivo di scorrimento. Il messaggio [**TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md) Recupera il rettangolo di delimitazione per il canale del TrackBar, ovvero l'area su cui si sposta il dispositivo di scorrimento. Contiene l'evidenziazione quando viene selezionato un intervallo. Se un TrackBar ha lo stile [**TBS \_ FIXEDLENGTH**](trackbar-control-styles.md) , è possibile inviare il messaggio [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md) per modificare la lunghezza del dispositivo di scorrimento.

Per recuperare o impostare l'intervallo di selezione, inviare messaggi al TrackBar. Usare il [**messaggio \_ SETSEL TBM**](tbm-setsel.md) per impostare le posizioni di inizio e fine di una selezione. Per impostare solo la posizione iniziale o solo la posizione finale di una selezione, inviare un messaggio [**TBM \_ SETSELSTART**](tbm-setselstart.md) o [**TBM \_ seselend**](tbm-setselend.md) . Per recuperare le posizioni iniziali o finali di un intervallo di selezione, inviare un messaggio [**TBM \_ GETSELSTART**](tbm-getselstart.md) o [**TBM \_ getselend**](tbm-getselend.md) . Per cancellare un intervallo di selezione e ripristinare il valore di TrackBar nell'intervallo originale, inviare il messaggio [**\_ CLEARSEL TBM**](tbm-clearsel.md) .

> [!Note]  
> È responsabilità dell'applicazione assicurarsi che l'utente non possa selezionare valori non compresi nell'intervallo di selezione. Il controllo stesso non impedisce all'utente di spostarlo all'esterno dell'intervallo.

 

## <a name="trackbar-notification-messages"></a>Messaggi di notifica TrackBar

Un TrackBar notifica alla finestra padre le azioni dell'utente inviando al padre un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) . Un TrackBar con lo stile [**TBS \_ orizzontalmente**](trackbar-control-styles.md) invia messaggi **WM \_ HSCROLL** . Un TrackBar con lo stile di [**TBS \_ Vert**](trackbar-control-styles.md) invia messaggi **WM \_ VSCROLL** . La parola più bassa del parametro *wParam* di **WM \_ HSCROLL** o **WM \_ VSCROLL** contiene il codice di notifica. Per i \_ codici di notifica TB THUMBPOSITION e TB \_ THUMBTRACK, la parola più ordinata del parametro *wParam* specifica la posizione del dispositivo di scorrimento. Per tutti gli altri codici di notifica, la parola più ordinata è zero; inviare il messaggio [**TBM \_ GETPOS**](tbm-getpos.md) per determinare la posizione del dispositivo di scorrimento. Il parametro *lParam* è l'handle per l'oggetto TrackBar.

Il sistema invia i \_ \_ codici di notifica principali TB, TB LINEDOWN, TB \_ e TB \_ solo quando l'utente interagisce con un TrackBar usando la tastiera. I \_ codici di notifica TB THUMBPOSITION e TB \_ THUMBTRACK vengono inviati solo quando l'utente usa il mouse. I \_ codici di notifica TB ENDTRACK, TB \_ PGGIÙ e TB \_ PAGEUP vengono inviati in entrambi i casi. Nella tabella seguente sono elencati i codici di notifica TrackBar e gli eventi (codici chiave virtuali o eventi del mouse) che causano l'invio delle notifiche dei [**codici di chiave virtuale**](/windows/desktop/inputdev/virtual-key-codes).



| Codice di notifica | Motivo dell'invio                                                                                                                     |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| TB in \_ basso        | [**\_fine VK**](/windows/desktop/inputdev/virtual-key-codes)                                                                         |
| TB \_ ENDTRACK      | [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) (l'utente ha rilasciato una chiave che ha inviato un codice di chiave virtuale pertinente)                              |
| TB \_ LINEDOWN      | [**VK \_ DESTRO**](/windows/desktop/inputdev/virtual-key-codes) o [ **VK \_ giù**](/windows/desktop/inputdev/virtual-key-codes)     |
| \_lineup TB        | [**VK \_ SINISTRO**](/windows/desktop/inputdev/virtual-key-codes) o [ **VK \_**](/windows/desktop/inputdev/virtual-key-codes)              |
| TB \_ PGGIÙ      | [**VK \_ AVANTI**](/windows/desktop/inputdev/virtual-key-codes) (l'utente ha fatto clic sul canale sotto o a destra del dispositivo di scorrimento)   |
| TB \_ PAGEUP        | [**VK \_ PRIMA**](/windows/desktop/inputdev/virtual-key-codes) (l'utente ha fatto clic sul canale sopra o a sinistra del dispositivo di scorrimento) |
| TB \_ THUMBPOSITION | [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) dopo un \_ codice di notifica TB THUMBTRACK                                         |
| TB \_ THUMBTRACK    | Spostamento del dispositivo di scorrimento (l'utente ha trascinato il dispositivo di scorrimento)                                                                                   |
| TB \_ superiore           | [**\_casa VK**](/windows/desktop/inputdev/virtual-key-codes)                                                                      |



 

## <a name="default-trackbar-message-processing"></a>Elaborazione del messaggio TrackBar predefinita

In questa sezione viene descritta l'elaborazione dei messaggi della finestra eseguita da un TrackBar.



| Message                                              | Elaborazione eseguita                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CAPTURECHANGED WM**](/windows/desktop/inputdev/wm-capturechanged) | Termina il timer se ne è stato impostato uno durante l'elaborazione di [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) e invia il \_ codice di notifica THUMBPOSITION TB, se necessario. Invia sempre il codice di \_ notifica ENDTRACK TB.                                     |
| [**creazione di WM \_**](/windows/desktop/winmsg/wm-create)                   | Esegue un'inizializzazione aggiuntiva, ad esempio impostando le dimensioni della riga, le dimensioni della pagina e la frequenza dei segni di graduazione sui valori predefiniti.                                                                                                                                 |
| [**eliminazione di WM \_**](/windows/desktop/winmsg/wm-destroy)                 | Libera risorse.                                                                                                                                                                                                                                         |
| [**\_Abilitazione WM**](/windows/desktop/winmsg/wm-enable)                   | Ridisegna la finestra TrackBar.                                                                                                                                                                                                                            |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd)           | Cancella lo sfondo della finestra, usando il colore di sfondo corrente per il controllo TrackBar.                                                                                                                                                                       |
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)           | Restituisce il \_ valore WANTARROWS di DLGC.                                                                                                                                                                                                                      |
| [**KeyDown di WM \_**](/windows/desktop/inputdev/wm-keydown)               | Elabora i tasti di direzione e invia i \_ codici di notifica TB top, TB \_ Bottom, TB \_ PAGEUP, TB \_ PGGIÙ, TB \_ e TB \_ LINEDOWN, a seconda dei casi.                                                                                               |
| [**KEYUP di WM \_**](/windows/desktop/inputdev/wm-keyup)                   | Invia il \_ codice di notifica ENDTRACK TB se il tasto è uno dei tasti di direzione.                                                                                                                                                                       |
| [**\_KILLFOCUS WM**](/windows/desktop/inputdev/wm-killfocus)           | Ridisegna la finestra TrackBar.                                                                                                                                                                                                                            |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)       | Imposta lo stato attivo e l'acquisizione del mouse sul TrackBar. Quando necessario, imposta un timer che determina la velocità di spostamento del dispositivo di scorrimento verso il cursore del mouse quando l'utente preme il pulsante del mouse nella finestra.                                      |
| [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)           | Rilascia l'acquisizione del mouse e termina il timer se ne è stato impostato uno durante l'elaborazione di [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) . Invia il codice di \_ notifica THUMBPOSITION TB, se necessario. Invia sempre il codice di \_ notifica ENDTRACK TB. |
| [**MOUSEMOVE di WM \_**](/windows/desktop/inputdev/wm-mousemove)           | Spostare il dispositivo di scorrimento e inviare il \_ codice di notifica THUMBTRACK TB quando si tiene traccia del mouse (vedere [**WM \_ timer**](/windows/desktop/winmsg/wm-timer)).                                                                                                                          |
| [**\_disegno WM**](/windows/desktop/gdi/wm-paint)                        | Disegna il TrackBar. Se il parametro wParam è diverso da NULL, il controllo presuppone che il valore sia un HDC e i colori che usano tale contesto di dispositivo.                                                                                                             |
| [**\_stato attivo WM**](/windows/desktop/inputdev/wm-setfocus)             | Ridisegna la finestra TrackBar.                                                                                                                                                                                                                            |
| [**\_dimensioni WM**](/windows/desktop/winmsg/wm-size)                       | Imposta le dimensioni del TrackBar, rimuovendo il dispositivo di scorrimento se lo spazio disponibile non è sufficiente per visualizzarlo.                                                                                                                                                      |
| [**\_timer WM**](/windows/desktop/winmsg/wm-timer)                     | Recupera la posizione del mouse e aggiorna la posizione del dispositivo di scorrimento. Viene ricevuto solo quando l'utente trascina il dispositivo di scorrimento.                                                                                                                         |
| [**\_WININICHANGE WM**](/windows/desktop/winmsg/wm-wininichange)       | Inizializza le dimensioni del dispositivo di scorrimento.                                                                                                                                                                                                                           |



 

## <a name="trackbar-tooltips"></a>Descrizioni comandi di TrackBar

Un TrackBar creato con lo stile delle [**\_ descrizioni comandi di TBS**](trackbar-control-styles.md) dispone di un controllo ToolTip predefinito. La descrizione comando rimane visibile e visualizza il valore corrente quando l'utente trascina il dispositivo di scorrimento usando il mouse.

È possibile assegnare un nuovo controllo ToolTip a un TrackBar inviando il messaggio [**TBM \_ setooltips**](tbm-settooltips.md) . Per recuperare l'handle a un controllo ToolTip assegnato, usare il messaggio [**TBM \_ GetToolTips**](tbm-gettooltips.md) .

 

 