---
title: Informazioni sui controlli intestazione
description: Un controllo intestazione è una finestra che in genere è posizionata sopra le colonne di testo o numeri. Contiene un titolo per ogni colonna, che può essere divisa in parti.
ms.assetid: b464fb9a-e342-4209-ba6f-15b5388f3914
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d9beaa9dc3bd8eb94d749ec271902a480b853e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730402"
---
# <a name="about-header-controls"></a>Informazioni sui controlli intestazione

Un controllo intestazione è una finestra che in genere è posizionata sopra le colonne di testo o numeri. Contiene un titolo per ogni colonna, che può essere divisa in parti. L'utente può trascinare i divisori che separano le parti per impostare la larghezza di ogni colonna. Nella figura seguente viene illustrato un controllo intestazione con colonne con etichetta che forniscono informazioni dettagliate sui file in una directory.

![Screenshot di una finestra di dialogo con un controllo intestazione a tre colonne](images/header.png)

È possibile creare un controllo Header usando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra di [**\_ intestazione WC**](common-control-window-classes.md) e gli stili appropriati del [controllo intestazione](header-control-styles.md). Questa classe della finestra viene registrata quando viene caricata la DLL del controllo comune. Per assicurarsi che questa DLL venga caricata, utilizzare la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) . Dopo aver creato un controllo intestazione, è possibile suddividerlo in parti, impostare il testo in ogni parte e controllare l'aspetto della finestra usando i messaggi della finestra di intestazione.

È possibile creare un controllo intestazione come finestra figlio di un altro controllo, ad esempio una casella di riepilogo. Tuttavia, il controllo padre non è a conoscenza del controllo intestazione e non consente lo spazio occupato dall'intestazione, con il risultato che gli elementi dell'elenco verranno visualizzati dietro l'intestazione. Se si desidera utilizzare un controllo intestazione in una casella di riepilogo o un altro controllo, il controllo padre deve essere creato dal proprietario in modo che tutti gli elementi vengano visualizzati nella posizione corretta.

I controlli di visualizzazione elenco dispongono già di controlli intestazione. Anziché creare un controllo intestazione per un controllo visualizzazione elenco, è possibile usare [**LVM \_ GetHeader**](lvm-getheader.md) o [**ListView \_ GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) per recuperare il controllo esistente.

