---
title: Informazioni sulle caselle di riepilogo
description: In questa sezione vengono descritte le funzionalità della casella di riepilogo.
ms.assetid: 359bb363-5b97-4e0c-bdc4-bfa6a6504a76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674712226a79960e44ab99ed8e59c88b27984efb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474326"
---
# <a name="about-list-boxes"></a>Informazioni sulle caselle di riepilogo

Un controllo casella di riepilogo contiene un semplice elenco da cui l'utente può in genere selezionare uno o più elementi. Le caselle di riepilogo offrono una flessibilità limitata rispetto ai controlli di [visualizzazione elenco](list-view-control-reference.md) .

Gli elementi della casella di riepilogo possono essere rappresentati da stringhe di testo, bitmap o entrambi. Se la casella di riepilogo non è sufficientemente grande da visualizzare contemporaneamente tutti gli elementi della casella di riepilogo, la casella di riepilogo fornisce una barra di scorrimento. L'utente scorre gli elementi della casella di riepilogo e applica o rimuove lo stato di selezione secondo necessità. Quando si seleziona un elemento della casella di riepilogo, viene modificato l'aspetto visivo, in genere cambiando il testo e i colori di sfondo in quelli specificati dalle metriche del sistema operativo pertinenti. Quando l'utente seleziona o deseleziona un elemento, il sistema invia un messaggio di notifica alla finestra padre della casella di riepilogo.

Per un'applicazione ANSI, il sistema converte il testo in una casella di riepilogo in formato Unicode usando la tabella codici **CP \_ ACP** . Ciò può causare problemi. Ad esempio, i caratteri romani accentati in una casella di riepilogo non Unicode in Windows, la versione giapponese verrà distorta. Per risolvere questo problema, compilare l'applicazione come Unicode o utilizzare una casella di riepilogo creata dal proprietario.

In questa sezione vengono illustrati gli argomenti seguenti:

