---
title: Informazioni sui controlli struttura a schede
description: Un controllo Struttura a schede è simile ai separatori in un blocco per appunti o alle etichette in un archivio. L'uso del controllo Struttura a schede consente a un'applicazione di definire più pagine per la stessa area di una finestra o una finestra di dialogo.
ms.assetid: 55ed2863-7f8d-43ce-a0f9-6f6d41e3f947
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c45ac7caa05c73e1dcf22a8e6f0eb4d031ca079
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118531"
---
# <a name="about-tab-controls"></a>Informazioni sui controlli struttura a schede

Un controllo Struttura a schede è simile ai separatori in un blocco per appunti o alle etichette in un archivio. L'uso del controllo Struttura a schede consente a un'applicazione di definire più pagine per la stessa area di una finestra o una finestra di dialogo. Ogni pagina è costituita da un determinato tipo di informazioni o da un gruppo di controlli che l'applicazione visualizza quando l'utente seleziona la scheda corrispondente.

Lo screenshot seguente mostra un semplice controllo struttura a schede che contiene le schede per i giorni della settimana. È stata selezionata la scheda Tuesday.

![Screenshot di una finestra delle proprietà con cinque schede, una per ogni giorno della settimana](images/tab-simple.png)

In questo argomento sono incluse le sezioni seguenti.

