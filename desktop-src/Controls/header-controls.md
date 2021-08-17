---
title: Informazioni sui controlli Header
description: Un controllo intestazione è una finestra in genere posizionata sopra colonne di testo o numeri. Contiene un titolo per ogni colonna e può essere suddiviso in parti.
ms.assetid: b464fb9a-e342-4209-ba6f-15b5388f3914
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a6308def8c760ffab492d7aeea086970740be07ebd559d94791baf3512c178b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412264"
---
# <a name="about-header-controls"></a>Informazioni sui controlli Header

Un controllo intestazione è una finestra in genere posizionata sopra colonne di testo o numeri. Contiene un titolo per ogni colonna e può essere suddiviso in parti. L'utente può trascinare i divisori che separano le parti per impostare la larghezza di ogni colonna. Nella figura seguente viene illustrato un controllo intestazione con colonne etichettate che forniscono informazioni dettagliate sui file in una directory.

![Screenshot di una finestra di dialogo con un controllo intestazione a tre colonne](images/header.png)

È possibile creare un controllo intestazione usando la funzione [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) specificando la classe della finestra [**HEADER WC \_**](common-control-window-classes.md) e gli stili [del controllo Header appropriati.](header-control-styles.md) Questa classe di finestra viene registrata quando viene caricata la DLL del controllo comune. Per assicurarsi che questa DLL sia caricata, usare la [**funzione InitCommonControlsEx.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) Dopo aver creato un controllo intestazione, è possibile dividerlo in parti, impostare il testo in ogni parte e controllare l'aspetto della finestra usando i messaggi della finestra di intestazione.

Un controllo intestazione può essere creato come finestra figlio di un altro controllo, ad esempio una casella di riepilogo. Tuttavia, il controllo padre non è a conoscenza del controllo intestazione e non consente lo spazio utilizzato dall'intestazione, con il risultato che gli elementi dell'elenco verranno visualizzati dietro l'intestazione. Se si vuole usare un controllo intestazione in una casella di riepilogo o in un altro controllo, il controllo padre deve essere disegnato dal proprietario in modo che tutti gli elementi siano visualizzati nella posizione corretta.

I controlli visualizzazione elenco hanno già controlli intestazione. Invece di creare un controllo intestazione per un controllo visualizzazione elenco, si usa [**LVM \_ GETHEADER**](lvm-getheader.md) o [**ListView \_ GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) per recuperare il controllo esistente.