-   [Creazione di una casella di riepilogo](#creating-a-list-box)
-   [Tipi e stili di casella di riepilogo](#list-box-types-and-styles)
-   [Funzioni casella di riepilogo](#list-box-functions)
-   [Messaggi di notifica dalle caselle di riepilogo](#notification-messages-from-list-boxes)
-   [Messaggi in caselle di riepilogo](#notification-messages-from-list-boxes)
-   [Elaborazione predefinita dei messaggi della finestra](#default-window-message-processing)
-   [Caselle di riepilogo create dal proprietario](#owner-drawn-list-boxes)
-   [Trascinare le caselle di riepilogo](#drag-list-boxes)
    -   [Creazione di caselle di riepilogo di trascinamento](#creating-drag-list-boxes)
    -   [Trascinare i messaggi della casella di riepilogo](#drag-list-box-messages)
    -   [Trascinare i codici di notifica della casella di riepilogo](#drag-list-box-notification-codes)

## <a name="creating-a-list-box"></a>Creazione di una casella di riepilogo

Il modo più semplice per creare una casella di riepilogo in una finestra di dialogo consiste nel trascinarlo dalla casella degli strumenti in Microsoft Visual Studio sulla risorsa della finestra di dialogo. Per creare una casella di riepilogo in modo dinamico o per creare una casella di riepilogo in una finestra diversa da una finestra di dialogo, utilizzare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra della casella di riepilogo [**\_ WC**](common-control-window-classes.md) e gli stili appropriati della [casella di riepilogo](list-box-styles.md).

## <a name="list-box-types-and-styles"></a>Tipi e stili di casella di riepilogo

Sono disponibili due tipi di caselle di riepilogo: selezione singola (impostazione predefinita) e selezione multipla. In una casella di riepilogo a selezione singola, l'utente può selezionare un solo elemento alla volta. In una casella di riepilogo a selezione multipla, l'utente può selezionare più di un elemento alla volta. Per creare una casella di riepilogo a selezione multipla, specificare lo stile [**lbs \_ MULTIPLESEL**](list-box-styles.md) o [**\_ EXTENDEDSEL**](list-box-styles.md) .

L'aspetto e il funzionamento di una casella di riepilogo sono controllati dagli [stili della casella di riepilogo](list-box-styles.md) e dagli stili della finestra. Questi stili indicano se l'elenco è ordinato, disposto in più colonne, disegnato dall'applicazione e così via. Le dimensioni e gli stili di una casella di riepilogo vengono in genere definiti in un modello di finestra di dialogo incluso nelle risorse di un'applicazione.

> [!Note]  
> Per usare gli stili di visualizzazione con questi controlli, un'applicazione deve includere un manifesto e deve chiamare [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) all'inizio del programma. Per informazioni sugli stili di visualizzazione, vedere [stili di visualizzazione](themes-overview.md). Per informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="list-box-functions"></a>Funzioni casella di riepilogo

La funzione [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) sostituisce il contenuto di una casella di riepilogo con i nomi di unità, directory e file che corrispondono a un set di criteri specificato. La funzione [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) recupera la selezione corrente in una casella di riepilogo inizializzata da **DlgDirList**. Queste funzioni consentono all'utente di selezionare un'unità, una directory o un file da una casella di riepilogo senza digitare il percorso e il nome del file.

Inoltre, la funzione [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) restituisce il numero di elementi per colonna in una casella di riepilogo specificata.

## <a name="notification-messages-from-list-boxes"></a>Messaggi di notifica dalle caselle di riepilogo

Quando si verifica un evento in una casella di riepilogo, nella casella di riepilogo viene inviato un codice di notifica, sotto forma di un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) , alla routine della finestra di dialogo della finestra proprietaria. I codici di notifica della casella di riepilogo vengono inviati quando un utente seleziona, fa doppio clic o Annulla un elemento casella di riepilogo; Quando la casella di riepilogo riceve o perde lo stato attivo della tastiera; e quando il sistema non è in grado di allocare memoria sufficiente per una richiesta di casella di riepilogo. Un messaggio di **\_ comando WM** contiene l'identificatore della casella di riepilogo nella parola di basso livello del parametro *wParam* e il codice di notifica nella parola più significativa. Il parametro *lParam* contiene l'handle della finestra del controllo.

Una routine della finestra di dialogo non è necessaria per elaborare questi messaggi; la routine della finestra predefinita le elabora.

Un'applicazione deve monitorare ed elaborare i seguenti codici di notifica della casella di riepilogo.



| Codice di notifica                   | Descrizione                                                      |
|-------------------------------------|------------------------------------------------------------------|
| [\_DBLCLK LBN](lbn-dblclk.md)       | L'utente fa doppio clic su un elemento nella casella di riepilogo.                  |
| [\_ERRSPACE LBN](lbn-errspace.md)   | La casella di riepilogo non può allocare memoria sufficiente per soddisfare una richiesta. |
| [\_KILLFOCUS LBN](lbn-killfocus.md) | La casella di riepilogo perde lo stato attivo della tastiera.                           |
| [\_SELCANCEL LBN](lbn-selcancel.md) | L'utente annulla la selezione di un elemento nella casella di riepilogo.       |
| [\_selChange LBN](lbn-selchange.md) | La selezione in una casella di riepilogo sta per essere modificata.                  |
| [LBN \_ SetFocus](lbn-setfocus.md)   | La casella di riepilogo riceve lo stato attivo della tastiera.                        |



 

## <a name="messages-to-list-boxes"></a>Messaggi in caselle di riepilogo

Una routine della finestra di dialogo può inviare messaggi a una casella di riepilogo per aggiungere, eliminare, esaminare e modificare gli elementi della casella di riepilogo. Una routine della finestra di dialogo, ad esempio, può inviare un messaggio [**lb \_ ADDSTRING**](lb-addstring.md) a una casella di riepilogo per aggiungere un elemento e un messaggio [**lb \_ GETSEL**](lb-getsel.md) per determinare se l'elemento è selezionato. Altri messaggi impostano e recuperano informazioni sulle dimensioni, l'aspetto e il comportamento della casella di riepilogo. Il messaggio [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) , ad esempio, imposta la larghezza scorrevole di una casella di riepilogo. Una routine della finestra di dialogo può inviare qualsiasi messaggio a una casella di riepilogo utilizzando la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) .

Il relativo *Indice* fa spesso riferimento a un elemento casella di riepilogo, un numero intero che rappresenta la posizione dell'elemento nella casella di riepilogo. L'indice del primo elemento in una casella di riepilogo è 0, l'indice del secondo elemento è 1 e così via.

Nella tabella seguente viene descritto il modo in cui la procedura predefinita della casella di riepilogo risponde ai messaggi della casella di riepilogo.



| Message                                                   | Risposta                                                                                                                                                                                                                         |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AddFile lb**](lb-addfile.md)                         | Inserisce un file in una casella di riepilogo directory riempita dalla funzione [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) e recupera l'indice della casella di riepilogo dell'elemento inserito.                                                                  |
| [**\_ADDSTRING lb**](lb-addstring.md)                     | Aggiunge una stringa a una casella di riepilogo e ne restituisce l'indice.                                                                                                                                                                               |
| [**\_DELETESTRING lb**](lb-deletestring.md)               | Rimuove una stringa da una casella di riepilogo e restituisce il numero di stringhe rimaste nell'elenco.                                                                                                                                      |
| [**\_dir lb**](lb-dir.md)                                 | Aggiunge un elenco di nomi di file a una casella di riepilogo e restituisce l'indice dell'ultimo nome file aggiunto.                                                                                                                                       |
| [**\_FindString lb**](lb-findstring.md)                   | Restituisce l'indice della prima stringa nella casella di riepilogo che inizia con una stringa specificata.                                                                                                                                       |
| [**\_FINDEXACTSTRING lb**](lb-findstringexact.md)         | Restituisce l'indice della stringa nella casella di riepilogo uguale a una stringa specificata.                                                                                                                                             |
| [**\_GETANCHORINDEX lb**](lb-getanchorindex.md)           | Restituisce l'indice dell'ultimo elemento selezionato dal mouse.                                                                                                                                                                      |
| [**\_GETCARETINDEX lb**](lb-getcaretindex.md)             | Restituisce l'indice dell'elemento con il rettangolo di attivazione.                                                                                                                                                                      |
| [**CONTEGGIO di LB \_**](lb-getcount.md)                       | Restituisce il numero di elementi nella casella di riepilogo.                                                                                                                                                                                     |
| [**LB \_ GETcursel**](lb-getcursel.md)                     | Restituisce l'indice dell'elemento attualmente selezionato.                                                                                                                                                                                |
| [**\_GETHORIZONTALEXTENT lb**](lb-gethorizontalextent.md) | Restituisce la larghezza dello scorrimento, in pixel, di una casella di riepilogo.                                                                                                                                                                          |
| [**\_GETITEMDATA lb**](lb-getitemdata.md)                 | Restituisce il valore associato all'elemento specificato.                                                                                                                                                                    |
| [**\_GETITEMHEIGHT lb**](lb-getitemheight.md)             | Restituisce l'altezza, in pixel, di un elemento in una casella di riepilogo.                                                                                                                                                                         |
| [**\_GETITEMRECT lb**](lb-getitemrect.md)                 | Recupera le coordinate client dell'elemento della casella di riepilogo specificato.                                                                                                                                                                 |
| [**LB \_ GETlocale**](lb-getlocale.md)                     | Recupera le impostazioni locali della casella di riepilogo. La parola più significativa contiene il codice paese/area geografica e la parola di ordine inferiore contiene l'identificatore della lingua.                                                                              |
| [**\_GETSEL lb**](lb-getsel.md)                           | Restituisce lo stato di selezione di un elemento della casella di riepilogo.                                                                                                                                                                                  |
| [**\_GETSELCOUNT lb**](lb-getselcount.md)                 | Restituisce il numero di elementi selezionati in una casella di riepilogo a selezione multipla.                                                                                                                                                           |
| [**\_GETSELITEMS lb**](lb-getselitems.md)                 | Crea una matrice di indici di tutti gli elementi selezionati in una casella di riepilogo a selezione multipla e restituisce il numero totale di elementi selezionati.                                                                                           |
| [**GetText LB \_**](lb-gettext.md)                         | Recupera la stringa associata a un elemento specificato e la lunghezza della stringa.                                                                                                                                              |
| [**\_GETTEXTLEN lb**](lb-gettextlen.md)                   | Restituisce la lunghezza, in caratteri, della stringa associata a un elemento specificato.                                                                                                                                               |
| [**\_GETTOPINDEX lb**](lb-gettopindex.md)                 | Restituisce l'indice del primo elemento visibile in una casella di riepilogo.                                                                                                                                                                       |
| [**\_INITSTORAGE lb**](lb-initstorage.md)                 | Alloca memoria per il numero specificato di elementi e le relative stringhe associate.                                                                                                                                                 |
| [**\_INSERTSTRING lb**](lb-insertstring.md)               | Inserisce una stringa in corrispondenza di un indice specificato in una casella di riepilogo.                                                                                                                                                                             |
| [**\_ITEMFROMPOINT lb**](lb-itemfrompoint.md)             | Recupera l'indice in base zero dell'elemento più vicino al punto specificato in una casella di riepilogo.                                                                                                                                            |
| [**\_ResetContent lb**](lb-resetcontent.md)               | Rimuove tutti gli elementi da una casella di riepilogo.                                                                                                                                                                                               |
| [**\_SELECTSTRING lb**](lb-selectstring.md)               | Seleziona la prima stringa trovata che corrisponde a un prefisso specificato.                                                                                                                                                               |
| [**\_SELITEMRANGE lb**](lb-selitemrange.md)               | Seleziona un intervallo specificato di elementi in una casella di riepilogo.                                                                                                                                                                                |
| [**\_SELITEMRANGEEX lb**](lb-selitemrangeex.md)           | Seleziona un intervallo specificato di elementi se l'indice del primo elemento nell'intervallo è minore dell'indice dell'ultimo elemento nell'intervallo. Annulla la selezione nell'intervallo se l'indice del primo elemento è maggiore dell'ultimo. |
| [**\_SETANCHORINDEX lb**](lb-setanchorindex.md)           | Imposta l'ultimo elemento selezionato dal mouse su un elemento specificato.                                                                                                                                                                  |
| [**\_SETCARETINDEX lb**](lb-setcaretindex.md)             | Imposta il rettangolo di attivazione su un elemento della casella di riepilogo specificato.                                                                                                                                                                           |
| [**\_SETCOLUMNWIDTH lb**](lb-setcolumnwidth.md)           | Imposta la larghezza, in pixel, di tutte le colonne in una casella di riepilogo.                                                                                                                                                                         |
| [**\_conteggio lb**](lb-setcount.md)                       | Imposta il numero di elementi in una casella di riepilogo.                                                                                                                                                                                          |
| [**di \_ lb**](lb-setcursel.md)                     | Seleziona un elemento casella di riepilogo specificato.                                                                                                                                                                                               |
| [**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md) | Imposta la larghezza di scorrimento, in pixel, di una casella di riepilogo.                                                                                                                                                                             |
| [**\_SETITEMDATA lb**](lb-setitemdata.md)                 | Associa un valore a un elemento casella di riepilogo.                                                                                                                                                                                         |
| [**\_SETITEMHEIGHT lb**](lb-setitemheight.md)             | Imposta l'altezza, in pixel, di un elemento o di elementi in una casella di riepilogo.                                                                                                                                                                   |
| [**\_impostazioni locali lb**](lb-setlocale.md)                     | Imposta le impostazioni locali di una casella di riepilogo e restituisce l'identificatore delle impostazioni locali precedente.                                                                                                                                                        |
| [**\_SETSEL lb**](lb-setsel.md)                           | Seleziona un elemento in una casella di riepilogo a selezione multipla.                                                                                                                                                                                |
| [**\_SETTABSTOPS lb**](lb-settabstops.md)                 | Imposta le tabulazioni su quelle specificate in una matrice specificata.                                                                                                                                                                      |
| [**\_SETTOPINDEX lb**](lb-settopindex.md)                 | Scorre la casella di riepilogo in modo che l'elemento specificato si trovi all'inizio dell'intervallo visibile.                                                                                                                                                   |



 

## <a name="default-window-message-processing"></a>Elaborazione predefinita dei messaggi della finestra

La routine della finestra della casella di riepilogo predefinita esegue l'elaborazione predefinita per tutti i messaggi non elaborati dalla casella di riepilogo. Quando la procedura della casella di riepilogo restituisce **false** per un messaggio, la routine della finestra predefinita controlla il messaggio ed esegue le azioni predefinite, come illustrato nella tabella seguente.



| Message                                            | Azione predefinita                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_carattere WM**](/windows/desktop/inputdev/wm-char)                   | Sposta la selezione sul primo elemento che inizia con il carattere digitato dall'utente. Se nella casella di riepilogo è presente lo stile L [**BS \_ OWNERDRAW**](button-styles.md) , non si verificherà alcuna azione. Più caratteri digitati in un intervallo breve vengono considerati come un gruppo e viene selezionato il primo elemento che inizia con tale serie di caratteri.<br/> |
| [**creazione di WM \_**](/windows/desktop/winmsg/wm-create)                 | Crea una casella di riepilogo vuota.                                                                                                                                                                                                                                                                                                                                               |
| [**eliminazione di WM \_**](/windows/desktop/winmsg/wm-destroy)               | Elimina definitivamente la casella di riepilogo e libera tutte le risorse utilizzate.                                                                                                                                                                                                                                                                                                              |
|                                                    | Passa il messaggio alla routine della finestra di dialogo o al processo della finestra padre.                                                                                                                                                                                                                                                                                                 |
| [**\_Abilitazione WM**](/windows/desktop/winmsg/wm-enable)                 | Se il controllo è visibile, invalida il rettangolo in modo che le stringhe possano essere dipinte in grigio.                                                                                                                                                                                                                                                                                 |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd)         | Cancella lo sfondo di una casella di riepilogo. Se la casella di riepilogo ha lo stile L [**BS \_ OWNERDRAW**](button-styles.md) , lo sfondo non viene cancellato.                                                                                                                                                                                                                   |
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)         | Restituisce DLGC \_ WANTARROWS \| DLGC \_ WANTCHARS, che indica che la procedura predefinita per la casella di riepilogo elabora i tasti di direzione e i messaggi [**WM \_ char**](/windows/desktop/inputdev/wm-char) .                                                                                                                                                                                                      |
| [**\_tipo di carattere WM GetFont**](/windows/desktop/winmsg/wm-getfont)               | Restituisce un handle per il tipo di carattere corrente per la casella di riepilogo.                                                                                                                                                                                                                                                                                                                   |
| [**\_HSCROLL WM**](wm-hscroll.md)                  | Scorre orizzontalmente la casella di riepilogo.                                                                                                                                                                                                                                                                                                                                       |
| [**KeyDown di WM \_**](/windows/desktop/inputdev/wm-keydown)             | Elabora le chiavi virtuali per lo scorrimento. La chiave virtuale è l'indice dell'elemento a cui spostare il punto di inserimento. La selezione non viene modificata.                                                                                                                                                                                                                                       |
| [**\_KILLFOCUS WM**](/windows/desktop/inputdev/wm-killfocus)         | Disattiva il punto di inserimento e lo elimina. Invia un codice di notifica [LBN \_ KILLFOCUS](lbn-killfocus.md) al proprietario della casella di riepilogo.                                                                                                                                                                                                                                        |
| [**\_LBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-lbuttondblclk) | Tiene traccia del mouse nell'area client della casella di riepilogo. Ciò consente all'utente di annullare una selezione se il pulsante del mouse viene rilasciato all'esterno dell'area client della casella di riepilogo.                                                                                                                                                                                                              |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)     | Tiene traccia del mouse nell'area client della casella di riepilogo. Ciò consente all'utente di annullare una selezione se il pulsante del mouse viene rilasciato all'esterno dell'area client della casella di riepilogo.                                                                                                                                                                                                              |
| [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)         | Tiene traccia del mouse nell'area client della casella di riepilogo. Ciò consente all'utente di annullare una selezione se il pulsante del mouse viene rilasciato all'esterno dell'area client della casella di riepilogo.                                                                                                                                                                                                              |
| [**MOUSEMOVE di WM \_**](/windows/desktop/inputdev/wm-mousemove)         | Tiene traccia del mouse nell'area client della casella di riepilogo. Ciò consente all'utente di annullare una selezione se il pulsante del mouse viene rilasciato all'esterno dell'area client della casella di riepilogo.                                                                                                                                                                                                              |
| [**\_disegno WM**](/windows/desktop/gdi/wm-paint)                      | Esegue un'operazione di disegno sottoclassata usando l'handle della casella di riepilogo per il contesto di dispositivo (DC).                                                                                                                                                                                                                                                                           |
| [**\_stato attivo WM**](/windows/desktop/inputdev/wm-setfocus)           | Attiva il cursore e invia un codice di notifica [LBN \_ SetFocus](lbn-setfocus.md) al proprietario della casella di riepilogo.                                                                                                                                                                                                                                                        |
| [**\_tipo di carattere WM**](/windows/desktop/winmsg/wm-setfont)               | Imposta un nuovo tipo di carattere per la casella di riepilogo.                                                                                                                                                                                                                                                                                                                                        |
| [**\_SETREDRAW WM**](/windows/desktop/gdi/wm-setredraw)              | Imposta o cancella il flag di ritraccia in base al valore di *wParam*.                                                                                                                                                                                                                                                                                                           |
| [**\_dimensioni WM**](/windows/desktop/winmsg/wm-size)                     | Ridimensiona la casella di riepilogo in un numero integrale di elementi.                                                                                                                                                                                                                                                                                                                     |
| [**\_VSCROLL WM**](wm-vscroll.md)                  | Scorre verticalmente la casella di riepilogo.                                                                                                                                                                                                                                                                                                                                         |



 

La routine della casella di riepilogo predefinita passa tutti gli altri messaggi a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per l'elaborazione predefinita.

## <a name="owner-drawn-list-boxes"></a>Owner-Drawn caselle di riepilogo

Un'applicazione può creare una casella di riepilogo creata dal *proprietario* per la creazione degli elementi dell'elenco. La finestra padre o la finestra di dialogo di una casella di riepilogo creata dal proprietario (il *proprietario*) riceve i messaggi [**WM \_ DrawItem**](wm-drawitem.md) quando è necessario disegnare una parte della casella di riepilogo. In una casella di riepilogo creata dal proprietario è possibile elencare informazioni diverse dalle stringhe di testo o in aggiunta.

Il proprietario di una casella di riepilogo creata dal proprietario deve elaborare il messaggio [**WM \_ DrawItem**](wm-drawitem.md) . Questo messaggio viene inviato ogni volta che è necessario ricreare una parte della casella di riepilogo. Il proprietario potrebbe dover elaborare altri messaggi, a seconda degli stili specificati per la casella di riepilogo.

Un'applicazione può creare una casella di riepilogo creata dal proprietario specificando lo stile [**\_ OwnerDrawVariable**](list-box-styles.md) [**lbs \_ OwnerDrawFixed**](list-box-styles.md) o lbs. Se tutti gli elementi dell'elenco nella casella di riepilogo sono della stessa altezza, ad esempio stringhe o icone, un'applicazione può usare lo stile **\_ OwnerDrawFixed lbs** . Se gli elementi dell'elenco sono di altezza variabile (ad esempio, bitmap di dimensioni diverse), un'applicazione può usare lo stile **\_ OwnerDrawVariable lbs** .

Il proprietario di una casella di riepilogo creata dal proprietario può elaborare un messaggio [**WM \_ MeasureItem**](wm-measureitem.md) per specificare le dimensioni degli elementi dell'elenco. Se l'applicazione crea la casella di riepilogo usando lo [**stile \_ OwnerDrawFixed di lbs**](list-box-styles.md) , il sistema invia il messaggio **WM \_ MeasureItem** una sola volta. Le dimensioni specificate dal proprietario vengono utilizzate per tutti gli elementi dell'elenco. Se viene usato lo stile [**\_ OwnerDrawVariable di lbs**](list-box-styles.md) , il sistema invia un messaggio **WM \_ MeasureItem** per ogni elemento elenco aggiunto alla casella di riepilogo. Il proprietario può determinare o impostare l'altezza di un elemento di elenco in qualsiasi momento usando i messaggi [**lb \_ GETITEMHEIGHT**](lb-getitemheight.md) e [**lb \_ SETITEMHEIGHT**](lb-setitemheight.md) , rispettivamente.

Se le informazioni visualizzate in una casella di riepilogo creata dal proprietario includono testo, un'applicazione può tenere traccia del testo per ogni elemento dell'elenco specificando lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) . Le caselle di riepilogo con lo stile di [**\_ ordinamento lbs**](list-box-styles.md) sono ordinate in base a questo testo. Se una casella di riepilogo è ordinata, ma non è dello stile **\_ HASSTRINGS lbs** , il proprietario deve elaborare il messaggio [**WM \_ COMPAREITEM**](wm-compareitem.md) .

In una casella di riepilogo creata dal proprietario, il proprietario deve tenere traccia degli elementi elenco contenenti informazioni diverse da o oltre al testo. Un modo pratico per eseguire questa operazione consiste nel salvare l'handle delle informazioni come dati degli elementi usando il messaggio [**lb \_ SETITEMDATA**](lb-setitemdata.md) . Per liberare gli oggetti dati associati agli elementi in una casella di riepilogo, il proprietario può elaborare il messaggio [**WM \_ DeleteItem**](wm-deleteitem.md) .

Per un esempio di casella di riepilogo creata dal proprietario, vedere [come creare una Owner-Drawn casella di riepilogo](create-an-owner-drawn-list-box.md).

## <a name="drag-list-boxes"></a>Trascinare le caselle di riepilogo

Una casella di riepilogo di trascinamento è un tipo speciale di casella di riepilogo che consente all'utente di trascinare gli elementi da una posizione a un'altra. Un'applicazione può usare una casella di riepilogo di trascinamento per visualizzare le stringhe in una determinata sequenza e consentire all'utente di modificare la sequenza trascinando gli elementi in posizione.

### <a name="creating-drag-list-boxes"></a>Creazione di caselle di riepilogo di trascinamento

Trascinare le caselle di riepilogo hanno gli stessi stili di finestra ed elaborare gli stessi messaggi delle caselle di riepilogo standard. Per creare una casella di riepilogo di trascinamento, creare prima una casella di riepilogo standard e quindi chiamare la funzione [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) . Per convertire una casella di riepilogo in una finestra di dialogo in una casella di riepilogo di trascinamento, è possibile chiamare **MakeDragList** quando il \_ messaggio WM INITDIALOG viene elaborato.

### <a name="drag-list-box-messages"></a>Trascinare i messaggi della casella di riepilogo

Una casella di riepilogo di trascinamento notifica alla finestra padre degli eventi di trascinamento inviando un messaggio di elenco di trascinamento. La finestra padre deve elaborare il messaggio relativo all'elenco di trascinamento.

La casella di riepilogo di trascinamento registra questo messaggio quando viene chiamata la funzione [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) . Per recuperare l'identificatore del messaggio (valore numerico) del messaggio dell'elenco di trascinamento, chiamare la funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) e specificare il valore DRAGLISTMSGSTRING.

Il parametro *wParam* del messaggio di trascinamento dell'elenco è l'identificatore del controllo per la casella di riepilogo di trascinamento. Il parametro *lParam* è l'indirizzo di una struttura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) , che contiene il codice di notifica per l'evento di trascinamento e altre informazioni. Il valore restituito del messaggio dipende dalla notifica.

### <a name="drag-list-box-notification-codes"></a>Trascinare i codici di notifica della casella di riepilogo

Il codice di notifica dell'elenco di trascinamento, identificato dal membro **uNotification** della struttura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) inclusa nel messaggio dell'elenco di trascinamento, può essere [dl \_ BEGINDRAG](dl-begindrag.md), DL [ \_ trascinamento](dl-dragging.md), [dl \_ CANCELDRAG](dl-canceldrag.md)o [dl \_ eliminato](dl-dropped.md).

Il codice di notifica [ \_ BEGINDRAG DL](dl-begindrag.md) viene inviato quando il cursore si trova in una voce di elenco e l'utente fa clic con il pulsante sinistro del mouse. La finestra padre può restituire **true** per avviare l'operazione di trascinamento o **false** per non consentire il trascinamento. In questo modo, la finestra padre può abilitare il trascinamento per alcuni elementi dell'elenco e disabilitarlo per altri. È possibile determinare quale elemento dell'elenco si trova nella posizione specificata tramite la funzione [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) .

Se il trascinamento è attivo, il codice di notifica di [ \_ trascinamento DL](dl-dragging.md) viene inviato ogni volta che il mouse viene spostato o a intervalli regolari se il mouse non viene spostato. La finestra padre deve innanzitutto determinare l'elemento dell'elenco sotto il cursore utilizzando [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) , quindi tracciare l'icona Inserisci utilizzando la funzione [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) . Specificando **true** per il parametro *bAutoScroll* di **LBItemFromPt**, è possibile fare in modo che la casella di riepilogo scorra da una riga se il cursore si trova sopra o sotto la relativa area client. Il valore restituito per questa notifica specifica il tipo di cursore del mouse da impostare per la casella di riepilogo di trascinamento.

Il codice di notifica [ \_ CANCELDRAG DL](dl-canceldrag.md) viene inviato se l'utente annulla un'operazione di trascinamento facendo clic con il pulsante destro del mouse o premendo ESC. Il codice di notifica [ \_ eliminato DL](dl-dropped.md) viene inviato se l'utente completa un'operazione di trascinamento rilasciando il pulsante sinistro del mouse, anche se il cursore non si trova su un elemento dell'elenco. La casella di riepilogo di trascinamento rilascia il mouse capture prima di inviare una notifica. Il valore restituito di queste due notifiche viene ignorato. Trascina elenco

 

