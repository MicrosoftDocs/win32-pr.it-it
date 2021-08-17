---
title: Informazioni sulle barre di scorrimento
description: Una finestra può visualizzare un oggetto dati, ad esempio un documento o una bitmap, più grande dell'area client della finestra.
ms.assetid: 9cb3afad-79ef-4817-950a-c8c1de39401b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93b3088df389753123e2a267ef3bc15eccb1b54626085ee90af7a20978107dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922373"
---
# <a name="about-scroll-bars"></a>Informazioni sulle barre di scorrimento

Una finestra può visualizzare un oggetto dati, ad esempio un documento o una bitmap, più grande dell'area client della finestra. Quando viene fornito con una barra di scorrimento, l'utente può scorrere un oggetto dati nell'area client per visualizzare le parti dell'oggetto che si estendono oltre i bordi della finestra.

Le barre di scorrimento devono essere incluse in qualsiasi finestra per cui il contenuto dell'area client si estende oltre i bordi della finestra. L'orientamento di una barra di scorrimento determina la direzione di scorrimento quando l'utente esegue la barra di scorrimento. Una barra di scorrimento orizzontale consente all'utente di scorrere il contenuto di una finestra verso sinistra o verso destra. Una barra di scorrimento verticale consente all'utente di scorrere il contenuto verso l'alto o verso il basso.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Parti di una barra di scorrimento](#parts-of-a-scroll-bar)
-   [Barre di scorrimento standard e controlli barra di scorrimento](#standard-scroll-bars-and-scroll-bar-controls)
-   [Posizione e intervallo di scorrimento della casella di scorrimento](#scroll-box-position-and-scrolling-range)
-   [Visibilità della barra di scorrimento](#scroll-bar-visibility)
-   [Richieste barra di scorrimento](#scroll-bar-requests)
-   [Interfaccia della tastiera per una barra di scorrimento](#keyboard-interface-for-a-scroll-bar)
-   [Scorrimento dell'area client](#scrolling-the-client-area)
-   [Metriche e colori della barra di scorrimento](#scroll-bar-colors-and-metrics)

## <a name="parts-of-a-scroll-bar"></a>Parti di una barra di scorrimento

Una barra di scorrimento è costituita da un'ombreggiatura con un pulsante *freccia* a ogni estremità e una casella di scorrimento (talvolta denominata casella di scorrimento) tra i pulsanti freccia. Una barra di scorrimento rappresenta la lunghezza o la larghezza complessiva di un oggetto dati nell'area client di una finestra. La casella di scorrimento rappresenta la parte dell'oggetto visibile nell'area client. La posizione della casella di scorrimento cambia ogni volta che l'utente scorre un oggetto dati per visualizzane una parte diversa. Il sistema regola anche le dimensioni della casella di scorrimento di una barra di scorrimento in modo da indicare quale parte dell'intero oggetto dati è attualmente visibile nella finestra. Se la maggior parte dell'oggetto è visibile, la casella di scorrimento occupa la maggior parte della barra di scorrimento. Analogamente, se è visibile solo una piccola parte dell'oggetto , la casella di scorrimento occupa una piccola parte della barra di scorrimento.

L'utente scorre il contenuto di una finestra facendo clic su uno dei pulsanti freccia, facendo clic sull'area nella barra di scorrimento ombreggiata oppure trascinando la casella di scorrimento. Quando l'utente fa clic su un pulsante freccia, l'applicazione scorre il contenuto di un'unità (in genere una singola riga o colonna). Quando l'utente fa clic su aree ombreggiate, l'applicazione scorre il contenuto di una finestra. La quantità di scorrimento che si verifica quando l'utente trascina la casella di scorrimento dipende dalla distanza da cui l'utente trascina la casella di scorrimento e dall'intervallo di scorrimento della barra di scorrimento. Per altre informazioni sull'intervallo di scorrimento, vedere Scroll Box Position (Posizione della casella di [scorrimento) e Scrolling Range (Intervallo di scorrimento).](#scroll-box-position-and-scrolling-range)

Lo screenshot seguente mostra un controllo Rich Edit con barre di scorrimento verticali e orizzontali, come potrebbero essere visualizzati in Windows Vista. La barra di scorrimento verticale è attualmente "hot" perché il puntatore del mouse era posizionato su di essa quando è stata visualizzata la schermata.

![Screenshot di un controllo Rich Edit con barre di scorrimento](images/sbvista.png)

## <a name="standard-scroll-bars-and-scroll-bar-controls"></a>Barre di scorrimento standard e controlli barra di scorrimento

Una barra di scorrimento viene inclusa in una finestra come barra di scorrimento standard o come controllo barra di scorrimento. Una barra di scorrimento standard si trova nell'area non client di una finestra. Viene creato con la finestra e visualizzato quando viene visualizzata. L'unico scopo di una barra di scorrimento standard è consentire all'utente di generare richieste di scorrimento per visualizzare l'intero contenuto dell'area client. È possibile includere una barra di scorrimento standard in una finestra specificando [**WS \_ HSCROLL,**](/windows/desktop/winmsg/window-styles) [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)o entrambi gli stili quando si crea la finestra. Lo **stile \_ HSCROLL WS** crea una barra di scorrimento orizzontale posizionata nella parte inferiore dell'area client. Lo **stile \_ VSCROLL WS** crea una barra di scorrimento verticale posizionata a destra dell'area client. I valori delle metriche di sistema \_ SM CXHSCROLL e SM CYHSCROLL definiscono la larghezza e l'altezza di una barra di scorrimento \_ orizzontale standard. I valori \_ SM CXVSCROLL e SM CYVSCROLL definiscono la larghezza e l'altezza di una barra di scorrimento \_ verticale standard. Una barra di scorrimento standard fa parte della finestra associata e pertanto non dispone di un handle di finestra proprio.

Un controllo barra di scorrimento è una finestra di controllo che appartiene alla classe della finestra SCROLLBAR. Viene visualizzato un controllo barra di scorrimento che funziona come una barra di scorrimento standard, ma è una finestra separata. Come finestra separata, un controllo barra di scorrimento assume lo stato attivo per l'input diretto. A differenza di una barra di scorrimento standard, un controllo barra di scorrimento ha anche un'interfaccia della tastiera incorporata.

È possibile usare tutti i controlli barra di scorrimento necessari in un'unica finestra. Quando si crea un controllo barra di scorrimento, è necessario specificare le dimensioni e la posizione della barra di scorrimento. Tuttavia, se la finestra di un controllo barra di scorrimento può essere ridimensionata, è necessario apportare modifiche alle dimensioni della barra di scorrimento ogni volta che le dimensioni della finestra cambiano.

Il vantaggio dell'uso di una barra di scorrimento standard è che il sistema crea la barra di scorrimento e ne imposta automaticamente le dimensioni e la posizione. Tuttavia, le barre di scorrimento standard sono talvolta troppo restrittive. Si supponga, ad esempio, di voler dividere un'area client in quadranti e di usare un set separato di barre di scorrimento per controllare il contenuto di ogni quadrante. Non è possibile usare le barre di scorrimento standard perché è possibile creare un solo set di barre di scorrimento per una determinata finestra. Usare invece i controlli barra di scorrimento, perché è possibile aggiungere il numero desiderato di controlli a una finestra.

Le applicazioni possono fornire controlli barra di scorrimento per scopi diversi da quello di scorrimento del contenuto di una finestra. Ad esempio, un'screen saver potrebbe fornire una barra di scorrimento per impostare la velocità di spostamento della grafica sullo schermo.

Un controllo barra di scorrimento può avere diversi stili che servono a controllare l'orientamento e la posizione della barra di scorrimento. È possibile specificare gli stili desiderati quando si chiama la [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un controllo barra di scorrimento. Alcuni stili creano un controllo barra di scorrimento che usa una larghezza o un'altezza predefinita. È tuttavia necessario specificare sempre le coordinate x e y e le altre dimensioni della barra di scorrimento.

Per una tabella degli stili dei controlli barra di scorrimento, vedere Stili del controllo Barra [di scorrimento.](scroll-bar-control-styles.md)

> [!Note]  
> Per usare gli stili di visualizzazione con le barre di scorrimento, un'applicazione deve includere un manifesto e chiamare [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) all'inizio del programma. Per informazioni sugli stili di visualizzazione, vedere [Stili di visualizzazione.](themes-overview.md) Per informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="scroll-box-position-and-scrolling-range"></a>Posizione e intervallo di scorrimento della casella di scorrimento

La posizione della casella di scorrimento è rappresentata come integer. è relativo all'estremità sinistra o superiore della barra di scorrimento, a seconda che la barra di scorrimento sia orizzontale o verticale. La posizione deve essere all'interno dei valori minimo e massimo dell'intervallo di scorrimento. Ad esempio, in una barra di scorrimento con un intervallo compreso tra 0 e 100, la posizione 50 si trova al centro, con le posizioni rimanenti distribuite equamente lungo la barra di scorrimento. L'intervallo iniziale dipende dalla barra di scorrimento. Le barre di scorrimento standard hanno un intervallo iniziale compreso tra 0 e 100. I controlli barra di scorrimento hanno un intervallo vuoto (i valori minimo e massimo sono pari a zero), a meno che al momento della creazione del controllo non venga specificato un intervallo esplicito. È possibile modificare l'intervallo in qualsiasi momento. È possibile usare la [**funzione SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) per impostare i valori di intervallo e la [**funzione GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) per recuperare i valori dell'intervallo corrente.

Un'applicazione regola in genere l'intervallo di scorrimento in valori interi pratici, semplificando la conversione della posizione della casella di scorrimento in un valore corrispondente all'oggetto dati da scorrere. Ad esempio, se un'applicazione deve visualizzare 260 righe di un file di testo in una finestra che può visualizzare solo 16 righe alla volta, l'intervallo della barra di scorrimento verticale può essere impostato su 1 e 244. Se la casella di scorrimento si trova nella posizione 1, la prima riga si trova nella parte superiore della finestra. Se la casella di scorrimento si trova nella posizione 244, l'ultima riga (riga 260) si trova nella parte inferiore della finestra. Se un'applicazione tenta di specificare un valore di posizione minore del valore minimo o maggiore del valore massimo, viene usato il valore dell'intervallo di scorrimento minimo o massimo.

È possibile impostare le dimensioni della pagina per una barra di scorrimento. Le *dimensioni della pagina* rappresentano il numero di unità dati che possono rientrare nell'area client della finestra proprietaria in base alle dimensioni correnti. Ad esempio, se l'area client può contenere 16 righe di testo, un'applicazione imposta le dimensioni della pagina su 16. Il sistema usa le dimensioni della pagina, insieme all'intervallo di scorrimento e alla lunghezza della barra di scorrimento, per impostare le dimensioni della casella di scorrimento. Ogni volta che una finestra contenente una barra di scorrimento viene ridimensionata, un'applicazione deve chiamare la [**funzione SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) per impostare le dimensioni della pagina. Un'applicazione può recuperare le dimensioni della pagina corrente chiamando la funzione [**GetScrollInfo di**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) invio.

Per stabilire una relazione utile tra l'intervallo della barra di scorrimento e l'oggetto dati, un'applicazione deve modificare l'intervallo ogni volta che le dimensioni dell'oggetto dati cambiano.

Quando l'utente sposta la casella di scorrimento in una barra di scorrimento, la barra di scorrimento segnala la posizione della casella di scorrimento come numero intero nell'intervallo di scorrimento. Se la posizione è il valore minimo, la casella di scorrimento si trova nella parte superiore di una barra di scorrimento verticale o all'estremità sinistra di una barra di scorrimento orizzontale. Se la posizione è il valore massimo, la casella di scorrimento si trova nella parte inferiore di una barra di scorrimento verticale o all'estremità destra di una barra di scorrimento orizzontale.

Il valore massimo che una barra di scorrimento può segnalare,ovvero la posizione massima di scorrimento, dipende dalle dimensioni della pagina. Se la barra di scorrimento ha una dimensione di pagina maggiore di uno, la posizione massima di scorrimento è minore del valore di intervallo massimo. È possibile usare la formula seguente per calcolare la posizione massima di scorrimento:


```
MaxScrollPos = MaxRangeValue - (PageSize - 1) 
```



Un'applicazione deve spostare la casella di scorrimento in una barra di scorrimento. Anche se l'utente effettua una richiesta di scorrimento in una barra di scorrimento, la barra di scorrimento non aggiorna automaticamente la posizione della casella di scorrimento. Passa invece la richiesta alla finestra padre, che deve scorrere i dati e aggiornare la posizione della casella di scorrimento. Un'applicazione usa la [**funzione SetScrollInfo per**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) aggiornare la posizione della casella di scorrimento. In caso contrario, usa la [**funzione SetScrollPos.**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) Poiché controlla lo spostamento della casella di scorrimento, l'applicazione può spostare la casella di scorrimento in incrementi ottimali per i dati da scorrere.

## <a name="scroll-bar-visibility"></a>Visibilità della barra di scorrimento

Il sistema nasconde e disabilita una barra di scorrimento standard quando vengono specificati valori minimi e massimi uguali. Il sistema nasconde e disabilita anche una barra di scorrimento standard se si specificano dimensioni di pagina che includono l'intero intervallo di scorrimento della barra di scorrimento. Questo è il modo per nascondere temporaneamente una barra di scorrimento quando non è necessaria per il contenuto dell'area client. Non è necessario eseguire richieste di scorrimento attraverso la barra di scorrimento quando è nascosta. Il sistema abilita la barra di scorrimento e la visualizza nuovamente quando si impostano i valori minimo e massimo su valori diversi e quando le dimensioni della pagina non includono l'intero intervallo di scorrimento. La [**funzione ShowScrollBar**](/windows/desktop/api/Winuser/nf-winuser-showscrollbar) può essere usata anche per nascondere o visualizzare una barra di scorrimento. Non influisce sull'intervallo, sulle dimensioni della pagina o sulla posizione della casella di scorrimento della barra di scorrimento.

La [**funzione EnableScrollBar**](/windows/desktop/api/Winuser/nf-winuser-enablescrollbar) può essere usata per disabilitare una o entrambe le frecce di una barra di scorrimento. Un'applicazione visualizza le frecce disabilitate in grigio e non risponde all'input dell'utente.

## <a name="scroll-bar-requests"></a>Richieste della barra di scorrimento

L'utente effettua richieste di scorrimento facendo clic su varie parti di una barra di scorrimento. Il sistema invia la richiesta alla finestra specificata sotto forma di messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL.**](wm-vscroll.md) Una barra di scorrimento orizzontale invia **il messaggio \_ WM HSCROLL.** Una barra di scorrimento verticale invia il **messaggio WM \_ VSCROLL.** Ogni messaggio include un codice di richiesta che corrisponde all'azione dell'utente, all'handle della barra di scorrimento (solo controlli barra di scorrimento) e, in alcuni casi, alla posizione della casella di scorrimento.

Il diagramma seguente mostra il codice della richiesta generato dall'utente quando fa clic su varie parti di una barra di scorrimento.

![diagramma che mostra i codici di richiesta associati a ogni area su due barre di scorrimento](images/csscr-02.png)

I valori SB \_ specificano l'azione eseguita dall'utente. Un'applicazione esamina i codici che accompagnano i [**messaggi WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) e quindi esegue l'operazione di scorrimento appropriata. Nella tabella seguente l'azione dell'utente viene specificata per ogni valore, seguita dalla risposta dell'applicazione. In ogni caso, un'unità viene definita dall'applicazione in base alle esigenze dei dati. Ad esempio, l'unità tipica per lo scorrimento verticale del testo è una riga di testo.



| Richiesta           | Azione                                                                               | Risposta                                                                                                                                                                                                                                                                                                                         |
|-------------------|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SB \_ LINEUP        | L'utente fa clic sulla freccia di scorrimento superiore.                                                | Decrementa la posizione della casella di scorrimento. scorre verso la parte superiore dei dati di un'unità.                                                                                                                                                                                                                                              |
| SB \_ LINEDOWN      | L'utente fa clic sulla freccia di scorrimento inferiore.                                             | Incrementa la posizione della casella di scorrimento. scorre verso la parte inferiore dei dati di un'unità.                                                                                                                                                                                                                                           |
| SB \_ LINELEFT      | L'utente fa clic sulla freccia di scorrimento a sinistra.                                               | Decrementa la posizione della casella di scorrimento. scorre verso l'estremità sinistra dei dati di un'unità.                                                                                                                                                                                                                                         |
| SB \_ LINERIGHT     | L'utente fa clic sulla freccia di scorrimento a destra.                                              | Incrementa la posizione della casella di scorrimento. scorre verso l'estremità destra dei dati di un'unità.                                                                                                                                                                                                                                        |
| SB \_ PAGEUP        | L'utente fa clic sull'albero della barra di scorrimento sopra la casella di scorrimento.                           | Decrementa la posizione della casella di scorrimento in base al numero di unità dati nella finestra. scorre verso la parte superiore dei dati dello stesso numero di unità.                                                                                                                                                                                    |
| SB \_ PAGEDOWN      | L'utente fa clic sull'albero della barra di scorrimento sotto la casella di scorrimento.                           | Incrementa la posizione della casella di scorrimento del numero di unità dati nella finestra. scorre verso la parte inferiore dei dati dello stesso numero di unità.                                                                                                                                                                                 |
| SB \_ PAGELEFT      | L'utente fa clic sull'albero della barra di scorrimento a sinistra della casella di scorrimento.                  | Decrementa la posizione della casella di scorrimento in base al numero di unità dati nella finestra. scorre verso l'estremità sinistra dei dati dello stesso numero di unità.                                                                                                                                                                               |
| SB \_ PAGERIGHT     | L'utente fa clic sull'albero della barra di scorrimento a destra della casella di scorrimento.                 | Incrementa la posizione della casella di scorrimento del numero di unità dati nella finestra. scorre verso l'estremità destra dei dati dello stesso numero di unità.                                                                                                                                                                              |
| SB \_ THUMBPOSITION | L'utente rilascia la casella di scorrimento dopo il trascinamento.                                  | Imposta la casella di scorrimento sulla posizione specificata nel messaggio. scorre i dati dello stesso numero di unità spostate dalla casella di scorrimento.                                                                                                                                                                                             |
| SB \_ THUMBTRACK    | L'utente trascina la casella di scorrimento.                                                       | Imposta la casella di scorrimento sulla posizione specificata nel messaggio e scorre i dati dello stesso numero di unità spostate dalla casella di scorrimento per le applicazioni che disegnano rapidamente i dati. Le applicazioni che non possono disegnare rapidamente i dati devono attendere il codice di richiesta SB THUMBPOSITION prima di spostare la casella di scorrimento \_ e scorrere i dati. |
| SB \_ ENDSCROLL     | L'utente rilascia il mouse dopo averlo premuto su una freccia o nell'albero della barra di scorrimento. | Non è necessaria alcuna risposta.                                                                                                                                                                                                                                                                                                           |



 

Una barra di scorrimento genera il codice di richiesta SB THUMBPOSITION e SB THUMBTRACK quando l'utente fa clic e \_ trascina la casella di \_ scorrimento. Un'applicazione deve essere programmata per elaborare il codice di richiesta SB THUMBTRACK o \_ SB \_ THUMBPOSITION.

Il codice di richiesta \_ SB THUMBPOSITION si verifica quando l'utente rilascia il pulsante del mouse dopo aver fatto clic sulla casella di scorrimento. Un'applicazione che elabora questo messaggio esegue l'operazione di scorrimento dopo che l'utente ha trascinato la casella di scorrimento nella posizione desiderata e rilasciato il pulsante del mouse.

Il codice della richiesta THUMBTRACK SB \_ si verifica quando l'utente trascina la casella di scorrimento. Se un'applicazione elabora i codici di richiesta SB THUMBTRACK, può scorrere il contenuto di una finestra mentre l'utente \_ trascina la casella di scorrimento. Tuttavia, una barra di scorrimento può generare molti codici di richiesta SB THUMBTRACK in un breve periodo, pertanto un'applicazione deve elaborare questi codici di richiesta solo se è in grado di ridisegnare rapidamente il contenuto \_ della finestra.

## <a name="keyboard-interface-for-a-scroll-bar"></a>Interfaccia della tastiera per una barra di scorrimento

Un controllo barra di scorrimento fornisce un'interfaccia della tastiera incorporata che consente all'utente di eseguire richieste di scorrimento tramite la tastiera. una barra di scorrimento standard non lo fa. Quando un controllo barra di scorrimento ha lo stato attivo della tastiera, invia messaggi [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) alla finestra padre quando l'utente preme i tasti di direzione. Il codice della richiesta viene inviato con ogni messaggio corrispondente al tasto di direzione premuto dall'utente. Di seguito sono riportati i tasti di direzione e i codici di richiesta corrispondenti.



| Tasto di direzione | Richiedere il codice                  |
|-----------|-------------------------------|
| DOWN      | SB \_ LINEDOWN o SB \_ LINERIGHT |
| FINE       | SB \_ BOTTOM                    |
| HOME      | SB \_ TOP                       |
| LEFT      | LINEUP SB \_ o SB \_ LINELEFT    |
| PGDN      | SB \_ PAGEDOWN o SB \_ PAGERIGHT |
| Pgup      | SB \_ PAGEUP o SB \_ PAGELEFT    |
| RIGHT     | SB \_ LINEDOWN o SB \_ LINERIGHT |
| UP        | LINEUP SB \_ o SB \_ LINELEFT    |



 

 

> [!Note]  
> L'interfaccia della tastiera di un controllo barra di scorrimento invia i codici di richiesta SB \_ TOP e SB \_ BOTTOM. Il codice della richiesta SB \_ TOP indica che l'utente ha raggiunto il primo valore dell'intervallo di scorrimento. Un'applicazione scorre il contenuto della finestra verso il basso in modo che la parte superiore dell'oggetto dati sia visibile. Il codice di richiesta SB \_ BOTTOM indica che l'utente ha raggiunto il valore inferiore dell'intervallo di scorrimento. Se un'applicazione elabora il codice della richiesta SB BOTTOM, scorre il contenuto della finestra verso l'alto in modo che la parte inferiore \_ dell'oggetto dati sia visibile.

 

Se si desidera un'interfaccia della tastiera per una barra di scorrimento standard, è possibile crearne una elaborando il messaggio [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) nella routine della finestra e quindi eseguendo l'azione di scorrimento appropriata in base al codice del tasto virtuale che accompagna il messaggio. Per informazioni su come creare un'interfaccia della tastiera per una barra di scorrimento, vedere Creazione di un'interfaccia della tastiera [per una barra di scorrimento standard.](using-scroll-bars.md)

## <a name="scrolling-the-client-area"></a>Scorrimento dell'area client

Il modo più semplice per scorrere il contenuto di un'area client è cancellare e quindi ridisegnarlo. Questo è il metodo che un'applicazione può usare con i codici di richiesta \_ SB PAGEUP, SB PAGEDOWN e SB TOP, che in genere richiedono \_ \_ contenuto completamente nuovo.

Per alcuni codici di richiesta, ad esempio SB LINEUP e SB LINEDOWN, non è necessario cancellare tutto il contenuto, perché alcuni rimangono visibili dopo lo \_ \_ scorrimento. La [**funzione ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) mantiene una parte del contenuto dell'area client, sposta la parte mantenuta in una quantità specificata e quindi prepara il resto dell'area client per disegnare nuove informazioni. **ScrollWindowEx usa** la [**funzione BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) per spostare una parte specifica dell'oggetto dati in una nuova posizione all'interno dell'area client. Qualsiasi parte individuata dell'area client (tutto ciò che non viene conservato) viene invalidata, cancellata e disegnata quando si verifica il successivo [**messaggio WM \_ PAINT.**](/windows/desktop/gdi/wm-paint)

La [**funzione ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) può essere usata per escludere una parte dell'area client dall'operazione di scorrimento. In questo modo gli elementi con posizioni fisse, ad esempio le finestre figlio, non si spostano all'interno dell'area client. Invalida automaticamente la parte dell'area client che deve ricevere le nuove informazioni, quindi l'applicazione non deve calcolare le proprie aree di ritaglio. Per altre informazioni sul ritaglio, vedere [Ritaglio.](/windows/desktop/gdi/clipping)

In genere un'applicazione scorre il contenuto di una finestra nella direzione opposta a quella indicata dalla barra di scorrimento. Ad esempio, quando l'utente fa clic sull'albero della barra di scorrimento nell'area sotto la casella di scorrimento, un'applicazione scorre l'oggetto nella finestra verso l'alto per visualizzare una parte dell'oggetto che si trova sotto la parte visibile.

È anche possibile scorrere un'area rettangolare usando la [**funzione ScrollDC.**](/windows/desktop/api/Winuser/nf-winuser-scrolldc)

## <a name="scroll-bar-colors-and-metrics"></a>Colori e metriche della barra di scorrimento

Il valore del colore definito dal sistema, COLOR \_ SCROLLBAR, controlla il colore all'interno di un albero della barra di scorrimento. Usare la [**funzione GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) per determinare il colore dell'albero della barra di scorrimento e la [**funzione SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) per impostare il colore dell'albero della barra di scorrimento. Si noti, tuttavia, che questa modifica del colore influisce su tutte le barre di scorrimento nel sistema.

È possibile ottenere le dimensioni delle bitmap utilizzate dal sistema nelle barre di scorrimento standard chiamando la [**funzione GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Di seguito sono riportati i valori delle metriche di sistema associati alle barre di scorrimento.



| Metrica di sistema | Descrizione                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| SM \_ CXHSCROLL | Larghezza della bitmap a freccia sulla barra di scorrimento orizzontale                                                                             |
| SM \_ CXHTHUMB  | Larghezza della casella di scorrimento sulla barra di scorrimento orizzontale. Questo valore recupera la larghezza di una barra di scorrimento con dimensioni di pagina pari a zero.    |
| SM \_ CXVSCROLL | Larghezza della bitmap a freccia sulla barra di scorrimento verticale                                                                               |
| SM \_ CYHSCROLL | Altezza della bitmap della freccia sulla barra di scorrimento orizzontale                                                                            |
| SM \_ CYVSCROLL | Altezza della bitmap della freccia sulla barra di scorrimento verticale                                                                              |
| SM \_ CYVTHUMB  | Altezza della casella di scorrimento sulla barra di scorrimento verticale. Questo valore recupera l'altezza di una barra di scorrimento con dimensioni di pagina pari a zero. |



 

 

 