-   [Dimensioni e posizione del controllo Intestazione](#header-control-size-and-position)
-   [Elementi](#items)
-   [Controlli Header disegnati dal proprietario](#owner-drawn-header-controls)
-   [Filtri di controllo intestazione](#header-control-filters)
-   [Elaborazione predefinita dei messaggi di controllo intestazione](#default-header-control-message-processing)

## <a name="header-control-size-and-position"></a>Dimensioni e posizione del controllo Intestazione

In genere, è necessario impostare le dimensioni e la posizione di un controllo intestazione per rientrare nei limiti di un particolare rettangolo, ad esempio l'area client di una finestra. Usando il messaggio [**LAYOUT HDM, \_**](hdm-layout.md) è possibile recuperare i valori appropriati per le dimensioni e la posizione dal controllo intestazione.

Quando si [**invia LAYOUT \_ HDM,**](hdm-layout.md)si specifica l'indirizzo di una struttura [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) che contiene le coordinate del rettangolo che il controllo intestazione deve occupare e fornisce un puntatore a una [**struttura WINDOWPOS.**](/windows/win32/api/winuser/ns-winuser-windowpos) Il controllo riempie la **struttura WINDOWPOS** con valori di dimensione e posizione appropriati per posizionare il controllo lungo la parte superiore del rettangolo specificato. Il valore di altezza è la somma delle altezze dei bordi orizzontali del controllo e dell'altezza media dei caratteri nel tipo di carattere attualmente selezionato nel contesto di dispositivo del controllo.

Se si vuole usare [**HDM \_ LAYOUT**](hdm-layout.md) per impostare le dimensioni iniziali e la posizione di un controllo intestazione, impostare lo stato di visibilità iniziale del controllo in modo che sia nascosto. Dopo aver **inviato IL \_ LAYOUT HDM** per recuperare i valori relativi a dimensioni e posizione, è possibile usare la [**funzione SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per impostare le nuove dimensioni, la nuova posizione e lo stato di visibilità.

## <a name="items"></a>Elementi

Un controllo intestazione include in genere diversi elementi di intestazione che definiscono le colonne del controllo. È possibile aggiungere un elemento a un controllo intestazione inviando il [**messaggio \_ INSERTITEM HDM**](hdm-insertitem.md) al controllo. Il messaggio include l'indirizzo di una [**struttura HDITEM.**](/windows/win32/api/commctrl/ns-commctrl-hditema) Questa struttura definisce le proprietà dell'elemento di intestazione, che possono includere una stringa, un'immagine bitmap, una dimensione iniziale e un valore LPARAM definito **dall'applicazione.**

Il **membro fmt** della struttura [**HDITEM di**](/windows/win32/api/commctrl/ns-commctrl-hditema) un elemento può includere il flag **HDF \_ STRING** o **HDF \_ BITMAP** per indicare se il controllo visualizza la stringa o la bitmap dell'elemento. Per visualizzare sia una stringa che una bitmap, creare un elemento creato dal proprietario impostando il membro **fmt** in modo da includere il flag **HDF \_ OWNERDRAW.** La **struttura HDITEM** specifica anche i flag di formattazione che specificano al controllo se allineare al centro, a sinistra o a destra la stringa o la bitmap nel rettangolo dell'elemento.

[**HDM \_ INSERTITEM**](hdm-insertitem.md) restituisce l'indice dell'elemento appena aggiunto. È possibile utilizzare l'indice in altri messaggi per impostare proprietà o recuperare informazioni sull'elemento. È possibile eliminare un elemento usando il [**messaggio \_ HDM DELETEITEM,**](hdm-deleteitem.md) specificando l'indice dell'elemento da eliminare.

È possibile usare il [**messaggio \_ HDM SETITEM**](hdm-setitem.md) per impostare le proprietà di un elemento di intestazione esistente e il messaggio [**\_ HDM GETITEM**](hdm-getitem.md) per recuperare le proprietà correnti di un elemento. Per recuperare un conteggio degli elementi in un controllo intestazione, usare il [**messaggio \_ HDM GETITEMCOUNT.**](hdm-getitemcount.md)

## <a name="owner-drawn-header-controls"></a>Owner-Drawn di intestazione

È possibile definire singoli elementi di un controllo intestazione come elementi disegnati dal proprietario. L'uso di questa tecnica offre un maggiore controllo rispetto a quanto sarebbe altrimenti possibile sull'aspetto di un elemento di intestazione.

È possibile usare il messaggio [**\_ INSERTITEM HDM**](hdm-insertitem.md) per inserire un nuovo elemento creato dal proprietario in un controllo intestazione o il messaggio [**\_ HDM SETITEM**](hdm-setitem.md) per modificare un elemento esistente in un elemento creato dal proprietario. Entrambi i messaggi includono l'indirizzo di [**una struttura HDITEM,**](/windows/win32/api/commctrl/ns-commctrl-hditema) che deve avere il membro **fmt** impostato sul **valore DI \_ OWNERDRAW di HDF.**

Quando un controllo intestazione deve disegnare un elemento disegnato dal proprietario, invia il [**messaggio \_ WM DRAWITEM**](wm-drawitem.md) alla finestra padre. Il *parametro wParam* del messaggio è l'identificatore della finestra figlio del controllo intestazione e il parametro *lParam* è l'indirizzo di una [**struttura DRAWITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) La finestra padre usa le informazioni nella struttura per disegnare l'elemento. Per un elemento disegnato dal proprietario in un controllo intestazione, la **struttura DRAWITEMSTRUCT** contiene le informazioni seguenti.



| Membro         | Descrizione                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | [**ODT \_ Tipo di**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) controllo header disegnato dal proprietario.                                                                                        |
| **CtlID**      | Identificatore della finestra figlio del controllo intestazione.                                                                                                         |
| **Itemid**     | Indice dell'elemento da disegnare.                                                                                                                         |
| **itemAction** | [**ODA \_ Flag draw-action DRAWENTIRE.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)                                                                                         |
| **itemState**  | [**ODS \_ Flag di**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) azione di disegno SELECTED se il cursore si trova sull'elemento e il pulsante del mouse è premuto. In caso contrario, questo membro è zero. |
| **hwndItem**   | Handle per il controllo intestazione.                                                                                                                          |
| **Hdc**        | Handle per il contesto di dispositivo del controllo intestazione.                                                                                                    |
| **rcItem**     | Coordinate dell'elemento di intestazione da disegnare. Le coordinate sono relative all'angolo superiore sinistro del controllo intestazione.                               |
| **Itemdata**   | Valore a 32 bit definito dall'applicazione associato all'elemento.                                                                                             |



 

## <a name="header-control-filters"></a>Filtri di controllo intestazione

Specificando lo stile della finestra [**\_ HDS FILTERBAR**](header-control-styles.md) per un controllo intestazione, è possibile abilitare la posizione delle caselle di modifica del filtro sotto le intestazioni di colonna. Accanto alla casella di modifica viene visualizzato un pulsante di filtro. È possibile implementare il filtro rispondendo ai codici di notifica [ \_ HDN BEGINFILTEREDIT,](hdn-beginfilteredit.md) [ \_ HDN ENDFILTEREDIT,](hdn-endfilteredit.md) [HDN \_ FILTERBTNCLICK](hdn-filterbtnclick.md)o [HDN \_ FILTERCHANGE.](hdn-filterchange.md)

Per impostazione predefinita, la casella di modifica contiene una richiesta di immissione di testo da parte dell'utente. È possibile ripristinare lo stato predefinito della casella di modifica usando [**Header \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) o [**Header \_ ClearAllFilters.**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)

Nell'esempio di codice seguente viene illustrato come recuperare il controllo intestazione da un controllo visualizzazione elenco e aggiungere una barra dei filtri.


```
// hList is the HWND of the list-view control.
HWND hHeader = ListView_GetHeader(hList);
LONG_PTR styles = GetWindowLongPtr(hHeader, GWL_STYLE);
SetWindowLongPtr(g_hHeader, GWL_STYLE, styles | HDS_FILTERBAR);
```



## <a name="default-header-control-message-processing"></a>Elaborazione predefinita dei messaggi di controllo intestazione

Questa sezione descrive i messaggi della finestra gestiti dalla routine della finestra per la classe di finestra [**WC \_ HEADER.**](common-control-window-classes.md)



| Message                                            | Elaborazione eseguita                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                 | Inizializza il controllo intestazione.                                                                                                                                                                                                                                                                               |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)               | Annulla l'inizializzazione del controllo intestazione.                                                                                                                                                                                                                                                                             |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)         | Riempie lo sfondo del controllo intestazione usando il colore di sfondo corrente del controllo.                                                                                                                                                                                                                      |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | Restituisce una combinazione dei [**valori DLGC \_ WANTTAB**](/windows/desktop/dlgbox/wm-getdlgcode) [**e DLGC \_ WANTARROWS.**](/windows/desktop/dlgbox/wm-getdlgcode)                                                                                                                     |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Restituisce l'handle per il tipo di carattere corrente, utilizzato dal controllo intestazione per disegnare il testo.                                                                                                                                                                                                                 |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) | Acquisisce l'input del mouse. Se il cursore del mouse si trova su un divisore, il controllo invia il codice di notifica [ \_ BEGINTRACK HDN](hdn-begintrack.md) e inizia a trascinare il divisore. Se il cursore si trova su un elemento, l'elemento viene visualizzato nello stato premuto.                                                            |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | Uguale al [**messaggio WM \_ LBUTTONDBLCLK.**](/windows/desktop/inputdev/wm-lbuttondblclk)                                                                                                                                                                                                                                       |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)         | Rilascia il mouse capture. Se il controllo stava verificando lo spostamento del mouse, invia il codice di notifica [ \_ HDN ENDTRACK](hdn-endtrack.md) e ridisegna il controllo intestazione. In caso contrario, il controllo invia il codice di notifica [ \_ HDN ITEMCLICK](hdn-itemclick.md) e ridisegna l'elemento di intestazione su cui è stato fatto clic. |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)         | Se viene trascinato un divisore, il controllo invia il codice di notifica [HDN \_ TRACK](hdn-track.md) e visualizza l'elemento nella nuova posizione. Se il pulsante sinistro del mouse è verso il basso e il cursore si trova su un elemento, l'elemento viene visualizzato nello stato premuto.                                                      |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)             | Alloca e inizializza una struttura di dati interna.                                                                                                                                                                                                                                                         |
| [**WM \_ NCDESTROY**](/windows/desktop/winmsg/wm-ncdestroy)           | Libera le risorse allocate dal controllo intestazione dopo l'annullamento dell'inizializzazione del controllo intestazione.                                                                                                                                                                                                                |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                      | Disegna l'area non valida del controllo intestazione. Se il *parametro wParam* è diverso da NULL, il controllo presuppone che il valore sia hdc e dipinge usando tale contesto di dispositivo.                                                                                                                                    |
| [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor)           | Imposta la forma del cursore, a seconda che il cursore si trova su un divisore o in un elemento di intestazione.                                                                                                                                                                                                                   |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | Seleziona un nuovo handle del tipo di carattere nel contesto di dispositivo per il controllo intestazione.                                                                                                                                                                                                                                     |



 

 

 