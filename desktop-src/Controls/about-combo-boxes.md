---
title: Informazioni sulle caselle combinate
description: In questa sezione vengono illustrati i diversi tipi di caselle combinate.
ms.assetid: 76410a87-aa0e-4da9-9e78-c80ac485e3cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344596a3c0aa772568956344aaddcc053b534993
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104560137"
---
# <a name="about-combo-boxes"></a>Informazioni sulle caselle combinate

Una casella combinata combina una casella di modifica o un testo statico e un elenco.

In questo argomento sono contenute le sezioni seguenti.

-   [Tipi e stili di caselle combinate](#combo-box-types-and-styles)
-   [Elenco di caselle combinate](#combo-box-list)
    -   [Selezione corrente](#current-selection)
    -   [Elenchi a discesa](#drop-down-lists)
    -   [Contenuto elenco](#list-contents)
-   [Modificare i campi di selezione del controllo](#edit-control-selection-fields)
-   [Caselle combinate create dal proprietario](#owner-drawn-combo-boxes)
-   [Caselle combinate sottoclassi](#subclassed-combo-boxes)

## <a name="combo-box-types-and-styles"></a>Tipi e stili di caselle combinate

Una casella combinata è costituita da un elenco e da un campo di selezione. L'elenco presenta le opzioni che un utente può selezionare e il campo di selezione Visualizza la selezione corrente. Se il campo di selezione è un controllo di modifica, l'utente può immettere informazioni non disponibili nell'elenco; in caso contrario, l'utente può solo selezionare gli elementi nell'elenco.

La libreria di controlli comuni include tre stili principali della casella combinata, come illustrato nella tabella seguente.



| Tipo di casella combinata             | Costante Style                                                 | Descrizione                                                                                  |
|----------------------------|----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Semplice                     | [**\_semplice CBS**](combo-box-styles.md)             | Visualizza l'elenco in qualsiasi momento e Mostra l'elemento selezionato in un controllo di modifica.              |
| Drop-down                  | [**\_elenco a discesa CBS**](combo-box-styles.md)         | Visualizza l'elenco quando si fa clic sull'icona e Mostra l'elemento selezionato in un controllo di modifica.  |
| Elenco a discesa (elenco a discesa) | [**\_DropDownList CBS**](combo-box-styles.md) | Visualizza l'elenco quando si fa clic sull'icona e Mostra l'elemento selezionato in un controllo statico. |



 

Le schermate seguenti mostrano i tre tipi di casella combinata che potrebbero essere visualizzati in Windows Vista. Nella prima schermata, l'utente ha selezionato un elemento nella casella combinata semplice. L'utente può anche digitare un nuovo valore nella casella di modifica del controllo. L'elenco è stato dimensionato nell'editor di risorse Microsoft Visual Studio ed è sufficientemente grande da contenere due elementi.

![cattura di schermata che mostra un elemento selezionato in una casella combinata semplice](images/simplecombo.png)

Nella seconda schermata, l'utente ha digitato nuovo testo nel controllo di modifica della casella combinata a discesa. È anche possibile che l'utente abbia selezionato un elemento esistente. La casella di riepilogo si espande per contenere il maggior numero possibile di elementi.

![screenshot che mostra il testo digitato in una casella combinata a discesa](images/dropdown.png)

Nella terza schermata, l'utente ha aperto la casella combinata dell'elenco a discesa. La casella di riepilogo si espande per contenere il maggior numero possibile di elementi. L'utente non può immettere nuovo testo.

![screenshot che mostra un elemento selezionato in un elenco a discesa casella combinata](images/droplist.png)

Sono inoltre disponibili diversi stili di caselle combinate che definiscono proprietà specifiche. Gli stili della casella combinata definiscono proprietà specifiche di una casella combinata. È possibile combinare gli stili; Tuttavia, alcuni stili si applicano solo a determinati tipi di caselle combinate. Per una tabella di stili di caselle combinate, vedere [stili di caselle combinate](combo-box-styles.md).

> [!Note]  
> Per usare gli stili di visualizzazione con le caselle combinate, un'applicazione deve includere un manifesto e deve chiamare [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) all'inizio del programma. Per informazioni sugli stili di visualizzazione, vedere [stili di visualizzazione](themes-overview.md). Per informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="combo-box-list"></a>Elenco di caselle combinate

L'elenco è la parte di una casella combinata che consente di visualizzare gli elementi selezionabili da un utente. In genere, un'applicazione Inizializza il contenuto dell'elenco quando crea una casella combinata. Qualsiasi elemento elenco selezionato dall'utente è la *selezione corrente*. Non è possibile selezionare più elementi. Nelle caselle combinate semplici e a discesa l'utente può digitare il campo di selezione anziché selezionare un elemento dell'elenco. In questi casi, non è presente alcuna selezione corrente ed è responsabilità dell'applicazione aggiungere l'elemento all'elenco e impostarlo come selezione corrente, se è appropriato.

In questa sezione vengono illustrati gli argomenti seguenti:

-   [Selezione corrente](#current-selection)
-   [Elenchi a discesa](#drop-down-lists)
-   [Contenuto elenco](#list-contents)

### <a name="current-selection"></a>Selezione corrente

La selezione corrente è un elemento elenco selezionato dall'utente. il testo selezionato verrà visualizzato nel campo di selezione della casella combinata. Tuttavia, nel caso di una casella combinata semplice o di una casella combinata a discesa, la selezione corrente è solo una forma di possibile input utente in una casella combinata. L'utente può anche digitare il testo nel campo di selezione.

La selezione corrente è identificata dall'indice in base zero dell'elemento di elenco selezionato. Un'applicazione può impostarla e recuperarla in qualsiasi momento. La finestra padre o la routine della finestra di dialogo riceve una notifica quando l'utente modifica la selezione corrente per una casella combinata. La finestra padre o la finestra di dialogo non viene notificata quando l'applicazione modifica la selezione.

Quando viene creata una casella combinata, non è presente alcuna selezione corrente. Questo vale anche per una casella combinata semplice o a discesa, se l'utente ha modificato il contenuto del campo di selezione. Per impostare la selezione corrente, un'applicazione invia il messaggio di errore [**CB \_**](cb-setcursel.md) alla casella combinata. Un'applicazione può anche usare il messaggio [**CB \_ SELECTSTRING**](cb-selectstring.md) per impostare la selezione corrente su un elemento dell'elenco la cui stringa inizia con una stringa specificata. Per determinare la selezione corrente, un'applicazione invia il messaggio del [**CB \_ GetCurSel**](cb-getcursel.md) alla casella combinata. Se non è presente alcuna selezione corrente, questo messaggio restituisce CB \_ Err.

Quando l'utente modifica la selezione corrente in una casella combinata, la finestra padre o la routine della finestra di dialogo riceve un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) con il codice di notifica [CBN \_ selChange](cbn-selchange.md) nella parola più ordinata del parametro *wParam* . Questo codice di notifica non viene inviato quando la selezione corrente viene impostata tramite il messaggio di base [**CB \_**](cb-setcursel.md) .

Una casella combinata a discesa o una casella di riepilogo a discesa Invia il codice di notifica [ \_ primo piano CBN](cbn-closeup.md) alla finestra padre o alla procedura della finestra di dialogo quando l'elenco a discesa viene chiuso. Se l'utente ha modificato la selezione corrente, la casella combinata invia anche il codice di notifica di [CBN \_ selChange](cbn-selchange.md) quando l'elenco a discesa viene chiuso. Per eseguire un processo specifico ogni volta che l'utente seleziona una voce di elenco, è possibile gestire il \_ codice di notifica di CBN SelChange o CBN \_ closeup. In genere, è possibile attendere il \_ codice di notifica primo piano CBN prima di elaborare una modifica nella selezione corrente. Questo può essere particolarmente importante se è necessaria una quantità significativa di elaborazione.

Un'applicazione può anche elaborare i codici di notifica [CBN \_ SELENDOK](cbn-selendok.md) e [CBN \_ SELENDCANCEL](cbn-selendcancel.md) . Il sistema invia \_ SELENDOK CBN quando l'utente seleziona un elemento elenco o seleziona un elemento e quindi lo chiude. Indica che l'utente ha terminato e che la selezione deve essere elaborata. \_Il SELENDCANCEL CBN viene inviato quando l'utente seleziona un elemento, ma seleziona un altro controllo, preme ESC mentre l'elenco a discesa è aperto o chiude la finestra di dialogo. Indica che la selezione dell'utente deve essere ignorata. Il \_ SELENDOK CBN viene inviato prima di ogni messaggio [ \_ selChange CBN](cbn-selchange.md) .

In una casella combinata semplice, il sistema invia il codice di notifica di [CBN \_ DBLCLK](cbn-dblclk.md) quando l'utente fa doppio clic su un elemento dell'elenco. In una casella combinata a discesa o un elenco a discesa, un singolo clic nasconde l'elenco, quindi non è possibile fare doppio clic su un elemento.

### <a name="drop-down-lists"></a>Elenchi a discesa

Alcune notifiche e messaggi si applicano solo alle caselle combinate contenenti elenchi a discesa. Quando un elenco a discesa è aperto o chiuso, la finestra padre di una casella combinata riceve una notifica sotto forma di messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) . Se l'elenco viene aperto, la parola più significativa di *wParam* è l'elenco [a \_ discesa CBN](cbn-dropdown.md). Se l'elenco è in fase di chiusura, [il \_ primo è CBN](cbn-closeup.md).

Un'applicazione può aprire l'elenco di una casella combinata a discesa o una casella di riepilogo a discesa usando il messaggio [**CB \_ SHOWDROPDOWN**](cb-showdropdown.md) . Può determinare se l'elenco è aperto usando il messaggio [**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md) e può determinare le coordinate di un elenco a discesa usando il messaggio [**CB \_ GETDROPPEDCONTROLRECT**](cb-getdroppedcontrolrect.md) . Un'applicazione può anche aumentare la larghezza di un elenco a discesa usando il messaggio [**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md) .

### <a name="list-contents"></a>Contenuto elenco

Quando un'applicazione crea una casella combinata, in genere Inizializza la casella combinata aggiungendo uno o più elementi all'elenco. Successivamente, un'applicazione può aggiungere o eliminare elementi elenco, reinizializzare l'elenco o recuperare informazioni sugli elementi.

Un'applicazione aggiunge elementi elenco a una casella combinata inviando il messaggio [**CB \_ ADDSTRING**](cb-addstring.md) . L'elemento specificato viene aggiunto alla fine dell'elenco o, in una casella combinata ordinata, nella posizione corretta ordinata in base alla stringa dell'elemento. In una casella combinata non ordinata, un'applicazione può usare il messaggio [**CB \_ INSERTSTRING**](cb-insertstring.md) per inserire un elemento in una posizione specifica. Una volta aggiunto, una voce di elenco viene identificata dalla relativa posizione.

Utilizzando il messaggio [**CB \_ FindString**](cb-findstring.md) o [**CB \_ FindExactString**](cb-findstringexact.md) , un'applicazione può determinare la posizione di un elemento elenco. **CB \_ FINDSTRING** trova un elemento la cui stringa inizia con la stringa specificata. **CB \_ FINDEXACTSTRING** trova un elemento la cui stringa corrisponde esattamente alla stringa. Nessun messaggio fa distinzione tra maiuscole e minuscole.

Un'applicazione può rimuovere una voce di elenco usando il messaggio [**CB \_ DELETESTRING**](cb-deletestring.md) . Se un'applicazione deve reinizializzare l'elenco di caselle combinate, può innanzitutto cancellare l'intero contenuto usando il messaggio [**CB \_ ResetContent**](cb-resetcontent.md) . Quando si aggiungono più elementi all'elenco dopo che è già stata visualizzata una casella combinata, un'applicazione può deselezionare il flag di ridisegno per impedire che la casella combinata venga ridisegnata dopo l'aggiunta di ogni elemento. Per ulteriori informazioni sul ridisegno, vedere la descrizione del messaggio [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw) .

Per recuperare la stringa associata a un elemento elenco, un'applicazione può usare il [**messaggio \_ GETLBTEXT CB**](cb-getlbtext.md) . La stringa dell'elemento viene copiata nel buffer specificato dall'applicazione. Per assicurarsi che il buffer sia sufficientemente grande da ricevere la stringa, l'applicazione può innanzitutto usare il messaggio [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) per determinare la lunghezza della stringa. Per ottenere il numero di voci di elenco in una casella combinata, un'applicazione può usare il messaggio [**CB \_ GetCount**](cb-getcount.md) .

## <a name="edit-control-selection-fields"></a>Modificare i campi di selezione del controllo

Un'applicazione può recuperare o impostare il contenuto del campo di selezione ed è in grado di determinare o impostare la selezione di modifica. L'applicazione può anche limitare la quantità di testo che un utente può digitare nel campo di selezione. Quando il contenuto del campo di selezione viene modificato, il sistema invia messaggi di notifica alla finestra padre o alla routine della finestra di dialogo.

Per recuperare il contenuto del campo di selezione, un'applicazione può inviare il messaggio [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext) alla casella combinata. Per impostare il contenuto del campo di selezione di una casella combinata semplice o a discesa, un'applicazione può inviare il messaggio [**di \_ testo WM**](/windows/desktop/winmsg/wm-settext) alla casella combinata.

La selezione di modifica è l'intervallo di testo selezionato, se presente, nel campo di selezione di una casella combinata semplice o a discesa. Un'applicazione può determinare le posizioni dei caratteri iniziale e finale della selezione corrente usando il messaggio [**CB \_ GETEDITSEL**](cb-geteditsel.md) . Può anche selezionare i caratteri nella selezione di modifica usando il messaggio [**CB \_ SETEDITSEL**](cb-seteditsel.md) .

Inizialmente, la quantità di testo che l'utente può digitare nel campo di selezione è limitata dalla dimensione del campo di selezione. Tuttavia, se la casella combinata ha lo stile [**CBS \_ AUTOHSCROLL**](combo-box-styles.md) , il testo può continuare oltre le dimensioni del campo di selezione. Un'applicazione può usare il messaggio [**CB \_ LIMITTEXT**](cb-limittext.md) per limitare la quantità di testo che un utente può digitare nel campo di selezione, indipendentemente dal fatto che il controllo abbia lo stile **\_ AUTOHSCROLL CBS** .

Quando l'utente modifica il contenuto del campo di selezione, la finestra padre o la routine della finestra di dialogo riceve i messaggi di notifica. Il codice di notifica di [CBN \_ EDITUPDATE](cbn-editupdate.md) viene inviato per primo, a indicare che il testo nel campo di selezione è stato modificato. Una volta visualizzato il testo modificato, il sistema invia [il \_ EDITCHANGE CBN](cbn-editchange.md). Quando il contenuto del campo di selezione viene modificato in seguito alla selezione di un elemento elenco, questi messaggi non vengono inviati.

## <a name="owner-drawn-combo-boxes"></a>Owner-Drawn caselle combinate

Un'applicazione può creare una casella combinata creata dal proprietario per avere la responsabilità di disegnare gli elementi dell'elenco. La finestra padre di una casella combinata creata dal proprietario (il proprietario) riceve i messaggi [**WM \_ DrawItem**](wm-drawitem.md) quando è necessario disegnare una parte della casella combinata. Una casella combinata creata dal proprietario può elencare informazioni diverse da, o in aggiunta a, stringhe di testo. Le caselle combinate create dal proprietario possono essere di qualsiasi tipo. Tuttavia, il controllo di modifica in una casella combinata semplice o a discesa può visualizzare solo testo, mentre il proprietario dipinge il campo di selezione in una casella di riepilogo a discesa.

Il proprietario di una casella combinata creata dal proprietario deve elaborare il messaggio [**WM \_ DrawItem**](wm-drawitem.md) . Questo messaggio viene inviato ogni volta che è necessario ricreare una parte della casella combinata. Il proprietario potrebbe dover elaborare altri messaggi, a seconda degli stili specificati per la casella combinata.

Un'applicazione può creare una casella combinata creata dal proprietario specificando lo stile [**CBS \_ OwnerDrawFixed**](combo-box-styles.md) o [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) . Se tutti gli elementi dell'elenco nella casella combinata hanno la stessa altezza, ad esempio stringhe o icone, un'applicazione può usare lo stile **CBS \_ OwnerDrawFixed** . Se gli elementi dell'elenco hanno un'altezza variabile, ad esempio bitmap di dimensioni diverse, un'applicazione può usare lo stile **\_ OwnerDrawVariable CBS** .

Il proprietario di una casella combinata creata dal proprietario può elaborare un messaggio [**WM \_ MeasureItem**](wm-measureitem.md) per specificare le dimensioni degli elementi dell'elenco nella casella combinata. Se l'applicazione crea la casella combinata usando lo stile [**CBS \_ OwnerDrawFixed**](combo-box-styles.md) , il sistema invia il messaggio **WM \_ MeasureItem** una sola volta. Le dimensioni specificate dal proprietario vengono utilizzate per tutti gli elementi dell'elenco. Se viene usato lo stile [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) , il sistema invia un messaggio **WM \_ MeasureItem** per ogni elemento elenco aggiunto alla casella combinata. Il proprietario può determinare o impostare l'altezza di un elemento di elenco in qualsiasi momento usando i messaggi [**CB \_ GETITEMHEIGHT**](cb-getitemheight.md) e [**CB \_ SETITEMHEIGHT**](cb-setitemheight.md) , rispettivamente.

Se le informazioni visualizzate in una casella combinata creata dal proprietario includono testo, un'applicazione può tenere traccia del testo per ogni elemento dell'elenco specificando lo [**stile \_ HASSTRINGS CBS**](combo-box-styles.md) . Le caselle combinate con lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) sono ordinate in base a questo testo. Se una casella combinata è ordinata e non dello stile **CBS \_ HASSTRINGS** , il proprietario deve elaborare il messaggio [**WM \_ COMPAREITEM**](wm-compareitem.md) .

In una casella combinata creata dal proprietario, il proprietario deve tenere traccia degli elementi elenco contenenti informazioni diverse da o oltre al testo. Un modo pratico per eseguire questa operazione consiste nel salvare l'handle nelle informazioni come dati dell'elemento. Per liberare gli oggetti dati associati agli elementi di una casella combinata, il proprietario può elaborare il messaggio [**WM \_ DeleteItem**](wm-deleteitem.md) .

## <a name="subclassed-combo-boxes"></a>Caselle combinate sottoclassi

La sottoclasse è una procedura che consente a un'applicazione di intercettare ed elaborare i messaggi inviati o pubblicati in una finestra. Utilizzando la sottoclasse, un'applicazione può sostituire la propria elaborazione per determinati messaggi, lasciando la maggior parte dell'elaborazione del messaggio alla routine della finestra definita dalla classe.

Quando il sistema operativo crea una finestra, Salva le relative informazioni in una struttura di dati interna che include un puntatore alla routine della finestra. Per sottoporre a una sottoclasse una finestra, un'applicazione chiama la funzione [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) per sostituire il puntatore alla procedura con un puntatore a una routine di sottoclasse definita dall'applicazione. Successivamente, tutti i messaggi alla finestra vengono inviati alla procedura di sottoclasse. Questa procedura usa quindi la funzione [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) per passare i messaggi non elaborati alla routine della finestra originale. Per una descrizione dell'elaborazione dei messaggi eseguita dalla procedura della finestra della classe COMBOBOX, vedere [comportamento predefinito della casella combinata](combo-box-features.md).

Quando la casella combinata si trova al di fuori di una finestra di dialogo, un'applicazione non può elaborare la scheda, immettere ed eseguire il tasto ESC, a meno che non utilizzi una routine di sottoclasse. Quando una casella combinata semplice o a discesa riceve lo stato attivo per l'input, imposta immediatamente lo stato attivo sul relativo controllo di modifica figlio. Un'applicazione deve quindi sottoporre a sottoclasse il controllo Edit per intercettare l'input da tastiera per una casella combinata semplice o a discesa. Per un esempio, vedere la pagina relativa alla [sottoclasse di una casella combinata](using-combo-boxes.md).

Se una routine di sottoclasse elabora il messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) , è necessario utilizzare la funzione [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) per prepararsi per il disegno. Prima di chiamare la funzione [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) , passa l'handle del contesto di dispositivo (DC) come parametro *wParam* per la routine della finestra. Se **EndPaint** viene chiamato per primo, la routine della finestra della classe non esegue il disegno perché **EndPaint** convalida l'intera finestra.

Una tecnica correlata alla sottoclasse è la superclasse. Una superclasse è simile a qualsiasi altra classe con la differenza che la routine della finestra non chiama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per gestire i messaggi non elaborati. Passa invece messaggi non elaborati alla routine della finestra per la classe della finestra padre. Seguire le linee guida nelle [procedure di Windows](/windows/desktop/winmsg/window-procedures) per evitare problemi che possono verificarsi con la sottoclasse e la superclasse.

 

 