-   [Dimensioni e posizione del controllo intestazione](#header-control-size-and-position)
-   [Elementi](#items)
-   [Controlli intestazione creati dal proprietario](#owner-drawn-header-controls)
-   [Filtri di controllo intestazione](#header-control-filters)
-   [Elaborazione del messaggio di controllo intestazione predefinita](#default-header-control-message-processing)

## <a name="header-control-size-and-position"></a>Dimensioni e posizione del controllo intestazione

In genere, è necessario impostare le dimensioni e la posizione di un controllo intestazione in modo che rientrino nei limiti di un determinato rettangolo, ad esempio l'area client di una finestra. Utilizzando il messaggio [**di \_ layout HDM**](hdm-layout.md) , è possibile recuperare i valori di dimensioni e posizioni appropriati dal controllo intestazione.

Quando si invia il [**\_ layout HDM**](hdm-layout.md), viene specificato l'indirizzo di una struttura [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) che contiene le coordinate del rettangolo che il controllo intestazione deve occupare e fornisce un puntatore a una struttura [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) . Il controllo Compila la struttura **WINDOWPOS** con i valori di posizione e dimensioni appropriati per posizionare il controllo lungo la parte superiore del rettangolo specificato. Il valore altezza è la somma delle altezze dei bordi orizzontali del controllo e l'altezza media dei caratteri nel tipo di carattere attualmente selezionato nel contesto di dispositivo del controllo.

Se si vuole usare il [**\_ layout HDM**](hdm-layout.md) per impostare le dimensioni iniziali e la posizione di un controllo intestazione, impostare lo stato di visibilità iniziale del controllo in modo che sia nascosto. Dopo aver inviato il **\_ layout HDM** per recuperare i valori di dimensioni e posizione, è possibile usare la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per impostare le nuove dimensioni, la posizione e lo stato di visibilità.

## <a name="items"></a>Elementi

Un controllo intestazione contiene in genere diversi elementi di intestazione che definiscono le colonne del controllo. Per aggiungere un elemento a un controllo intestazione, inviare il messaggio [**HDM \_ INSERTITEM**](hdm-insertitem.md) al controllo. Il messaggio include l'indirizzo di una struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) . Questa struttura definisce le proprietà dell'elemento di intestazione, che può includere una stringa, un'immagine bitmap, una dimensione iniziale e un valore **lParam** definito dall'applicazione.

Il membro **FMT** della struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) di un elemento può includere il flag **HDF \_ String** o **HDF \_ bitmap** per indicare se il controllo Visualizza la stringa o la bitmap dell'elemento. Se si desidera visualizzare sia una stringa che una bitmap, creare un elemento creato dal proprietario impostando il membro **FMT** in modo da includere il flag **HDF \_ OWNERDRAW** . La struttura **HDITEM** specifica anche i flag di formattazione che indicano al controllo se allineare al centro, a sinistra o a destra la stringa o la bitmap nel rettangolo dell'elemento.

[**HDM \_ INSERTITEM**](hdm-insertitem.md) restituisce l'indice dell'elemento appena aggiunto. È possibile utilizzare l'indice in altri messaggi per impostare le proprietà o recuperare le informazioni sull'elemento. È possibile eliminare un elemento usando il messaggio [**HDM \_ DeleteItem**](hdm-deleteitem.md) , specificando l'indice dell'elemento da eliminare.

Per impostare le proprietà di un elemento di intestazione esistente e il messaggio [**\_ GetItem di HDM**](hdm-getitem.md) per recuperare le proprietà correnti di un elemento, è possibile utilizzare il messaggio [**HDM \_**](hdm-setitem.md) . Per recuperare un conteggio degli elementi in un controllo Header, usare il messaggio [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md) .

## <a name="owner-drawn-header-controls"></a>Controlli intestazione Owner-Drawn

È possibile definire singoli elementi di un controllo intestazione come elementi creati dal proprietario. L'uso di questa tecnica offre un maggiore controllo rispetto all'aspetto di un elemento di intestazione.

È possibile utilizzare il messaggio [**HDM \_ INSERTITEM**](hdm-insertitem.md) per inserire un nuovo elemento creato dal proprietario in un controllo intestazione o il messaggio [**HDM \_ elemento**](hdm-setitem.md) per modificare un elemento esistente in un elemento creato dal proprietario. Entrambi i messaggi includono l'indirizzo di una struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) , che deve avere il membro **FMT** impostato sul **valore \_ OWNERDRAW di HDF** .

Quando un controllo intestazione deve disegnare un elemento creato dal proprietario, invia il messaggio [**WM \_ DrawItem**](wm-drawitem.md) alla finestra padre. Il parametro *wParam* del messaggio è l'identificatore della finestra figlio del controllo intestazione e il parametro *lParam* è un indirizzo di una struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . La finestra padre utilizza le informazioni della struttura per tracciare l'elemento. Per un elemento creato dal proprietario in un controllo Header, la struttura **DRAWITEMSTRUCT** contiene le informazioni seguenti.



| Membro         | Descrizione                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | [**ODT \_**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Tipo di controllo creato dal proprietario dell'intestazione.                                                                                        |
| **CtlID**      | Identificatore della finestra figlio del controllo intestazione.                                                                                                         |
| **ID elemento**     | Indice dell'elemento da disegnare.                                                                                                                         |
| **itemAction** | [**Oda \_**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Flag di disegno-azione DRAWENTIRE.                                                                                         |
| **itemState**  | [**ODS \_**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Flag di disegno-azione selezionato se il cursore si trova sull'elemento e il pulsante del mouse è inattivo. In caso contrario, questo membro è zero. |
| **hwndItem**   | Handle per il controllo intestazione.                                                                                                                          |
| **hDC**        | Handle per il contesto di dispositivo del controllo intestazione.                                                                                                    |
| **rcItem**     | Coordinate dell'elemento dell'intestazione da disegnare. Le coordinate sono relative all'angolo superiore sinistro del controllo intestazione.                               |
| **itemData**   | Valore a 32 bit definito dall'applicazione associato all'elemento.                                                                                             |



 

## <a name="header-control-filters"></a>Filtri di controllo intestazione

Specificando lo stile della finestra [**HDS \_ FILTERBAR**](header-control-styles.md) per un controllo Header, è possibile abilitare il posizionamento delle caselle di modifica del filtro sotto le intestazioni di colonna. Accanto alla casella di modifica viene visualizzato un pulsante filtro. È possibile implementare il filtro rispondendo ai codici di notifica [HDN \_ BEGINFILTEREDIT](hdn-beginfilteredit.md), [HDN \_ ENDFILTEREDIT](hdn-endfilteredit.md), [HDN \_ ](hdn-filterbtnclick.md)FILTERBTNCLICK o [HDN \_ FILTERCHANGE](hdn-filterchange.md) .

Per impostazione predefinita, la casella di modifica contiene una richiesta di immissione del testo da parte dell'utente. È possibile ripristinare lo stato predefinito della casella di modifica usando l' [**intestazione \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) o [**\_ ClearAllFilters**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters).

Nell'esempio di codice seguente viene illustrato come recuperare il controllo Header da un controllo visualizzazione elenco e aggiungere una barra dei filtri.


```
// hList is the HWND of the list-view control.
HWND hHeader = ListView_GetHeader(hList);
LONG_PTR styles = GetWindowLongPtr(hHeader, GWL_STYLE);
SetWindowLongPtr(g_hHeader, GWL_STYLE, styles | HDS_FILTERBAR);
```



## <a name="default-header-control-message-processing"></a>Elaborazione del messaggio di controllo intestazione predefinita

In questa sezione vengono descritti i messaggi della finestra gestiti dalla routine della finestra per la classe della finestra di [**\_ intestazione WC**](common-control-window-classes.md) .



| Message                                            | Elaborazione eseguita                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**creazione di WM \_**](/windows/desktop/winmsg/wm-create)                 | Inizializza il controllo intestazione.                                                                                                                                                                                                                                                                               |
| [**eliminazione di WM \_**](/windows/desktop/winmsg/wm-destroy)               | Inizializza il controllo intestazione.                                                                                                                                                                                                                                                                             |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd)         | Riempie lo sfondo del controllo intestazione utilizzando il colore di sfondo corrente del controllo.                                                                                                                                                                                                                      |
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)         | Restituisce una combinazione dei valori [**DLGC \_ WANTTAB**](/windows/desktop/dlgbox/wm-getdlgcode) e [**DLGC \_ WANTARROWS**](/windows/desktop/dlgbox/wm-getdlgcode) .                                                                                                                     |
| [**\_tipo di carattere WM GetFont**](/windows/desktop/winmsg/wm-getfont)               | Restituisce l'handle per il tipo di carattere corrente, utilizzato dal controllo intestazione per creare il relativo testo.                                                                                                                                                                                                                 |
| [**\_LBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-lbuttondblclk) | Acquisisce l'input del mouse. Se il cursore del mouse si trova su un divisore, il controllo Invia il codice di notifica [ \_ BEGINTRACK di HDN](hdn-begintrack.md) e inizia a trascinare il divisore. Se il cursore si trova su un elemento, l'elemento viene visualizzato nello stato premuto.                                                            |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)     | Uguale al messaggio [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) .                                                                                                                                                                                                                                       |
| [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)         | Rilascia l'acquisizione del mouse. Se il controllo tiene traccia del movimento del mouse, invia il codice di notifica [ \_ ENDTRACK HDN](hdn-endtrack.md) e ridisegnato il controllo intestazione. In caso contrario, il controllo Invia il codice di notifica [ \_ ITEMCLICK di HDN](hdn-itemclick.md) e ritraccia l'elemento dell'intestazione su cui è stato fatto clic. |
| [**MOUSEMOVE di WM \_**](/windows/desktop/inputdev/wm-mousemove)         | Se un divisore viene trascinato, il controllo Invia il codice di notifica di [ \_ rilevamento HDN](hdn-track.md) e visualizza l'elemento nella nuova posizione. Se il pulsante sinistro del mouse è premuto e il cursore si trova su un elemento, l'elemento viene visualizzato nello stato premuto.                                                      |
| [**\_NCCREATE WM**](/windows/desktop/winmsg/wm-nccreate)             | Alloca e Inizializza una struttura di dati interna.                                                                                                                                                                                                                                                         |
| [**\_NCDESTROY WM**](/windows/desktop/winmsg/wm-ncdestroy)           | Libera le risorse allocate dal controllo intestazione dopo che il controllo intestazione non è stato inizializzato.                                                                                                                                                                                                                |
| [**\_disegno WM**](/windows/desktop/gdi/wm-paint)                      | Disegna l'area non valida del controllo intestazione. Se il parametro *wParam* è diverso da null, il controllo presuppone che il valore sia un HDC e i colori che usano tale contesto di dispositivo.                                                                                                                                    |
| [**\_cursore WM**](/windows/desktop/menurc/wm-setcursor)           | Imposta la forma del cursore, a seconda che il cursore si trovi in un divisore o in un elemento di intestazione.                                                                                                                                                                                                                   |
| [**\_tipo di carattere WM**](/windows/desktop/winmsg/wm-setfont)               | Seleziona un nuovo handle del tipo di carattere nel contesto di dispositivo per il controllo intestazione.                                                                                                                                                                                                                                     |



 

 

 