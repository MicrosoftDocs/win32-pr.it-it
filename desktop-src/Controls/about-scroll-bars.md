---
title: Informazioni sulle barre di scorrimento
description: Una finestra può visualizzare un oggetto dati, ad esempio un documento o una bitmap, più grande dell'area client della finestra.
ms.assetid: 9cb3afad-79ef-4817-950a-c8c1de39401b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d410e98ea1fe722d6dc1c4869010df30f99bddb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047388"
---
# <a name="about-scroll-bars"></a>Informazioni sulle barre di scorrimento

Una finestra può visualizzare un oggetto dati, ad esempio un documento o una bitmap, più grande dell'area client della finestra. Quando viene fornito con una barra di scorrimento, l'utente può scorrere un oggetto dati nell'area client per visualizzare le parti dell'oggetto che si estendono oltre i bordi della finestra.

Le barre di scorrimento devono essere incluse in qualsiasi finestra per cui il contenuto dell'area client si estende oltre i bordi della finestra. L'orientamento di una barra di scorrimento determina la direzione in cui lo scorrimento si verifica quando l'utente esegue la barra di scorrimento. Una barra di scorrimento orizzontale consente all'utente di scorrere il contenuto di una finestra verso sinistra o verso destra. Una barra di scorrimento verticale consente all'utente di scorrere il contenuto verso l'alto o verso il basso.

In questa sezione vengono descritti gli argomenti seguenti.

