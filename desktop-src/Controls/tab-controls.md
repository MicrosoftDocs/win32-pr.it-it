---
title: Informazioni sui controlli Struttura a schede
description: Un controllo Struttura a schede è simile ai separatori in un blocco per appunti o alle etichette in un archivio. L'uso del controllo Struttura a schede consente a un'applicazione di definire più pagine per la stessa area di una finestra o una finestra di dialogo.
ms.assetid: 55ed2863-7f8d-43ce-a0f9-6f6d41e3f947
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 512955ec2b3426227366ef109669c52a6c07c8882374d935023123182de194ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670426"
---
# <a name="about-tab-controls"></a>Informazioni sui controlli Struttura a schede

Un controllo Struttura a schede è simile ai separatori in un blocco per appunti o alle etichette in un archivio. L'uso del controllo Struttura a schede consente a un'applicazione di definire più pagine per la stessa area di una finestra o una finestra di dialogo. Ogni pagina è costituita da un determinato tipo di informazioni o da un gruppo di controlli che l'applicazione visualizza quando l'utente seleziona la scheda corrispondente.

Lo screenshot seguente mostra un semplice controllo Struttura a schede che contiene schede per i giorni della settimana. La scheda Martedì è stata selezionata.

![Screenshot di una finestra delle proprietà con cinque schede, una per ogni giorno della settimana](images/tab-simple.png)

In questo argomento sono incluse le sezioni seguenti.