-   [Creazione di controlli struttura a schede](#creating-tab-controls)
-   [Stili del controllo Tab](#tab-control-styles)
-   [Schede e attributi di tabulazione](#tabs-and-tab-attributes)
-   [Area di visualizzazione](#display-area)
-   [Selezione scheda](#tab-selection)
-   [Elenchi di immagini del controllo Tab](#tab-control-image-lists)
-   [Dimensioni e posizione delle tabulazioni](#tab-size-and-position)
-   [Schede create dal proprietario](#owner-drawn-tabs)
-   [Descrizioni comandi del controllo Tab](#tab-control-tooltips)
-   [Elaborazione dei messaggi di controllo scheda predefiniti](#default-tab-control-message-processing)

## <a name="creating-tab-controls"></a>Creazione di controlli struttura a schede

È possibile creare un controllo struttura a schede chiamando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe [**WC \_ TABCONTROL**](common-control-window-classes.md) Window. Questa classe della finestra viene registrata quando viene caricata la DLL dei controlli comuni. Per assicurarsi che la DLL venga caricata, utilizzare la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .

In Microsoft Visual Studio, è possibile creare un controllo struttura a schede utilizzando la casella degli strumenti.

Si inviano messaggi a un controllo struttura a schede per aggiungere schede e influire in altro modo sull'aspetto e sul comportamento del controllo. Ogni messaggio ha una macro corrispondente che è possibile usare anziché inviare il messaggio in modo esplicito. Non è possibile disabilitare una singola scheda in un controllo struttura a schede. Tuttavia, è possibile disabilitare un controllo struttura a schede in una finestra delle proprietà disabilitando la pagina corrispondente.

## <a name="tab-control-styles"></a>Stili del controllo Tab

È possibile applicare determinate caratteristiche ai controlli struttura a schede specificando gli stili del controllo Tab quando viene creato il controllo. Ad esempio, è possibile specificare l'allineamento e l'aspetto generale delle schede in un controllo struttura a schede.

È possibile fare in modo che le schede apparino come pulsanti specificando lo stile dei [**\_ pulsanti TCS**](tab-control-styles.md) . Le schede in questo tipo di controllo struttura a schede devono gestire la stessa funzione dei controlli Button; ovvero fare clic su una scheda per eseguire un comando anziché visualizzare una pagina. Poiché l'area di visualizzazione in un controllo scheda pulsante non viene in genere utilizzata, non viene tracciato alcun bordo.

È possibile fare in modo che una scheda riceva lo stato attivo per l'input quando si fa clic specificando lo stile [**\_ FOCUSONBUTTONDOWN di TCS**](tab-control-styles.md) . Questo stile viene in genere usato solo con lo stile dei [**\_ pulsanti TCS**](tab-control-styles.md) . È possibile specificare che una scheda non riceve lo stato attivo per l'input quando si fa clic con lo stile [**TCS \_ FOCUSNEVER**](tab-control-styles.md) .

Per impostazione predefinita, un controllo struttura a schede Visualizza una sola riga di schede. Se non è possibile visualizzare tutte le schede contemporaneamente, il controllo struttura a schede Visualizza un controllo di scorrimento, in modo che l'utente possa scorrere le schede aggiuntive nella visualizzazione. È possibile fare in modo che un controllo struttura a schede visualizzi più righe di tabulazioni, se necessario, specificando lo stile su più [**\_ righe di TCS**](tab-control-styles.md) . Con questo stile, tutte le schede possono essere visualizzate contemporaneamente. Le schede sono allineate a sinistra all'interno di ogni riga, a meno che non si specifichi lo stile [**\_ RIGHTJUSTIFY di TCS**](tab-control-styles.md) . In questo caso, la larghezza di ogni scheda viene aumentata in modo che ogni riga di schede riempia l'intera larghezza del controllo struttura a schede.

Un controllo struttura a schede ridimensiona automaticamente ogni scheda per adattarla, se presente, e la relativa etichetta. Per assegnare a tutte le schede la stessa larghezza, è possibile specificare lo stile [**\_ FIXEDWIDTH di TCS**](tab-control-styles.md) . Il controllo ridimensiona tutte le schede per adattarle all'etichetta più ampia oppure è possibile assegnare una larghezza e un'altezza specifiche usando il messaggio [**TCM \_ SETITEMSIZE**](tcm-setitemsize.md) . All'interno di ogni scheda, il controllo Centra l'icona e l'etichetta, posizionando l'icona a sinistra dell'etichetta. È possibile forzare l'icona a sinistra, lasciando l'etichetta centrata, specificando lo [**stile \_ FORCEICONLEFT di TCS**](tab-control-styles.md) . È possibile allineare a sinistra sia l'icona che l'etichetta usando lo stile [**TCS \_ FORCELABELLEFT**](tab-control-styles.md) . Non è possibile usare lo stile **TCS \_ FIXEDWIDTH** con lo stile [**\_ RIGHTJUSTIFY di TCS**](tab-control-styles.md) .

È possibile specificare che la finestra padre disegni le schede nel controllo utilizzando lo stile [**TCS \_ OwnerDrawFixed**](tab-control-styles.md) . Per ulteriori informazioni, vedere [schede create dal proprietario](#owner-drawn-tabs).

È possibile specificare che un controllo struttura a schede creerà un controllo ToolTip usando lo [**stile \_ Descrizione comando TCS**](tab-control-styles.md) . Per altre informazioni, vedere [descrizioni comandi del controllo Tab](#tab-control-tooltips).

## <a name="tabs-and-tab-attributes"></a>Schede e attributi di tabulazione

Ogni scheda in un controllo struttura a schede è costituita da un'icona, un'etichetta e dati definiti dall'applicazione. Queste informazioni vengono specificate da una struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . È possibile aggiungere schede a un controllo struttura a schede, recuperare il numero di schede, recuperare e impostare il contenuto di una scheda ed eliminare le schede. Le schede sono identificate dal relativo indice in base zero.

Per aggiungere schede a un controllo struttura a schede, usare il messaggio [**\_ INSERTITEM INSERTITEM**](tcm-insertitem.md) , specificando la posizione dell'elemento e l'indirizzo di una struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . È possibile recuperare e impostare il contenuto di una scheda esistente usando i messaggi [**TCM \_**](tcm-getitem.md) GetItem e [**TCM \_**](tcm-setitem.md) . Per ogni scheda è possibile specificare un'icona, un'etichetta o entrambe. È inoltre possibile specificare i dati definiti dall'applicazione da associare alla scheda.

È possibile recuperare il numero corrente di schede usando il messaggio [**TCM \_ GETITEMCOUNT**](tcm-getitemcount.md) , eliminare una scheda usando il messaggio [**TCM \_ DeleteItem**](tcm-deleteitem.md) ed eliminare tutte le schede in un controllo struttura a schede usando il messaggio [**TCM \_ DELETEALLITEMS**](tcm-deleteallitems.md) .

È possibile associare dati definiti dall'applicazione a ogni scheda. Ad esempio, è possibile salvare le informazioni su ogni pagina con la scheda corrispondente. Per impostazione predefinita, un controllo struttura a schede consente di allocare quattro byte aggiuntivi per scheda per i dati definiti dall'applicazione. È possibile modificare il numero di byte aggiuntivi per scheda usando il messaggio [**TCM \_ SETITEMEXTRA**](tcm-setitemextra.md) . È possibile utilizzare questo messaggio solo quando il controllo Tab è vuoto.

I dati definiti dall'applicazione vengono specificati dal membro **lParam** della struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . Se si usano più di 4 byte di dati definiti dall'applicazione, è necessario definire una struttura personalizzata e usarla invece di **TCITEM**. È possibile recuperare e impostare i dati definiti dall'applicazione nello stesso modo in cui si recuperano e si impostano altre informazioni su una scheda, usando i messaggi [**TCM \_ GetItem**](tcm-getitem.md) e [**TCM \_**](tcm-setitem.md) .

Il primo membro della struttura deve essere una struttura [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) e i membri rimanenti devono specificare i dati definiti dall'applicazione. **TCITEMHEADER** è identico a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema), ad eccezione del fatto che non dispone del membro **lParam** . La differenza tra le dimensioni della struttura e le dimensioni di **TCITEMHEADER** deve essere uguale al numero di byte aggiuntivi per scheda.

## <a name="display-area"></a>Area di visualizzazione

L'area di visualizzazione di un controllo struttura a schede è l'area in cui un'applicazione Visualizza la pagina corrente. In genere, un'applicazione crea una finestra o una finestra di dialogo figlio, impostando le dimensioni e la posizione della finestra in modo che corrispondano all'area di visualizzazione. Dato il rettangolo della finestra per un controllo struttura a schede, è possibile calcolare il rettangolo di delimitazione dell'area di visualizzazione usando il messaggio [**TCM \_ ADJUSTRECT**](tcm-adjustrect.md) .

In alcuni casi l'area di visualizzazione deve avere una dimensione specifica, ad esempio la dimensione di una finestra di dialogo figlio non modale. Dato il rettangolo di delimitazione per l'area di visualizzazione, è possibile usare [**TCM \_ ADJUSTRECT**](tcm-adjustrect.md) per calcolare il rettangolo della finestra corrispondente per il controllo struttura a schede.

## <a name="tab-selection"></a>Selezione scheda

Quando l'utente seleziona una scheda, un controllo struttura a schede invia i codici di notifica della finestra padre sotto forma di messaggi di [**\_ notifica WM**](wm-notify.md) . Il codice di notifica [ \_ SELCHANGING di TCN](tcn-selchanging.md) viene inviato prima della modifica della selezione e il codice di notifica [ \_ selChange TCN](tcn-selchange.md) viene inviato dopo la modifica della selezione.

È possibile elaborare [TCN \_ SELCHANGING](tcn-selchanging.md) per salvare lo stato della pagina in uscita. È possibile restituire **true** per impedire la modifica della selezione. Ad esempio, è possibile che non si desideri disattivare una finestra di dialogo figlio in cui un controllo presenta un'impostazione non valida.

È necessario elaborare [TCN \_ selChange](tcn-selchange.md) per visualizzare la pagina in arrivo nell'area di visualizzazione. Questo può semplicemente richiedere la modifica delle informazioni visualizzate in una finestra figlio. Più spesso, ogni pagina è costituita da una finestra o una finestra di dialogo figlio. In questo caso, un'applicazione può elaborare la notifica eliminando o nascondendo la finestra o la finestra di dialogo figlio in uscita e creando o visualizzando la finestra o la finestra di dialogo figlio in arrivo.

È possibile recuperare e impostare la selezione corrente usando i messaggi [**TCM \_ GetCurSel**](tcm-getcursel.md) e [**TCM \_**](tcm-setcursel.md) .

## <a name="tab-control-image-lists"></a>Elenchi di immagini del controllo Tab

A ogni scheda può essere associata un'icona, specificata da un indice nell'elenco di immagini per il controllo struttura a schede. Quando viene creato, un controllo struttura a schede non dispone di un elenco di immagini associato. Un'applicazione può creare un elenco di immagini usando la funzione di [**\_ creazione ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) e quindi assegnarla a un controllo struttura a schede usando il messaggio di base di [**TCM \_**](tcm-setimagelist.md) .

È possibile aggiungere immagini a un elenco di immagini di un controllo struttura a schede Analogamente a qualsiasi altro elenco di immagini. Tuttavia, un'applicazione deve rimuovere le immagini usando il messaggio [**TCM \_ REMOVEIMAGE**](tcm-removeimage.md) anziché la funzione [**di \_ rimozione ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) . Questo messaggio garantisce che ogni scheda rimanga associata alla stessa immagine precedente.

L'eliminazione di un controllo struttura a schede non comporta l'eliminazione di un elenco di immagini associato. È necessario eliminare l'elenco di immagini separatamente. Questa opzione è utile se si desidera assegnare lo stesso elenco di immagini a più controlli scheda.

Per recuperare l'handle per l'elenco immagini attualmente associato a un controllo struttura a schede, è possibile usare il messaggio [**TCM \_ getimagine**](tcm-getimagelist.md) .

## <a name="tab-size-and-position"></a>Dimensioni e posizione delle tabulazioni

Ogni scheda in un controllo struttura a schede ha una dimensione e una posizione. È possibile impostare le dimensioni delle schede, recuperare il rettangolo delimitatore di una scheda o determinare quale scheda si trova in una posizione specificata.

Per i controlli di tabulazione a larghezza fissa e proprietari, è possibile impostare la larghezza e l'altezza esatte delle schede usando il messaggio [**TCM \_ SETITEMSIZE**](tcm-setitemsize.md) . In altri controlli di tabulazione, le dimensioni di ogni scheda vengono calcolate in base all'icona e all'etichetta per la scheda. Il controllo struttura a schede include lo spazio per un bordo e un margine aggiuntivo. È possibile impostare lo spessore del margine utilizzando il messaggio [**TCM \_ sepadding**](tcm-setpadding.md) .

È possibile determinare il rettangolo di delimitazione corrente per una scheda usando il messaggio [**TCM \_ GETITEMRECT**](tcm-getitemrect.md) . È possibile determinare la scheda, se presente, che si trova in una posizione specificata tramite il messaggio [**TCM \_ HITTEST**](tcm-hittest.md) .

In un controllo struttura a schede con lo stile [**\_ multiriga TCS**](tab-control-styles.md) è possibile determinare il numero corrente di righe di schede usando il messaggio [**TCM \_ GetRowCount**](tcm-getrowcount.md) .

## <a name="owner-drawn-tabs"></a>Schede Owner-Drawn

Se un controllo struttura a schede ha lo stile [**\_ OwnerDrawFixed di TCS**](tab-control-styles.md) , la finestra padre deve disegnare le schede elaborando il messaggio [**WM \_ DrawItem**](wm-drawitem.md) . Il controllo struttura a schede Invia questo messaggio ogni volta che è necessario disegnare una scheda. Il parametro *lParam* specifica l'indirizzo di una struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , che contiene l'indice della scheda, il rettangolo di delimitazione e il contesto di dispositivo (DC) in cui eseguire il progetto.

Per impostazione predefinita, il membro **ItemData** di [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contiene il valore del membro **lParam** della struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . Tuttavia, se si modifica la quantità di dati definiti dall'applicazione per scheda, **ItemData** contiene invece l'indirizzo dei dati. È possibile modificare la quantità di dati definiti dall'applicazione per ogni scheda usando il messaggio [**TCM \_ SETITEMEXTRA**](tcm-setitemextra.md) .

Per specificare le dimensioni degli elementi in un controllo struttura a schede, la finestra padre deve elaborare il messaggio [**WM \_ MeasureItem**](wm-measureitem.md) . Poiché tutte le schede in un controllo struttura a schede creato dal proprietario hanno le stesse dimensioni, il messaggio viene inviato una sola volta. Non è disponibile alcun stile di controllo TAB per le schede create dal proprietario di dimensioni variabili. È anche possibile impostare la larghezza e l'altezza delle schede usando il messaggio [**TCM \_ SETITEMSIZE**](tcm-setitemsize.md) .

## <a name="tab-control-tooltips"></a>Descrizioni comandi del controllo Tab

È possibile usare un controllo ToolTip per fornire una breve descrizione di ogni scheda in un controllo struttura a schede. Un controllo struttura a schede con lo stile della descrizione comando [**TCS \_**](tab-control-styles.md) crea un controllo ToolTip quando viene creato ed Elimina il controllo ToolTip quando viene eliminato definitivamente. È anche possibile creare un controllo ToolTip e assegnarlo a un controllo struttura a schede.

Se si usa un controllo ToolTip con un controllo struttura a schede, la finestra padre deve elaborare il codice di notifica [ \_ GETDISPINFO TTN](ttn-getdispinfo.md) per fornire una descrizione di ogni scheda su richiesta.

Per usare lo stesso controllo ToolTip con più di un controllo struttura a schede, creare il controllo ToolTip manualmente e assegnarlo al controllo struttura a schede usando il messaggio [**TCM \_ setooltips**](tcm-settooltips.md) . È possibile recuperare l'handle per il controllo ToolTip corrente di un controllo Tab usando il messaggio [**TCM \_ GetToolTips**](tcm-gettooltips.md) . Se si crea un controllo ToolTip personalizzato, non usare lo stile delle [**\_ descrizioni comandi di TCS**](tab-control-styles.md) .

## <a name="default-tab-control-message-processing"></a>Elaborazione dei messaggi di controllo scheda predefiniti

In questa sezione viene descritta l'elaborazione dei messaggi eseguita da un controllo struttura a schede. I messaggi specifici per i controlli struttura a schede sono descritti in altre sezioni di questa documentazione.



| Message                                                  | Elaborazione eseguita                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CAPTURECHANGED WM**](/windows/desktop/inputdev/wm-capturechanged) | Non esegue alcuna operazione se il controllo struttura a schede ha rilasciato l'acquisizione del mouse. Se un'altra finestra acquisisce il mouse e viene tenuto premuto un pulsante, il comando rilascia il pulsante.                                                                                                                                                                                                                                                                                                                |
| [**creazione di WM \_**](/windows/desktop/winmsg/wm-create)                 | Alloca e Inizializza una struttura di dati interna. Il controllo Crea un controllo ToolTip se viene specificato lo stile delle [**\_ descrizioni comandi di TCS**](tab-control-styles.md) .                                                                                                                                                                                                                                                                                                    |
| [**eliminazione di WM \_**](/windows/desktop/winmsg/wm-destroy)               | Libera le risorse allocate durante l'elaborazione di [**WM \_ create**](/windows/desktop/winmsg/wm-create) .                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)         | Restituisce una combinazione dei valori DLGC \_ WANTARROWS e DLGC \_ WANTCHARS.                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_tipo di carattere WM GetFont**](/windows/desktop/winmsg/wm-getfont)               | Restituisce l'handle per il tipo di carattere utilizzato per le etichette.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**KeyDown di WM \_**](/windows/desktop/inputdev/wm-keydown)               | Elabora i tasti di direzione e modifica la selezione, se appropriato.                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**\_KILLFOCUS WM**](/windows/desktop/inputdev/wm-killfocus)           | Invalida la scheda con lo stato attivo, in modo che venga ridisegnata per riflettere uno stato non attivo.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)       | Invia il messaggio al controllo ToolTip, se disponibile, e modifica la selezione se l'utente fa clic su una scheda. Se l'utente fa clic su un pulsante, il controllo ridisegni il pulsante per assegnare un aspetto incassato e acquisisce il mouse. Se l'utente fa clic su una scheda o un pulsante e viene specificato lo stile [**TCS \_ FOCUSONBUTTONDOWN**](tab-control-styles.md) , il controllo imposta lo stato attivo su se stesso.                                                     |
| [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)           | Rilascia il mouse se è stato premuto un pulsante. Se il cursore è posizionato sul pulsante e viene tenuto premuto, il controllo modifica la selezione di conseguenza e ridisegnato il pulsante.                                                                                                                                                                                                                                                                                                         |
| [**MOUSEMOVE di WM \_**](/windows/desktop/inputdev/wm-mousemove)           | Invia il messaggio al controllo ToolTip, se disponibile. Se viene specificato lo stile dei [**\_ pulsanti del TCS**](tab-control-styles.md) e il pulsante del mouse viene tenuto premuto dopo aver fatto clic, il controllo può anche ricreare il pulsante interessato per assegnargli un aspetto elevato o incassato.                                                                                                                                                                                            |
| [**\_notifica WM**](wm-notify.md)                          | Inoltra i codici di notifica inviati dal controllo ToolTip.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_disegno WM**](/windows/desktop/gdi/wm-paint)                            | Disegna un bordo intorno all'area di visualizzazione (a meno che non sia specificato lo stile dei [**\_ pulsanti TCS**](tab-control-styles.md) ) e disegna le schede che intersecano il rettangolo non valido. Per ogni scheda viene disegnato il corpo della scheda (oppure viene inviato un messaggio [**WM \_ DrawItem**](wm-drawitem.md) alla finestra padre), quindi viene disegnato un bordo intorno alla scheda. Se il parametro *wParam* è diverso da null, il controllo presuppone che il valore sia un HDC e i colori che usano tale contesto di dispositivo. |
| [**\_RBUTTONDOWN WM**](/windows/desktop/inputdev/wm-rbuttondown)       | Invia un codice di notifica [ \_ RCLICK Nm](nm-rclick-tab.md) alla finestra padre.                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**\_stato attivo WM**](/windows/desktop/inputdev/wm-setfocus)             | Invalida la scheda con lo stato attivo, in modo che venga ridisegnata per riflettere uno stato attivo.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_tipo di carattere WM**](/windows/desktop/winmsg/wm-setfont)               | Imposta il tipo di carattere utilizzato per le etichette.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**\_SETREDRAW WM**](/windows/desktop/gdi/wm-setredraw)                    | Imposta lo stato di un flag interno che determina se il controllo viene ridisegnato quando gli elementi vengono inseriti ed eliminati, quando viene modificato il tipo di carattere e così via.                                                                                                                                                                                                                                                                                                                      |
| [**\_dimensioni WM**](/windows/desktop/winmsg/wm-size)                     | Ricalcola le posizioni delle schede e può invalidare parte del controllo struttura a schede per forzare il ridisegno di alcune o tutte le schede.                                                                                                                                                                                                                                                                                                                                                             |



 

 

 