-   [Parti di una barra di scorrimento](#parts-of-a-scroll-bar)
-   [Barre di scorrimento standard e controlli barra di scorrimento](#standard-scroll-bars-and-scroll-bar-controls)
-   [Posizione della casella di scorrimento e intervallo di scorrimento](#scroll-box-position-and-scrolling-range)
-   [Visibilità della barra di scorrimento](#scroll-bar-visibility)
-   [Richieste barra di scorrimento](#scroll-bar-requests)
-   [Interfaccia della tastiera per una barra di scorrimento](#keyboard-interface-for-a-scroll-bar)
-   [Scorrimento dell'area client](#scrolling-the-client-area)
-   [Colori e metriche della barra di scorrimento](#scroll-bar-colors-and-metrics)

## <a name="parts-of-a-scroll-bar"></a>Parti di una barra di scorrimento

Una barra di scorrimento è costituita da un albero ombreggiato con un pulsante freccia a ogni estremità e una *casella di scorrimento* (talvolta denominata Thumb) tra i pulsanti freccia. Una barra di scorrimento rappresenta la lunghezza o la larghezza complessiva di un oggetto dati nell'area client di una finestra. la casella di scorrimento rappresenta la parte dell'oggetto visibile nell'area client. La posizione della casella di scorrimento cambia ogni volta che l'utente scorre un oggetto dati per visualizzarne una parte diversa. Il sistema regola anche le dimensioni della casella di scorrimento di una barra di scorrimento in modo che indichi la parte dell'intero oggetto dati attualmente visibile nella finestra. Se la maggior parte dell'oggetto è visibile, la casella di scorrimento occupa la maggior parte dell'albero della barra di scorrimento. Analogamente, se è visibile solo una piccola parte dell'oggetto, la casella di scorrimento occupa una piccola parte dell'albero della barra di scorrimento.

L'utente scorre il contenuto di una finestra facendo clic su uno dei pulsanti freccia, facendo clic sull'area nell'albero della barra di scorrimento ombreggiata o trascinando la casella di scorrimento. Quando l'utente fa clic su un pulsante freccia, l'applicazione scorre il contenuto di un'unità (in genere una singola riga o colonna). Quando l'utente fa clic sulle aree ombreggiate, l'applicazione scorre il contenuto di una finestra. La quantità di scorrimento che si verifica quando l'utente trascina la casella di scorrimento dipende dalla distanza con cui l'utente trascina la casella di scorrimento e dall'intervallo di scorrimento della barra di scorrimento. Per ulteriori informazioni sull'intervallo di scorrimento, vedere [posizione della casella di scorrimento e intervallo di scorrimento](#scroll-box-position-and-scrolling-range).

Lo screenshot seguente mostra un controllo Rich Edit con barre di scorrimento verticali e orizzontali, come potrebbero apparire in Windows Vista. La barra di scorrimento verticale è attualmente "attiva" perché il puntatore del mouse è posizionato su di esso quando è stata eseguita la cattura dello schermo.

![Screenshot di un controllo Rich Edit con barre di scorrimento](images/sbvista.png)

## <a name="standard-scroll-bars-and-scroll-bar-controls"></a>Barre di scorrimento standard e controlli barra di scorrimento

Una barra di scorrimento è inclusa in una finestra come barra di scorrimento standard o come controllo barra di scorrimento. Una barra di scorrimento standard si trova nell'area non client di una finestra. Viene creata con la finestra e visualizzata quando viene visualizzata la finestra. L'unico scopo di una barra di scorrimento standard è quello di consentire all'utente di generare richieste di scorrimento per visualizzare l'intero contenuto dell'area client. È possibile includere una barra di scorrimento standard in una finestra specificando [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)o entrambi gli stili quando si crea la finestra. Lo stile **WS \_ HSCROLL** crea una barra di scorrimento orizzontale posizionata nella parte inferiore dell'area client. Lo stile **WS \_ VSCROLL** crea una barra di scorrimento verticale posizionata a destra dell'area client. I \_ valori delle metriche di sistema SM CXHSCROLL e SM \_ CYHSCROLL definiscono la larghezza e l'altezza di una barra di scorrimento orizzontale standard. I \_ valori SM CXVSCROLL e SM \_ CYVSCROLL definiscono la larghezza e l'altezza di una barra di scorrimento verticale standard. Una barra di scorrimento standard fa parte della finestra associata e pertanto non dispone di un handle di finestra.

Un controllo barra di scorrimento è una finestra di controllo che appartiene alla classe della finestra della barra di scorrimento. Viene visualizzato un controllo barra di scorrimento che funziona come una barra di scorrimento standard, ma è una finestra separata. Come finestra separata, un controllo barra di scorrimento accetta lo stato attivo per l'input diretto. Diversamente da una barra di scorrimento standard, un controllo barra di scorrimento dispone anche di un'interfaccia di tastiera incorporata.

È possibile utilizzare tutti i controlli della barra di scorrimento necessari in una singola finestra. Quando si crea un controllo barra di scorrimento, è necessario specificare le dimensioni e la posizione della barra di scorrimento. Tuttavia, se la finestra di un controllo barra di scorrimento può essere ridimensionata, le modifiche alle dimensioni della barra di scorrimento devono essere eseguite ogni volta che viene modificata la dimensione della finestra.

Il vantaggio dell'utilizzo di una barra di scorrimento standard consiste nel fatto che il sistema crea la barra di scorrimento e ne imposta automaticamente le dimensioni e la posizione. Tuttavia, le barre di scorrimento standard sono talvolta troppo restrittive. Si supponga, ad esempio, di voler dividere un'area client in quadranti e utilizzare un set separato di barre di scorrimento per controllare il contenuto di ciascun quadrante. Non è possibile usare le barre di scorrimento standard perché è possibile creare solo un set di barre di scorrimento per una determinata finestra. Utilizzare invece i controlli della barra di scorrimento, in quanto è possibile aggiungerli a una finestra nel modo desiderato.

Le applicazioni possono fornire controlli barra di scorrimento per scopi diversi dallo scorrimento del contenuto di una finestra. Ad esempio, un'applicazione screen saver potrebbe fornire una barra di scorrimento per impostare la velocità di spostamento della grafica sullo schermo.

Un controllo barra di scorrimento può avere diversi stili che servono a controllare l'orientamento e la posizione della barra di scorrimento. Si specificano gli stili desiderati quando si chiama la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un controllo barra di scorrimento. Alcuni stili creano un controllo barra di scorrimento che usa una larghezza o un'altezza predefinita. Tuttavia, è necessario specificare sempre le coordinate x e y e le altre dimensioni della barra di scorrimento.

Per una tabella degli stili del controllo barra di scorrimento, vedere [stili di controllo barra di scorrimento](scroll-bar-control-styles.md).

> [!Note]  
> Per usare gli stili di visualizzazione con le barre di scorrimento, un'applicazione deve includere un manifesto e deve chiamare [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) all'inizio del programma. Per informazioni sugli stili di visualizzazione, vedere [stili di visualizzazione](themes-overview.md). Per informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="scroll-box-position-and-scrolling-range"></a>Posizione della casella di scorrimento e intervallo di scorrimento

La posizione della casella di scorrimento è rappresentata come numero intero. è relativo al lato sinistro o superiore della barra di scorrimento, a seconda se la barra di scorrimento è orizzontale o verticale. La posizione deve essere compresa tra i valori minimo e massimo dell'intervallo di scorrimento. Ad esempio, in una barra di scorrimento con un intervallo compreso tra 0 e 100, la posizione 50 si trova al centro, con le posizioni rimanenti distribuite equamente lungo la barra di scorrimento. L'intervallo iniziale dipende dalla barra di scorrimento. Le barre di scorrimento standard hanno un intervallo iniziale compreso tra 0 e 100. i controlli barra di scorrimento hanno un intervallo vuoto (i valori minimo e massimo sono pari a zero), a meno che non si fornisca un intervallo esplicito al momento della creazione del controllo. È possibile modificare l'intervallo in qualsiasi momento. È possibile usare la funzione [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) per impostare i valori di intervallo e la funzione [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) per recuperare i valori di intervallo correnti.

Un'applicazione in genere regola l'intervallo di scorrimento in numeri interi pratici, semplificando la conversione della posizione della casella di scorrimento in un valore corrispondente all'oggetto dati da scorrere. Se, ad esempio, un'applicazione deve visualizzare 260 righe di un file di testo in una finestra che può mostrare solo 16 righe alla volta, l'intervallo della barra di scorrimento verticale può essere impostato su 1 e 244. Se la casella di scorrimento si trova nella posizione 1, la prima riga si troverà nella parte superiore della finestra. Se la casella di scorrimento si trova nella posizione 244, l'ultima riga (riga 260) si troverà nella parte inferiore della finestra. Se un'applicazione tenta di specificare un valore di posizione minore del valore minimo o superiore al valore massimo, viene invece utilizzato il valore di intervallo di scorrimento minimo o massimo.

È possibile impostare le dimensioni di pagina per una barra di scorrimento. Le *dimensioni della pagina* rappresentano il numero di unità dati che possono essere riportate nell'area client della finestra proprietaria in base alle dimensioni correnti. Se, ad esempio, l'area client può ospitare 16 righe di testo, un'applicazione imposterà le dimensioni della pagina su 16. Il sistema usa le dimensioni della pagina, insieme all'intervallo di scorrimento e alla lunghezza dell'albero della barra di scorrimento, per impostare le dimensioni della casella di scorrimento. Ogni volta che una finestra contenente una barra di scorrimento viene ridimensionata, un'applicazione deve chiamare la funzione [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) per impostare le dimensioni della pagina. Un'applicazione può recuperare le dimensioni correnti della pagina chiamando la funzione [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) di invio.

Per stabilire una relazione utile tra l'intervallo della barra di scorrimento e l'oggetto dati, un'applicazione deve regolare l'intervallo ogni volta che vengono modificate le dimensioni dell'oggetto dati.

Quando l'utente sposta la casella di scorrimento in una barra di scorrimento, la barra di scorrimento segnala la posizione della casella di scorrimento sotto forma di numero intero nell'intervallo di scorrimento. Se la posizione è il valore minimo, la casella di scorrimento si trova nella parte superiore di una barra di scorrimento verticale o all'estremità sinistra di una barra di scorrimento orizzontale. Se la posizione è il valore massimo, la casella di scorrimento si trova nella parte inferiore di una barra di scorrimento verticale o all'estremità destra di una barra di scorrimento orizzontale.

Il valore massimo che una barra di scorrimento può segnalare, ovvero la posizione di scorrimento massima, dipende dalle dimensioni della pagina. Se la barra di scorrimento ha una dimensione della pagina maggiore di uno, la posizione di scorrimento massima è inferiore al valore di intervallo massimo. È possibile utilizzare la formula seguente per calcolare la posizione di scorrimento massima:


```
MaxScrollPos = MaxRangeValue - (PageSize - 1) 
```



Un'applicazione deve spostare la casella di scorrimento in una barra di scorrimento. Anche se l'utente effettua una richiesta di scorrimento in una barra di scorrimento, la barra di scorrimento non aggiorna automaticamente la posizione della casella di scorrimento. Passa invece la richiesta alla finestra padre, che deve scorrere i dati e aggiornare la posizione della casella di scorrimento. Un'applicazione usa la funzione [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) per aggiornare la posizione della casella di scorrimento; in caso contrario, viene utilizzata la funzione [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) . Poiché controlla lo spostamento della casella di scorrimento, l'applicazione può spostare la casella di scorrimento in incrementi che funzionano meglio per i dati da scorrere.

## <a name="scroll-bar-visibility"></a>Visibilità della barra di scorrimento

Il sistema nasconde e Disabilita una barra di scorrimento standard quando si specificano valori minimi e massimi uguali. Il sistema nasconde inoltre e Disabilita una barra di scorrimento standard se si specificano le dimensioni di pagina che includono l'intero intervallo di scorrimento della barra di scorrimento. Questo è il modo per nascondere temporaneamente una barra di scorrimento quando non è necessaria per il contenuto dell'area client. Non è necessario effettuare lo scorrimento delle richieste attraverso la barra di scorrimento quando viene nascosta. Il sistema Abilita la barra di scorrimento e la Mostra nuovamente quando si impostano i valori minimo e massimo su valori diversi o quando le dimensioni della pagina non includono l'intero intervallo di scorrimento. La funzione [**ShowScrollBar**](/windows/desktop/api/Winuser/nf-winuser-showscrollbar) può essere usata anche per nascondere o visualizzare una barra di scorrimento. Non influisce sull'intervallo della barra di scorrimento, sulle dimensioni della pagina o sulla posizione della casella di scorrimento.

La funzione [**EnableScrollBar**](/windows/desktop/api/Winuser/nf-winuser-enablescrollbar) può essere usata per disabilitare una o entrambe le frecce di una barra di scorrimento. Un'applicazione Visualizza le frecce disabilitate in grigio e non risponde all'input dell'utente.

## <a name="scroll-bar-requests"></a>Richieste barra di scorrimento

L'utente esegue lo scorrimento delle richieste facendo clic su varie parti di una barra di scorrimento. Il sistema invia la richiesta alla finestra specificata sotto forma di un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) . Una barra di scorrimento orizzontale invia il messaggio **WM \_ HSCROLL** . una barra di scorrimento verticale invia il messaggio **WM \_ VSCROLL** . Ogni messaggio include un codice di richiesta che corrisponde all'azione dell'utente, all'handle per la barra di scorrimento (solo controlli barra di scorrimento) e, in alcuni casi, alla posizione della casella di scorrimento.

Il diagramma seguente mostra il codice di richiesta generato dall'utente quando si fa clic su varie parti di una barra di scorrimento.

![diagramma che mostra i codici di richiesta associati a ogni area su due barre di scorrimento](images/csscr-02.png)

I \_ valori SB specificano l'azione eseguita dall'utente. Un'applicazione esamina i codici che accompagnano i messaggi [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) e quindi esegue l'operazione di scorrimento appropriata. Nella tabella seguente viene specificata l'azione dell'utente per ogni valore, seguita dalla risposta dell'applicazione. In ogni caso, un'unità viene definita dall'applicazione nel modo appropriato per i dati. Ad esempio, l'unità tipica per lo scorrimento verticale del testo è una riga di testo.



| Richiesta           | Azione                                                                               | Risposta                                                                                                                                                                                                                                                                                                                         |
|-------------------|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_lineup SB        | L'utente fa clic sulla freccia in alto a scorrimento.                                                | Decrementa la posizione della casella di scorrimento; scorre verso la parte superiore dei dati di un'unità.                                                                                                                                                                                                                                              |
| \_LINEDOWN SB      | L'utente fa clic sulla freccia in basso a scorrimento.                                             | Incrementa la posizione della casella di scorrimento; scorre verso la parte inferiore dei dati di un'unità.                                                                                                                                                                                                                                           |
| \_LINELEFT SB      | L'utente fa clic sulla freccia di scorrimento a sinistra.                                               | Decrementa la posizione della casella di scorrimento; scorre verso l'estremità sinistra dei dati di un'unità.                                                                                                                                                                                                                                         |
| \_LINERIGHT SB     | L'utente fa clic sulla freccia di scorrimento a destra.                                              | Incrementa la posizione della casella di scorrimento; scorre verso l'estremità destra dei dati di un'unità.                                                                                                                                                                                                                                        |
| \_PAGEUP SB        | L'utente fa clic sull'albero della barra di scorrimento sopra la casella di scorrimento.                           | Decrementa la posizione della casella di scorrimento per il numero di unità dati nella finestra; scorre verso la parte superiore dei dati in base allo stesso numero di unità.                                                                                                                                                                                    |
| \_PGGIÙ SB      | L'utente fa clic sull'albero della barra di scorrimento sotto la casella di scorrimento.                           | Incrementa la posizione della casella di scorrimento per il numero di unità dati nella finestra; scorre verso la parte inferiore dei dati in base allo stesso numero di unità.                                                                                                                                                                                 |
| \_PAGELEFT SB      | L'utente fa clic sull'albero della barra di scorrimento a sinistra della casella di scorrimento.                  | Decrementa la posizione della casella di scorrimento per il numero di unità dati nella finestra; scorre verso l'estremità sinistra dei dati per lo stesso numero di unità.                                                                                                                                                                               |
| \_PAGERIGHT SB     | L'utente fa clic sull'albero della barra di scorrimento a destra della casella di scorrimento.                 | Incrementa la posizione della casella di scorrimento per il numero di unità dati nella finestra; scorre verso l'estremità destra dei dati per lo stesso numero di unità.                                                                                                                                                                              |
| \_THUMBPOSITION SB | L'utente rilascia la casella di scorrimento dopo averla trascinata.                                  | Imposta la casella di scorrimento sulla posizione specificata nel messaggio. scorre i dati in base allo stesso numero di unità spostate dalla casella di scorrimento.                                                                                                                                                                                             |
| \_THUMBTRACK SB    | L'utente trascina la casella di scorrimento.                                                       | Imposta la casella di scorrimento sulla posizione specificata nel messaggio e scorre i dati per lo stesso numero di unità che la casella di scorrimento è stata spostata per le applicazioni che consentono di creare rapidamente i dati. Le applicazioni che non possono creare dati rapidamente devono attendere il \_ codice della richiesta THUMBPOSITION SB prima di spostare la casella di scorrimento e scorrere i dati. |
| \_ENDSCROLL SB     | L'utente rilascia il mouse dopo averlo tenuto su una freccia o sull'albero della barra di scorrimento. | Non è necessaria alcuna risposta.                                                                                                                                                                                                                                                                                                           |



 

Una barra di scorrimento genera \_ \_ il codice della richiesta SB THUMBPOSITION e SB THUMBTRACK quando l'utente fa clic e trascina la casella di scorrimento. Un'applicazione deve essere programmata per elaborare il \_ codice della richiesta SB THUMBTRACK o SB \_ THUMBPOSITION.

Il \_ codice di richiesta SB THUMBPOSITION si verifica quando l'utente rilascia il pulsante del mouse dopo aver fatto clic sulla casella di scorrimento. Un'applicazione che elabora questo messaggio esegue l'operazione di scorrimento dopo che l'utente ha trascinato la casella di scorrimento nella posizione desiderata e rilasciato il pulsante del mouse.

Il \_ codice di richiesta THUMBTRACK SB si verifica quando l'utente trascina la casella di scorrimento. Se un'applicazione elabora i \_ codici di richiesta SB THUMBTRACK, può scorrere il contenuto di una finestra quando l'utente trascina la casella di scorrimento. Tuttavia, una barra di scorrimento può generare molti \_ codice di richiesta THUMBTRACK SB in un breve periodo di tempo, quindi un'applicazione deve elaborare questi codici di richiesta solo se può ridisegnare rapidamente il contenuto della finestra.

## <a name="keyboard-interface-for-a-scroll-bar"></a>Interfaccia della tastiera per una barra di scorrimento

Un controllo barra di scorrimento fornisce un'interfaccia di tastiera integrata che consente all'utente di emettere richieste di scorrimento tramite la tastiera. non è presente una barra di scorrimento standard. Quando un controllo barra di scorrimento dispone dello stato attivo della tastiera, invia i messaggi [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) alla finestra padre quando l'utente preme i tasti di direzione. Il codice della richiesta viene inviato con ogni messaggio corrispondente al tasto freccia premuto dall'utente. Di seguito sono riportati i tasti di direzione e i codici di richiesta corrispondenti.



| Tasto freccia | Codice richiesta                  |
|-----------|-------------------------------|
| DOWN      | SB \_ LINEDOWN o SB \_ LINERIGHT |
| FINE       | SB in \_ basso                    |
| HOME      | SB \_ Top                       |
| LEFT      | SB \_ lineup o SB \_ LINELEFT    |
| PGDN      | SB \_ PGGIÙ o SB \_ PAGERIGHT |
| PGSU      | SB \_ PAGEUP o SB \_ PAGELEFT    |
| RIGHT     | SB \_ LINEDOWN o SB \_ LINERIGHT |
| UP        | SB \_ lineup o SB \_ LINELEFT    |



 

 

> [!Note]  
> L'interfaccia della tastiera di un controllo barra di scorrimento invia i \_ codici della richiesta SB Top e SB \_ Bottom. Il \_ codice della richiesta SB Top indica che l'utente ha raggiunto il valore superiore dell'intervallo di scorrimento. Un'applicazione scorre il contenuto della finestra verso il basso in modo che la parte superiore dell'oggetto dati sia visibile. Il \_ codice di richiesta inferiore SB indica che l'utente ha raggiunto il valore inferiore dell'intervallo di scorrimento. Se un'applicazione elabora il \_ codice della richiesta SB Bottom, scorre il contenuto della finestra verso l'alto in modo che la parte inferiore dell'oggetto dati sia visibile.

 

Se si vuole un'interfaccia della tastiera per una barra di scorrimento standard, è possibile crearne una autonomamente elaborando il messaggio di [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) nella routine della finestra ed eseguendo quindi l'azione di scorrimento appropriata in base al codice della chiave virtuale che accompagna il messaggio. Per informazioni su come creare un'interfaccia della tastiera per una barra di scorrimento, vedere [creazione di un'interfaccia della tastiera per una barra di scorrimento standard](using-scroll-bars.md).

## <a name="scrolling-the-client-area"></a>Scorrimento dell'area client

Il modo più semplice per scorrere il contenuto di un'area client consiste nel cancellarlo e ridisegnato. Si tratta del metodo che è probabile che un'applicazione usi con i \_ codici di richiesta SB PAGEUP, SB \_ PGGIÙ e SB \_ Top, che in genere richiedono contenuto completamente nuovo.

Per alcuni codici di richiesta, ad esempio SB \_ lineup e SB \_ LINEDOWN, non è necessario cancellare tutto il contenuto, perché alcuni restano visibili dopo lo scorrimento. La funzione [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) mantiene una parte del contenuto dell'area client, sposta la porzione mantenuta in un importo specificato e quindi prepara il resto dell'area client per disegnare nuove informazioni. **ScrollWindowEx** usa la funzione [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) per spostare una parte specifica dell'oggetto dati in una nuova posizione all'interno dell'area client. Qualsiasi parte dell'area client senza copertura (qualsiasi elemento non mantenuto) viene invalidata, cancellata e disegnata quando si verifica il successivo messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) .

La funzione [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) può essere usata per escludere una parte dell'area client dall'operazione di scorrimento. In questo modo gli elementi con posizioni fisse, ad esempio le finestre figlio, non vengono spostati all'interno dell'area client. Invalida automaticamente la parte dell'area client che riceverà le nuove informazioni, pertanto non è necessario che l'applicazione calcoli le proprie aree di ritaglio. Per ulteriori informazioni sul ritaglio, vedere [ritaglio](/windows/desktop/gdi/clipping).

In genere, un'applicazione scorre il contenuto di una finestra nella direzione opposta a quella indicata dalla barra di scorrimento. Ad esempio, quando l'utente fa clic sull'albero della barra di scorrimento nell'area sotto la casella di scorrimento, un'applicazione scorre l'oggetto nella finestra verso l'alto per rivelare una parte dell'oggetto che si trova al di sotto della parte visibile.

È anche possibile scorrere un'area rettangolare usando la funzione [**ScrollDC**](/windows/desktop/api/Winuser/nf-winuser-scrolldc) .

## <a name="scroll-bar-colors-and-metrics"></a>Colori e metriche della barra di scorrimento

Il valore di colore definito dal sistema, \_ barra di scorrimento colore, controlla il colore all'interno di un albero della barra di scorrimento. Usare la funzione [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) per determinare il colore dell'albero della barra di scorrimento e la funzione [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) per impostare il colore dell'albero della barra di scorrimento. Si noti, tuttavia, che questa modifica di colore influiscono su tutte le barre di scorrimento nel sistema.

È possibile ottenere le dimensioni delle bitmap utilizzate dal sistema nelle barre di scorrimento standard chiamando la funzione [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Di seguito sono riportati i valori delle metriche di sistema associati alle barre di scorrimento.



| Metrica di sistema | Descrizione                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| \_CXHSCROLL SM | Larghezza dell'immagine bitmap della freccia sulla barra di scorrimento orizzontale                                                                             |
| \_CXHTHUMB SM  | Larghezza della casella di scorrimento sulla barra di scorrimento orizzontale. Questo valore recupera la larghezza di una barra di scorrimento con una dimensione di pagina pari a zero.    |
| \_CXVSCROLL SM | Larghezza dell'immagine bitmap della freccia sulla barra di scorrimento verticale                                                                               |
| \_CYHSCROLL SM | Altezza dell'immagine bitmap della freccia sulla barra di scorrimento orizzontale                                                                            |
| \_CYVSCROLL SM | Altezza dell'immagine bitmap della freccia sulla barra di scorrimento verticale                                                                              |
| \_CYVTHUMB SM  | Altezza della casella di scorrimento sulla barra di scorrimento verticale. Questo valore recupera l'altezza di una barra di scorrimento con una dimensione di pagina pari a zero. |



 

 

 