-   [Creazione di controlli Struttura a schede](#creating-tab-controls)
-   [Stili del controllo Tab](#tab-control-styles)
-   [Schede e attributi delle schede](#tabs-and-tab-attributes)
-   [Area di visualizzazione](#display-area)
-   [Selezione delle schede](#tab-selection)
-   [Elenchi di immagini del controllo Struttura a schede](#tab-control-image-lists)
-   [Dimensioni e posizione delle schede](#tab-size-and-position)
-   [Schede disegnate dal proprietario](#owner-drawn-tabs)
-   [Descrizioni comando del controllo Struttura a schede](#tab-control-tooltips)
-   [Elaborazione predefinita dei messaggi del controllo Struttura a schede](#default-tab-control-message-processing)

## <a name="creating-tab-controls"></a>Creazione di controlli Struttura a schede

È possibile creare un controllo Struttura a schede chiamando [**la funzione CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) specificando la classe di finestra [**\_ TABCONTROL WC.**](common-control-window-classes.md) Questa classe di finestra viene registrata quando viene caricata la DLL dei controlli comuni. Per assicurarsi che la DLL sia caricata, usare la [**funzione InitCommonControlsEx.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)

In Microsoft Visual Studio è possibile creare un controllo Struttura a schede usando la casella degli strumenti.

È possibile inviare messaggi a un controllo Struttura a schede per aggiungere schede e influire altrimenti sull'aspetto e sul comportamento del controllo. Ogni messaggio ha una macro corrispondente che è possibile usare invece di inviare il messaggio in modo esplicito. Non è possibile disabilitare una singola scheda in un controllo Struttura a schede. È tuttavia possibile disabilitare un controllo Struttura a schede in una finestra delle proprietà disabilitando la pagina corrispondente.

## <a name="tab-control-styles"></a>Stili del controllo Tab

È possibile applicare determinate caratteristiche ai controlli struttura a schede specificando gli stili del controllo Struttura a schede quando viene creato il controllo. Ad esempio, è possibile specificare l'allineamento e l'aspetto generale delle schede in un controllo Struttura a schede.

È possibile fare in modo che le schede si presentino come pulsanti specificando lo stile [**TCS \_ BUTTONS.**](tab-control-styles.md) Le schede in questo tipo di controllo struttura a schede devono avere la stessa funzione dei controlli pulsante. ciò significa che facendo clic su una scheda si dovrebbe eseguire un comando anziché visualizzare una pagina. Poiché l'area di visualizzazione in un controllo struttura a schede del pulsante non viene in genere utilizzata, non viene disegnato alcun bordo intorno a esso.

È possibile fare in modo che una scheda riceva lo stato attivo per l'input quando si fa clic specificando lo stile [**\_ FOCUSONBUTTONDOWN di TCS.**](tab-control-styles.md) Questo stile viene in genere usato solo con lo [**stile \_ TCS BUTTONS.**](tab-control-styles.md) È possibile specificare che una scheda non riceve lo stato attivo per l'input quando si fa clic con lo stile [**\_ FOCUSNEVER TCS.**](tab-control-styles.md)

Per impostazione predefinita, un controllo Struttura a schede visualizza solo una riga di schede. Se non tutte le schede possono essere visualizzate contemporaneamente, il controllo Struttura a schede visualizza un controllo di scorrimento in modo che l'utente possa scorrere altre schede nella visualizzazione. Se necessario, è possibile fare in modo che un controllo Struttura a schede visualizza più righe di schede specificando lo stile [**\_ MULTILINE TCS.**](tab-control-styles.md) Con questo stile, tutte le schede possono essere visualizzate contemporaneamente. Le schede sono allineate a sinistra all'interno di ogni riga, a meno che non si specifica lo stile [**\_ TCS RIGHTJUSTIFY.**](tab-control-styles.md) In questo caso, la larghezza di ogni scheda viene aumentata in modo che ogni riga di schede riempia l'intera larghezza del controllo struttura a schede.

Un controllo Struttura a schede ridimensiona automaticamente ogni scheda in base alla relativa icona, se presente, e alla relativa etichetta. Per assegnare a tutte le schede la stessa larghezza, è possibile specificare lo [**stile \_ TCS FIXEDWIDTH.**](tab-control-styles.md) Il controllo ridimensiona tutte le schede in modo che si adattino all'etichetta più ampia oppure è possibile assegnare una larghezza e un'altezza specifiche usando il messaggio [**\_ SETITEMSIZE di TCM.**](tcm-setitemsize.md) All'interno di ogni scheda, il controllo centra l'icona e l'etichetta, posizionando l'icona a sinistra dell'etichetta. È possibile forzare l'icona a sinistra, lasciando l'etichetta centrata, specificando lo stile [**\_ TCS FORCEICONLEFT.**](tab-control-styles.md) È possibile allineare a sinistra sia l'icona che l'etichetta usando lo stile [**\_ TCS FORCELABELLEFT.**](tab-control-styles.md) Non è possibile usare **lo stile \_ TCS FIXEDWIDTH** con [**lo stile \_ TCS RIGHTJUSTIFY.**](tab-control-styles.md)

È possibile specificare che la finestra padre disegna le schede nel controllo usando lo stile [**\_ TCS OWNERDRAWFIXED.**](tab-control-styles.md) Per altre informazioni, vedere [Schede disegnate dal proprietario.](#owner-drawn-tabs)

È possibile specificare che un controllo Struttura a schede creerà un controllo descrizione comando usando lo stile [**TCS \_ TOOLTIPS.**](tab-control-styles.md) Per altre informazioni, vedere Descrizioni [comando del controllo Struttura a schede.](#tab-control-tooltips)

## <a name="tabs-and-tab-attributes"></a>Schede e attributi delle schede

Ogni scheda in un controllo Struttura a schede è costituita da un'icona, un'etichetta e dati definiti dall'applicazione. Queste informazioni vengono specificate da una [**struttura TCITEM.**](/windows/win32/api/commctrl/ns-commctrl-tcitema) È possibile aggiungere schede a un controllo Struttura a schede, recuperare il numero di schede, recuperare e impostare il contenuto di una scheda ed eliminare le schede. Le schede sono identificate dal relativo indice in base zero.

Per aggiungere schede a un controllo Struttura a schede, usare il messaggio [**\_ INSERTITEM di TCM,**](tcm-insertitem.md) specificando la posizione dell'elemento e l'indirizzo di una [**struttura TCITEM.**](/windows/win32/api/commctrl/ns-commctrl-tcitema) È possibile recuperare e impostare il contenuto di una scheda esistente usando i messaggi [**\_ TCM GETITEM**](tcm-getitem.md) e [**\_ SETITEM TCM.**](tcm-setitem.md) Per ogni scheda è possibile specificare un'icona, un'etichetta o entrambe. È anche possibile specificare dati definiti dall'applicazione da associare alla scheda.

È possibile recuperare il numero corrente di schede usando il messaggio [**\_ TCM GETITEMCOUNT,**](tcm-getitemcount.md) eliminare una scheda usando il messaggio [**\_ TCM DELETEITEM**](tcm-deleteitem.md) ed eliminare tutte le schede in un controllo struttura a schede usando il messaggio [**TCM \_ DELETEALLITEMS.**](tcm-deleteallitems.md)

È possibile associare dati definiti dall'applicazione a ogni scheda. Ad esempio, è possibile salvare le informazioni su ogni pagina con la scheda corrispondente. Per impostazione predefinita, un controllo Struttura a schede alloca quattro byte aggiuntivi per scheda per i dati definiti dall'applicazione. È possibile modificare il numero di byte aggiuntivi per scheda usando il [**messaggio \_ TCM SETITEMEXTRA.**](tcm-setitemextra.md) È possibile usare questo messaggio solo quando il controllo Struttura a schede è vuoto.

I dati definiti dall'applicazione vengono specificati dal **membro lParam** della [**struttura TCITEM.**](/windows/win32/api/commctrl/ns-commctrl-tcitema) Se si usano più di 4 byte di dati definiti dall'applicazione, è necessario definire la propria struttura e usarla al posto di **TCITEM.** È possibile recuperare e impostare i dati definiti dall'applicazione nello stesso modo in cui si recuperano e si impostano altre informazioni su una scheda, usando i messaggi [**\_ TCM GETITEM**](tcm-getitem.md) e [**\_ SETITEM TCM.**](tcm-setitem.md)

Il primo membro della struttura deve essere una [**struttura TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) e i membri rimanenti devono specificare dati definiti dall'applicazione. **TCITEMHEADER è** identico a [**TCITEM,**](/windows/win32/api/commctrl/ns-commctrl-tcitema)ad eccezione del fatto che non ha il **membro lParam.** La differenza tra le dimensioni della struttura e la dimensione di **TCITEMHEADER** deve essere uguale al numero di byte aggiuntivi per scheda.

## <a name="display-area"></a>Area di visualizzazione

L'area di visualizzazione di un controllo Struttura a schede è l'area in cui un'applicazione visualizza la pagina corrente. In genere, un'applicazione crea una finestra figlio o una finestra di dialogo, impostando le dimensioni e la posizione della finestra in modo che si adattino all'area di visualizzazione. Dato il rettangolo della finestra per un controllo struttura a schede, è possibile calcolare il rettangolo di delimitazione dell'area di visualizzazione usando il messaggio [**\_ TCM ADJUSTRECT.**](tcm-adjustrect.md)

A volte l'area di visualizzazione deve avere dimensioni particolari, ad esempio le dimensioni di una finestra di dialogo figlio non modabile. Dato il rettangolo di delimitazione per l'area di visualizzazione, è possibile usare [**\_ TCM ADJUSTRECT**](tcm-adjustrect.md) per calcolare il rettangolo della finestra corrispondente per il controllo Struttura a schede.

## <a name="tab-selection"></a>Selezione delle schede

Quando l'utente seleziona una scheda, un controllo struttura a schede invia i codici di notifica della finestra padre sotto forma di [**messaggi WM \_ NOTIFY.**](wm-notify.md) Il codice di notifica [TCN \_ SELCHANGING](tcn-selchanging.md) viene inviato prima della modifica della selezione e il codice di notifica [TCN \_ SELCHANGE](tcn-selchange.md) viene inviato dopo la modifica della selezione.

È possibile elaborare [TCN \_ SELCHANGING](tcn-selchanging.md) per salvare lo stato della pagina in uscita. È possibile restituire **TRUE** per impedire la modifica della selezione. Ad esempio, potrebbe non essere necessario passare da una finestra di dialogo figlio in cui un controllo ha un'impostazione non valida.

È necessario elaborare [TCN \_ SELCHANGE](tcn-selchange.md) per visualizzare la pagina in ingresso nell'area di visualizzazione. Ciò potrebbe comportare semplicemente la modifica delle informazioni visualizzate in una finestra figlio. Più spesso, ogni pagina è costituita da una finestra figlio o da una finestra di dialogo. In questo caso, un'applicazione potrebbe elaborare questa notifica eliminando o nascondendo la finestra o la finestra di dialogo figlio in uscita e creando o visualizzando la finestra figlio o la finestra di dialogo in ingresso.

È possibile recuperare e impostare la selezione corrente usando i messaggi [**\_ TCM GETCURSEL**](tcm-getcursel.md) e [**\_ TCM SETCURSEL.**](tcm-setcursel.md)

## <a name="tab-control-image-lists"></a>Elenchi di immagini del controllo Struttura a schede

A ogni scheda può essere associata un'icona, specificata da un indice nell'elenco immagini per il controllo Struttura a schede. Quando viene creato, un controllo Struttura a schede non ha un elenco di immagini associato. Un'applicazione può creare un elenco di immagini usando la funzione [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) e quindi assegnarlo a un controllo Struttura a schede usando il messaggio [**\_ SETIMAGELIST TCM.**](tcm-setimagelist.md)

È possibile aggiungere immagini all'elenco di immagini di un controllo Struttura a schede esattamente come si farebbe con qualsiasi altro elenco di immagini. Tuttavia, un'applicazione deve rimuovere le immagini usando il messaggio [**\_ REMOVEIMAGE di TCM**](tcm-removeimage.md) anziché la [**funzione Remove di ImageList. \_**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) Questo messaggio garantisce che ogni scheda rimanga associata alla stessa immagine di prima.

L'eliminazione di un controllo Struttura a schede non elimina un elenco di immagini associato. È necessario eliminare l'elenco di immagini separatamente. Ciò è utile se si vuole assegnare lo stesso elenco di immagini a più controlli struttura a schede.

Per recuperare l'handle per l'elenco di immagini attualmente associato a un controllo Struttura a schede, è possibile usare il messaggio [**\_ TCM GETIMAGELIST.**](tcm-getimagelist.md)

## <a name="tab-size-and-position"></a>Dimensioni e posizione della scheda

Ogni scheda in un controllo Struttura a schede ha dimensioni e posizione. È possibile impostare le dimensioni delle schede, recuperare il rettangolo di delimitazione di una scheda o determinare quale scheda si trova in una posizione specificata.

Per i controlli struttura a schede disegnati dal proprietario e a larghezza fissa, è possibile impostare la larghezza e l'altezza esatte delle schede usando il messaggio [**\_ SETITEMSIZE di TCM.**](tcm-setitemsize.md) In altri controlli struttura a schede le dimensioni di ogni scheda vengono calcolate in base all'icona e all'etichetta per la scheda. Il controllo Struttura a schede include lo spazio per un bordo e un margine aggiuntivo. È possibile impostare lo spessore del margine usando il [**messaggio \_ TCM SETPADDING.**](tcm-setpadding.md)

È possibile determinare il rettangolo di delimitazione corrente per una scheda usando il messaggio [**\_ GETITEMRECT di TCM.**](tcm-getitemrect.md) È possibile determinare quale scheda, se presente, si trova in una posizione specificata usando il [**messaggio \_ HITTEST di TCM.**](tcm-hittest.md)

In un controllo Struttura a schede con lo stile [**TCS \_ MULTILINE**](tab-control-styles.md) è possibile determinare il numero corrente di righe di schede usando il messaggio [**\_ TCM GETROWCOUNT.**](tcm-getrowcount.md)

## <a name="owner-drawn-tabs"></a>Owner-Drawn schede

Se un controllo Struttura a schede ha lo stile [**\_ TCS OWNERDRAWFIXED,**](tab-control-styles.md) la finestra padre deve disegnare le schede elaborando il [**messaggio WM \_ DRAWITEM.**](wm-drawitem.md) Il controllo Struttura a schede invia questo messaggio ogni volta che è necessario disegnare una scheda. Il *parametro lParam* specifica l'indirizzo di una struttura [**DRAWITEMSTRUCT,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) che contiene l'indice della scheda, il rettangolo di delimitazione e il contesto di dispositivo (DC) in cui disegnare.

Per impostazione predefinita, **il membro itemData** di [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contiene il valore del membro **lParam** della [**struttura TCITEM.**](/windows/win32/api/commctrl/ns-commctrl-tcitema) Tuttavia, se si modifica la quantità di dati definiti dall'applicazione per scheda, **itemData** contiene invece l'indirizzo dei dati. È possibile modificare la quantità di dati definiti dall'applicazione per scheda usando il [**messaggio \_ TCM SETITEMEXTRA.**](tcm-setitemextra.md)

Per specificare le dimensioni degli elementi in un controllo Struttura a schede, la finestra padre deve elaborare il [**messaggio WM \_ MEASUREITEM.**](wm-measureitem.md) Poiché tutte le schede in un controllo Struttura a schede disegnate dal proprietario hanno le stesse dimensioni, questo messaggio viene inviato una sola volta. Non esiste uno stile di controllo struttura a schede per le schede disegnate dal proprietario di dimensioni variabili. È anche possibile impostare la larghezza e l'altezza delle schede usando il [**messaggio \_ SETITEMSIZE di TCM.**](tcm-setitemsize.md)

## <a name="tab-control-tooltips"></a>Descrizioni comando del controllo Struttura a schede

È possibile usare un controllo descrizione comando per fornire una breve descrizione di ogni scheda in un controllo Struttura a schede. Un controllo struttura a schede con lo stile [**\_ TOOLTIPS TCS**](tab-control-styles.md) crea un controllo descrizione comando quando viene creato ed elimina il controllo descrizione comando quando viene eliminato. È anche possibile creare un controllo descrizione comando e assegnarlo a un controllo Struttura a schede.

Se si usa un controllo descrizione comando con un controllo Struttura a schede, la finestra padre deve elaborare il codice di notifica [ \_ GETDISPINFO TTN](ttn-getdispinfo.md) per fornire una descrizione di ogni scheda su richiesta.

Per usare lo stesso controllo descrizione comando con più di un controllo struttura a schede, creare il controllo descrizione comando manualmente e assegnarlo al controllo struttura a schede usando il messaggio [**\_ TCM SETTOOLTIPS.**](tcm-settooltips.md) È possibile recuperare l'handle per il controllo descrizione comando corrente di un controllo Struttura a schede usando il messaggio [**\_ GETTOOLTIPS di TCM.**](tcm-gettooltips.md) Se si crea un controllo descrizione comando personalizzato, non è consigliabile usare lo [**stile \_ TOOLTIPS di TCS.**](tab-control-styles.md)

## <a name="default-tab-control-message-processing"></a>Elaborazione predefinita dei messaggi del controllo Struttura a schede

In questa sezione viene descritta l'elaborazione dei messaggi eseguita da un controllo Struttura a schede. I messaggi specifici dei controlli struttura a schede vengono illustrati in altre sezioni di questa documentazione.



| Message                                                  | Elaborazione eseguita                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAPTURECHANGED**](/windows/desktop/inputdev/wm-capturechanged) | Non esegue alcuna operazione se il controllo Struttura a schede ha rilasciato lo stesso mouse capture. Se un'altra finestra ha acquisito il mouse e viene premuto un pulsante, il comando rilascia il pulsante.                                                                                                                                                                                                                                                                                                                |
| [**CREAZIONE DI WM \_**](/windows/desktop/winmsg/wm-create)                 | Alloca e inizializza una struttura di dati interna. Il controllo crea un controllo descrizione comando se viene specificato lo stile [**\_ TOOLTIPS TCS.**](tab-control-styles.md)                                                                                                                                                                                                                                                                                                    |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)               | Libera le risorse allocate durante [**l'elaborazione WM \_ CREATE.**](/windows/desktop/winmsg/wm-create)                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | Restituisce una combinazione dei valori DLGC \_ WANTARROWS e DLGC \_ WANTCHARS.                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Restituisce l'handle per il tipo di carattere utilizzato per le etichette.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)               | Elabora le chiavi di direzione e modifica la selezione, se appropriato.                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)           | Invalida la scheda con lo stato attivo in modo che verrà ridisegnata per riflettere uno stato non attivo.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)       | Inoltra il messaggio al controllo descrizione comando, se presente, e modifica la selezione se l'utente fa clic su una scheda. Se l'utente fa clic su un pulsante, il controllo ridisegna il pulsante per ottenere un aspetto incassato e acquisisce il mouse. Se l'utente fa clic su una scheda o un pulsante e viene specificato lo stile [**\_ TCS FOCUSONBUTTONDOWN,**](tab-control-styles.md) il controllo imposta lo stato attivo su se stesso.                                                     |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)           | Rilascia il mouse se è stato premuto un pulsante. Se il cursore è posizionato sul pulsante e viene tenuto premuto, il controllo modifica la selezione di conseguenza e ridisegna il pulsante.                                                                                                                                                                                                                                                                                                         |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)           | Inoltra il messaggio al controllo della descrizione comando, se presente. Se viene specificato lo stile [**TCS \_ BUTTONS**](tab-control-styles.md) e il pulsante del mouse viene premuto dopo aver fatto clic, il controllo può anche ridisegnare il pulsante interessato per assegnargli un aspetto elevato o incassato.                                                                                                                                                                                            |
| [**WM \_ NOTIFY**](wm-notify.md)                          | Inoltra i codici di notifica inviati dal controllo descrizione comando.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                            | Disegna un bordo intorno all'area di visualizzazione (a meno che non sia specificato lo stile [**TCS \_ BUTTONS)**](tab-control-styles.md) e disegna le schede che intersecano il rettangolo non valido. Per ogni scheda, disegna il corpo della scheda (o invia un messaggio [**WM \_ DRAWITEM**](wm-drawitem.md) alla finestra padre) e quindi disegna un bordo intorno alla scheda. Se il *parametro wParam* è diverso da NULL, il controllo presuppone che il valore sia hdc e dipinge usando tale contesto di dispositivo. |
| [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)       | Invia un [codice \_ di notifica RCLICK](nm-rclick-tab.md) NM alla finestra padre.                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)             | Invalida la scheda con lo stato attivo in modo che verrà ridisegnata per riflettere uno stato attivo.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | Imposta il tipo di carattere utilizzato per le etichette.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw)                    | Imposta lo stato di un flag interno che determina se il controllo viene ridisegnato quando gli elementi vengono inseriti ed eliminati, quando il tipo di carattere viene modificato e così via.                                                                                                                                                                                                                                                                                                                      |
| [**DIMENSIONI \_ WM**](/windows/desktop/winmsg/wm-size)                     | Ricalcola le posizioni delle schede e può invalidare parte del controllo Struttura a schede per forzare il ridisegno di alcune o tutte le schede.                                                                                                                                                                                                                                                                                                                                                             |



 

 

 