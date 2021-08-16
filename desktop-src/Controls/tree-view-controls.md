---
title: Informazioni Tree-View seguenti
description: Un controllo visualizzazione albero è una finestra che visualizza un elenco gerarchico di elementi, ad esempio le intestazioni di un documento, le voci in un indice o i file e le directory su disco.
ms.assetid: 10cc7949-dd77-412d-bad1-db8d8a049582
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08743a7ac138a6cea5f766dd91aee2ec714acc2d4c8b98e1f2bee26c42ff9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769813"
---
# <a name="about-tree-view-controls"></a>Informazioni Tree-View seguenti

Un controllo visualizzazione albero è una finestra che visualizza un elenco gerarchico di elementi, ad esempio le intestazioni di un documento, le voci in un indice o i file e le directory su disco. Ogni elemento è costituito da un'etichetta e un'immagine bitmap facoltativa e a ogni elemento può essere associato un elenco di elementi secondari. Facendo clic su un elemento, l'utente può espandere o comprimere l'elenco associato di elementi secondari.

Nella figura seguente viene illustrato un controllo visualizzazione albero semplice con un nodo radice, un nodo espanso e un nodo compresso. Il controllo usa una bitmap per l'elemento selezionato e un'altra bitmap per altri elementi.

![Screenshot che mostra cinque nodi in una gerarchia. il testo di un nodo è selezionato, ma i nodi non sono collegati tra loro tramite righe](images/tv-simple.png)

Dopo aver creato un controllo di visualizzazione albero, è possibile aggiungere, rimuovere, disporre o modificare in altro modo gli elementi inviando messaggi al controllo. Ogni messaggio ha una o più macro corrispondenti che è possibile usare invece di inviare il messaggio in modo esplicito.

In questa sezione vengono descritti gli argomenti seguenti.

-   [Stili di visualizzazione albero](#tree-view-styles)
-   [Elementi padre e figlio](#parent-and-child-items)
-   [Etichette degli elementi](#item-labels)
-   [Modifica delle etichette della visualizzazione struttura ad albero](#tree-view-label-editing)
-   [Posizione dell'elemento della visualizzazione albero](#tree-view-item-position)
-   [Panoramica degli stati degli elementi della visualizzazione albero](#tree-view-item-states-overview)
-   [Selezione dell'elemento](#item-selection)
-   [Informazioni sull'elemento](#item-information)
-   [Elenchi di immagini con visualizzazione albero](#tree-view-image-lists)
-   [Operazioni di trascinamento della selezione](#drag-and-drop-operations)
-   [Messaggi di notifica del controllo Visualizzazione struttura ad albero](#tree-view-control-notification-messages)
-   [Impostazione predefinita Tree-View'elaborazione dei messaggi di controllo](#default-tree-view-control-message-processing)
-   [Argomenti correlati](#related-topics)

## <a name="tree-view-styles"></a>Tree-View stili

Gli stili di visualizzazione albero regolano gli aspetti dell'aspetto di un controllo visualizzazione albero. Gli stili iniziali vengono impostati quando si crea il controllo visualizzazione albero. È possibile recuperare e modificare gli stili dopo aver creato il controllo visualizzazione albero usando le [**funzioni GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) [**e SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

Lo [**stile \_ TVS HASLINES**](tree-view-control-window-styles.md) migliora la rappresentazione grafica della gerarchia di un controllo visualizzazione albero disegnando linee che collegano elementi figlio all'elemento padre, come illustrato nella figura seguente.

![Screenshot che mostra la disposizione precedente, ma con linee che uniscono i nodi; la prima riga scende dal nodo radice](images/tv-haslines.png)

Questo stile di per sé non disegna linee nella radice della gerarchia. A tale scopo, è necessario combinare gli stili [**\_ TVS HASLINES**](tree-view-control-window-styles.md) e [**\_ TVS LINESATROOT.**](tree-view-control-window-styles.md) Il risultato è illustrato nella figura seguente.

![Screenshot che mostra la disposizione precedente, ma con una linea orizzontale aggiuntiva che porta al nodo radice](images/tv-rootlines.png)

L'utente può espandere o comprimere l'elenco di elementi figlio di un elemento padre facendo doppio clic sull'elemento padre. Un controllo di visualizzazione albero con lo stile [**\_ TVS HASBUTTONS**](tree-view-control-window-styles.md) aggiunge un pulsante a sinistra di ogni elemento padre. L'utente può fare clic sul pulsante una sola volta anziché fare doppio clic sull'elemento padre per espandere o comprimere l'elemento figlio. **TVS \_ HASBUTTONS** non aggiunge pulsanti agli elementi nella radice della gerarchia. A tale scopo, è necessario combinare [**TVS \_ HASLINES,**](tree-view-control-window-styles.md) [**TVS \_ LINESATROOT**](tree-view-control-window-styles.md)e **TVS \_ HASBUTTONS**. Questa combinazione di stili è illustrata nella figura seguente.

![Screenshot che mostra la disposizione precedente, ma con pulsanti espandi/comprimi in ogni vertice di due righe](images/tv-hasbuttons.png)

Lo [**stile TVS \_ CHECKBOXES**](tree-view-control-window-styles.md) crea caselle di controllo accanto a ogni elemento. Se si vuole usare lo stile della casella di controllo, è necessario impostare lo stile **TVS \_ CHECKBOXES** (con [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)) dopo aver creato il controllo visualizzazione albero e prima di popolare l'albero. In caso contrario, le caselle di controllo potrebbero essere deselezionate, a seconda dei problemi di temporizzazione. Nella figura seguente viene illustrato lo stile della casella di controllo.

![Screenshot che mostra la disposizione precedente, ma con una casella di controllo accanto a ogni nodo. due delle caselle di controllo sono selezionate](images/tv-haschecks.png)

Lo [**stile TVS \_ FULLROWSELECT**](tree-view-control-window-styles.md) fa sì che l'evidenziazione della selezione si estenda sull'intera larghezza del controllo, non solo sull'elemento stesso. Nella figura seguente viene illustrato questo stile.

![Screenshot che mostra la disposizione originale di cinque nodi senza linee, ma l'evidenziazione della selezione estende l'intera larghezza del controllo](images/tv-fullrow.png)

Lo [**stile \_ TVS EDITLABELS**](tree-view-control-window-styles.md) consente all'utente di modificare le etichette degli elementi della visualizzazione albero. Per altre informazioni sulla modifica delle etichette, vedere [Modifica delle etichette della visualizzazione ad albero](#tree-view-label-editing).

Per altre informazioni su questi e altri stili, vedere Stili della finestra del controllo Visualizzazione [struttura ad albero](tree-view-control-window-styles.md).

## <a name="parent-and-child-items"></a>Elementi padre e figlio

A qualsiasi elemento di un controllo di visualizzazione albero può essere associato un elenco di elementi secondari, denominati *elementi* figlio. Un elemento con uno o più elementi figlio è denominato *elemento padre.* Un elemento figlio viene visualizzato sotto l'elemento padre e rientrato per indicare che è subordinato all'elemento padre. Un elemento che non ha elementi padre viene visualizzato nella parte superiore della gerarchia e viene chiamato *elemento radice*.

Per aggiungere un elemento a un controllo di visualizzazione albero, inviare il [**messaggio \_ TVM INSERTITEM**](tvm-insertitem.md) al controllo. Il messaggio restituisce un handle per il tipo HTREEITEM, che identifica in modo univoco l'elemento. Quando si aggiunge un elemento, è necessario specificare l'handle per l'elemento padre del nuovo elemento. Se si specifica **NULL** o il valore TVI ROOT anziché un handle di elemento padre nella \_ struttura [**TVINSERTSTRUCT,**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) l'elemento viene aggiunto come elemento radice.

In qualsiasi momento, lo stato dell'elenco di elementi figlio di un elemento padre può essere espanso o compresso. Quando lo stato viene espanso, gli elementi figlio vengono visualizzati sotto l'elemento padre. Quando viene compresso, gli elementi figlio non vengono visualizzati. L'elenco passa automaticamente tra gli stati espansi e compressi quando l'utente fa doppio clic sull'elemento padre o, se l'elemento padre ha lo stile [**\_ TVS HASBUTTONS,**](tree-view-control-window-styles.md) quando l'utente fa clic sul pulsante associato all'elemento padre. Un'applicazione può espandere o comprimere gli elementi figlio usando il [**messaggio TVM \_ EXPAND.**](tvm-expand.md)

Un controllo visualizzazione albero invia alla finestra padre un messaggio di notifica [ \_ TVN ITEMEXPANDING](tvn-itemexpanding.md) quando l'elenco di elementi figlio di un elemento padre sta per essere espanso o compresso. La notifica offre a un'applicazione la possibilità di impedire la modifica o di impostare gli attributi dell'elemento padre che dipendono dallo stato dell'elenco di elementi figlio. Dopo aver modificato lo stato dell'elenco, il controllo visualizzazione albero invia alla finestra padre un messaggio di notifica [ \_ TVN ITEMEXPANDED.](tvn-itemexpanded.md)

Quando un elenco di elementi figlio viene espanso, viene rientrato rispetto all'elemento padre. È possibile impostare la quantità di rientro usando il messaggio [**\_ TVM SETINDENT**](tvm-setindent.md) o recuperare la quantità corrente usando il [**messaggio TVM \_ GETINDENT.**](tvm-getindent.md)

Un controllo visualizzazione albero usa la memoria allocata dall'heap del processo che crea il controllo visualizzazione albero. Il numero massimo di elementi in una visualizzazione albero è basato sulla quantità di memoria disponibile nell'heap.

## <a name="item-labels"></a>Etichette degli elementi

In genere si specifica il testo dell'etichetta di un elemento quando si aggiunge l'elemento al controllo visualizzazione albero. Il [**messaggio TVM \_ INSERTITEM**](tvm-insertitem.md) include una [**struttura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che definisce le proprietà dell'elemento, inclusa una stringa contenente il testo dell'etichetta.

Un controllo visualizzazione albero alloca memoria per l'archiviazione di ogni elemento. il testo delle etichette degli elementi occupa una parte significativa di questa memoria. Se l'applicazione gestisce una copia delle stringhe nel controllo visualizzazione albero, è possibile ridurre i requisiti di memoria del controllo specificando il valore LPSTR TEXTCALLBACK nel membro \_ **pszText** di [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) anziché passare le stringhe effettive alla visualizzazione albero. L'uso di LPSTR TEXTCALLBACK fa sì che il controllo visualizzazione albero recuperi il testo dell'etichetta di un elemento dalla finestra padre ogni volta che \_ l'elemento deve essere ridisegnato. Per recuperare il testo, il controllo visualizzazione albero invia un messaggio di notifica [ \_ TVN GETDISPINFO,](tvn-getdispinfo.md) che include l'indirizzo di [**una struttura NMTVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) La finestra padre deve riempire i membri appropriati della struttura inclusa.

## <a name="tree-view-label-editing"></a>Tree-View di etichette

L'utente può modificare direttamente le etichette degli elementi in un controllo di visualizzazione albero con lo stile [**\_ TVS EDITLABELS.**](tree-view-control-window-styles.md) L'utente inizia la modifica facendo clic sull'etichetta dell'elemento con lo stato attivo. Un'applicazione inizia la modifica usando il [**messaggio \_ TVM EDITLABEL.**](tvm-editlabel.md) Il controllo visualizzazione albero invia una notifica alla finestra padre quando inizia la modifica e quando viene annullata o completata. Al termine della modifica, la finestra padre è responsabile dell'aggiornamento dell'etichetta dell'elemento, se appropriato.

Quando inizia la modifica delle etichette, un controllo visualizzazione albero invia alla finestra padre [un messaggio di notifica \_ TVN BEGINLABELEDIT.](tvn-beginlabeledit.md) Elaborando questa notifica, un'applicazione può consentire la modifica di alcune etichette e impedire la modifica di altre. La restituzione di zero consente la modifica e la restituzione di un valore diverso da zero ne impedisce la modifica.

Quando la modifica delle etichette viene annullata o completata, un controllo visualizzazione albero invia alla finestra padre un messaggio di notifica [ \_ TVN ENDLABELEDIT.](tvn-endlabeledit.md) Il *parametro lParam* è l'indirizzo di una [**struttura NMTVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) Il *parametro item* è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che identifica l'elemento e include il testo modificato. La finestra padre è responsabile dell'aggiornamento dell'etichetta dell'elemento se vuole mantenere la nuova etichetta. Il **membro pszText** di **TVITEM** è zero se la modifica viene annullata.

Durante la modifica delle etichette, in genere in risposta al messaggio di notifica [TVN \_ BEGINLABELEDIT,](tvn-beginlabeledit.md) è possibile recuperare l'handle per il controllo di modifica usato per la modifica delle etichette usando il [**messaggio TVM \_ GETEDITCONTROL.**](tvm-geteditcontrol.md) È possibile inviare al controllo di modifica un messaggio [**EM \_ SETLIMITTEXT**](em-setlimittext.md) per limitare la quantità di testo che un utente può immettere o sottoclassare nel controllo di modifica per intercettare ed eliminare i caratteri non validi. Si noti, tuttavia, che il controllo di modifica viene visualizzato solo *dopo l'invio* di TVN \_ BEGINLABELEDIT.

## <a name="tree-view-item-position"></a>Tree-View posizione dell'elemento

La posizione iniziale di un elemento viene impostata quando l'elemento viene aggiunto al controllo visualizzazione albero tramite il [**messaggio \_ INSERTITEM di TVM.**](tvm-insertitem.md) Il messaggio include una [**struttura TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) che specifica l'handle per l'elemento padre e l'handle per l'elemento dopo il quale deve essere inserito il nuovo elemento. Il secondo handle deve identificare un elemento figlio dell'elemento padre specificato o uno di questi valori: TVI \_ FIRST, TVI \_ LAST o TVI \_ SORT.

Quando si imposta TVI FIRST o TVI LAST, il controllo visualizzazione albero inserisce il nuovo elemento all'inizio o alla fine dell'elenco di elementi \_ \_ figlio dell'elemento padre specificato. Quando si specifica TVI SORT, il controllo visualizzazione albero inserisce il nuovo elemento nell'elenco di elementi figlio in ordine alfabetico in base al testo delle \_ etichette degli elementi.

È possibile inserire l'elenco di elementi figlio di un elemento padre in ordine alfabetico usando il [**messaggio TVM \_ SORTCHILDREN.**](tvm-sortchildren.md) Il messaggio include un parametro che specifica se anche tutti i livelli di elementi figlio in ordine decrescente rispetto all'elemento padre specificato vengono ordinati in ordine alfabetico.

Il [**messaggio TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) consente di ordinare gli elementi figlio in base ai criteri definiti. Quando si usa questo messaggio, si specifica una funzione di callback definita dall'applicazione che il controllo visualizzazione albero può chiamare ogni volta che è necessario decidere l'ordine relativo di due elementi figlio. La funzione di callback riceve due valori definiti dall'applicazione a 32 bit per gli elementi confrontati e un terzo valore a 32 bit specificato durante l'invio di **TVM \_ SORTCHILDRENCB.**

## <a name="tree-view-item-states-overview"></a>panoramica Tree-View stati degli elementi

Ogni elemento in un controllo di visualizzazione albero ha uno stato corrente. Le informazioni sullo stato per ogni elemento includono un set di flag di bit e indici dell'elenco immagini che indicano l'immagine di stato dell'elemento e l'immagine di sovrapposizione. I flag di bit indicano se l'elemento è selezionato, disabilitato, espanso e così via. Nella maggior parte dei casi, un controllo di visualizzazione albero imposta automaticamente lo stato di un elemento in modo da riflettere le azioni dell'utente, ad esempio la selezione di un elemento. Tuttavia, è anche possibile impostare lo stato di un elemento usando il messaggio [**\_ TVM SETITEM**](tvm-setitem.md) ed è possibile recuperare lo stato corrente di un elemento usando il [**messaggio TVM \_ GETITEM.**](tvm-getitem.md) Per un elenco completo degli stati degli elementi, vedere [Stati degli elementi del controllo TreeView](tree-view-control-item-states.md).

Lo stato corrente di un elemento viene specificato dal membro **dello** stato della [**struttura TVITEM.**](/windows/win32/api/commctrl/ns-commctrl-tvitema) Un controllo visualizzazione albero potrebbe modificare lo stato di un elemento in modo da riflettere un'azione dell'utente, ad esempio la selezione dell'elemento o l'impostazione dello stato attivo sull'elemento. Inoltre, un'applicazione può modificare lo stato di un elemento per disabilitare o nascondere l'elemento o per specificare un'immagine sovrapposta o un'immagine di stato.

Quando si specifica o si modifica lo stato di un elemento, il membro **statemask** di  [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) specifica i bit di stato da impostare e il membro dello stato contiene i nuovi valori per tali bit.

Per impostare l'immagine di sovrimpressione di un elemento, **statemask** deve includere il valore [**TVIS \_ OVERLAYMASK**](tree-view-control-item-states.md) e **lo** stato deve includere l'indice in base uno dell'immagine sovrapposta spostata a sinistra di 8 bit usando la macro [**INDEXTOOVERLAYMASK.**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) L'indice può essere zero per non specificare alcuna immagine di sovrapposizione.

Accanto all'icona di un elemento viene visualizzata un'immagine di stato per indicare uno stato definito dall'applicazione. Le immagini di stato sono contenute in un *elenco* di immagini di stato specificato inviando un [**messaggio \_ TVM SETIMAGELIST.**](tvm-setimagelist.md) Per impostare l'immagine di stato di un elemento, includere il valore [**TVIS \_ STATEIMAGEMASK**](tree-view-control-item-states.md) nel membro **statemask** della [**struttura TVITEM.**](/windows/win32/api/commctrl/ns-commctrl-tvitema) I bit da 12 a 15 del membro dello stato della struttura specificano l'indice nell'elenco di immagini di stato dell'immagine da disegnare. 

Per impostare l'indice dell'immagine di stato, [**usare INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask). Questa macro accetta un indice e imposta i bit da 12 a 15 in modo appropriato. Per indicare che l'elemento non ha un'immagine di stato, impostare l'indice su zero. Questa convenzione indica che l'immagine zero nell'elenco delle immagini di stato non può essere usata come immagine di stato. Per isolare i bit da 12 a 15 del membro **dello** stato, usare la maschera [**TVIS \_ STATEIMAGEMASK.**](tree-view-control-item-states.md) Per altre informazioni sulle immagini di sovrapposizione e stato, vedere [Elenchi di immagini visualizzazione albero](#tree-view-image-lists).

## <a name="item-selection"></a>Selezione dell'elemento

Un controllo di visualizzazione albero invia una notifica alla finestra padre quando la selezione cambia da un elemento a un altro inviando i messaggi di notifica [ \_ TVN SELCHANGING](tvn-selchanging.md) e [TVN \_ SELCHANGED.](tvn-selchanged.md) Entrambe le notifiche includono un valore che specifica se la modifica è il risultato di un clic del mouse o di una sequenza di tasti. Le notifiche includono anche informazioni sull'elemento che sta guadagnando la selezione e sull'elemento che perde la selezione. È possibile usare queste informazioni per impostare gli attributi dell'elemento che dipendono dallo stato di selezione dell'elemento. La restituzione **di TRUE** in risposta a TVN \_ SELCHANGING impedisce la modifica della selezione e la restituzione **di FALSE** consente la modifica.

Un'applicazione può modificare la selezione inviando il [**messaggio TVM \_ SELECTITEM.**](tvm-selectitem.md)

## <a name="item-information"></a>Informazioni sull'elemento

I controlli visualizzazione albero supportano una serie di messaggi che recuperano informazioni sugli elementi nel controllo .

Il [**messaggio TVM \_ GETITEM**](tvm-getitem.md) può recuperare l'handle e gli attributi di un elemento. Gli attributi di un elemento includono lo stato corrente, gli indici nell'elenco di immagini del controllo delle immagini bitmap selezionate e non selezionate dell'elemento, un flag che indica se l'elemento dispone di elementi figlio, l'indirizzo della stringa di etichetta dell'elemento e il valore a 32 bit definito dall'applicazione dell'elemento.

Il [**messaggio TVM \_ GETNEXTITEM**](tvm-getnextitem.md) recupera l'elemento della visualizzazione albero che contiene la relazione specificata con l'elemento corrente. Il messaggio può recuperare l'elemento padre di un elemento, l'elemento visibile successivo o precedente, il primo elemento figlio e così via.

Il [**messaggio TVM \_ GETITEMRECT**](tvm-getitemrect.md) recupera il rettangolo di delimitazione per un elemento della visualizzazione albero. I messaggi [**TVM \_ GETCOUNT**](tvm-getcount.md) e [**TVM \_ GETVISIBLECOUNT**](tvm-getvisiblecount.md) recuperano rispettivamente un conteggio degli elementi in un controllo visualizzazione albero e un conteggio degli elementi che possono essere completamente visibili nella finestra del controllo visualizzazione albero. È possibile assicurarsi che un particolare elemento sia visibile usando il [**messaggio TVM \_ ENSUREVISIBLE.**](tvm-ensurevisible.md)

## <a name="tree-view-image-lists"></a>Tree-View di immagini

A ogni elemento di un controllo di visualizzazione albero possono essere associate quattro immagini bitmap.

-   Immagine, ad esempio una cartella aperta, visualizzata quando l'elemento viene selezionato.
-   Immagine, ad esempio una cartella chiusa, visualizzata quando l'elemento non è selezionato.
-   Immagine sovrapposta disegnata in modo trasparente sull'immagine selezionata o non selezionata.
-   Immagine di stato, ovvero un'immagine aggiuntiva visualizzata a sinistra dell'immagine selezionata o non selezionata. È possibile usare immagini di stato, ad esempio caselle di controllo selezionate e deselezionate, per indicare gli stati degli elementi definiti dall'applicazione.

Per impostazione predefinita, un controllo visualizzazione albero non visualizza le immagini degli elementi. Per visualizzare le immagini degli elementi, è necessario creare elenchi di immagini e associarli al controllo . Per altre informazioni sugli elenchi di immagini, vedere [Elenchi di immagini](image-lists.md).

Un controllo visualizzazione albero può avere due elenchi di immagini: un elenco di immagini normale e un elenco di immagini di stato. Un normale elenco di immagini archivia le immagini selezionate, non selezionate e sovrapposte. Un elenco di immagini di stato archivia le immagini di stato. Usare la [**funzione ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) per creare un elenco di immagini e usare altre funzioni dell'elenco immagini per aggiungere bitmap all'elenco immagini. Quindi, per associare l'elenco di immagini al controllo visualizzazione albero, usare il [**messaggio TVM \_ SETIMAGELIST.**](tvm-setimagelist.md) Il [**messaggio TVM \_ GETIMAGELIST**](tvm-getimagelist.md) recupera un handle per uno degli elenchi di immagini di un controllo visualizzazione albero. Questo messaggio è utile se è necessario aggiungere altre immagini all'elenco.

Oltre alle immagini selezionate e non selezionate, l'elenco immagini normale di un controllo visualizzazione albero può contenere fino a quattro immagini sovrapposte. Le immagini sovrapposte sono identificate da un indice in base uno e sono progettate per essere disegnate in modo trasparente sulle immagini selezionate e non selezionate. Per assegnare un indice di maschera di sovrapposizione a un'immagine nell'elenco immagini normale, chiamare la [**funzione ImageList \_ SetOverlayImage.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage)

Per impostazione predefinita, tutti gli elementi visualizzano la prima immagine nell'elenco immagini normale per gli stati selezionato e non selezionato. Inoltre, per impostazione predefinita, gli elementi non visualizzano immagini sovrapposte o immagini di stato. È possibile modificare questi comportamenti predefiniti per un elemento inviando il messaggio [**\_ TVM INSERTITEM**](tvm-insertitem.md) o [**TVM \_ SETITEM.**](tvm-setitem.md) Questi messaggi usano la [**struttura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) per specificare gli indici dell'elenco immagini per un elemento.

Per specificare le immagini selezionate e non selezionate di un elemento, impostare i bit TVIF SELECTEDIMAGE e TVIF IMAGE nel membro mask della struttura TVITEM e specificare gli indici dal normale elenco di immagini del controllo nei membri \_ \_ **iSelectImage** **e iImage.**  [](/windows/win32/api/commctrl/ns-commctrl-tvitema) In alternativa, è possibile specificare il valore I \_ IMAGECALLBACK in **iSelectImage** e **iImage** anziché specificare gli indici. In questo modo il controllo esegue una query sulla finestra padre per trovare un indice dell'elenco immagini ogni volta che l'elemento sta per essere ridisegnato. Il controllo invia il [messaggio di notifica \_ TVN GETDISPINFO](tvn-getdispinfo.md) per recuperare l'indice.

Per associare un'immagine di sovrimpressione a un elemento, usare  la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) per specificare un indice di maschera di sovrimpressione nel membro di stato della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dell'elemento. È anche necessario impostare i bit [**TVIS \_ OVERLAYMASK**](tree-view-control-item-states.md) nel **membro stateMask.** Gli indici delle maschere sovrapposte sono basati su uno; Un indice pari a zero indica che non è stata specificata alcuna immagine di sovrapposizione.

Le immagini di stato vengono archiviate in un elenco di immagini di stato separato e identificate dal relativo indice. Per specificare l'elenco di immagini di stato, inviare un [**messaggio \_ TVM SETIMAGELIST.**](tvm-setimagelist.md) A differenza del controllo visualizzazione elenco, che usa un indice in base uno per identificare le immagini di stato, le immagini dello stato del controllo visualizzazione albero sono identificate da un indice in base zero. Tuttavia, un indice pari a zero indica che l'elemento non dispone di un'immagine di stato. Di conseguenza, l'immagine zero non può essere usata come immagine di stato. Per altre informazioni sullo stato degli elementi e sulle immagini di stato, vedere Panoramica degli [stati degli elementi della visualizzazione albero](#tree-view-item-states-overview).

## <a name="drag-and-drop-operations"></a>Operazioni di trascinamento della selezione

Un controllo di visualizzazione albero notifica alla finestra padre quando l'utente inizia a trascinare un elemento. La finestra padre riceve un messaggio di notifica [TVN \_ BEGINDRAG](tvn-begindrag.md) quando l'utente inizia a trascinare un elemento con il pulsante sinistro del mouse e un messaggio di notifica [TVN \_ BEGINRDRAG](tvn-beginrdrag.md) quando l'utente inizia a trascinare con il pulsante destro del mouse. È possibile impedire a un controllo visualizzazione albero di inviare queste notifiche fornendo al controllo visualizzazione albero lo stile [**\_ TVS DISABLEDRAGDROP.**](tree-view-control-window-styles.md)

Si ottiene un'immagine da visualizzare durante un'operazione di trascinamento usando il [**messaggio TVM \_ CREATEDRAGIMAGE.**](tvm-createdragimage.md) Il controllo visualizzazione albero crea una bitmap di trascinamento in base all'etichetta dell'elemento trascinato. Il controllo visualizzazione albero crea quindi un elenco di immagini, aggiunge la bitmap e restituisce l'handle all'elenco di immagini.

È necessario fornire il codice che effettivamente trascina l'elemento. Ciò comporta in genere l'uso delle funzionalità di trascinamento delle funzioni dell'elenco di immagini e l'elaborazione dei messaggi [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) e [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (o [**WM \_ RBUTTONUP)**](/windows/desktop/inputdev/wm-rbuttonup)inviati alla finestra padre dopo l'inizio dell'operazione di trascinamento.

Se gli elementi in un controllo di visualizzazione albero devono essere le destinazioni delle operazioni di trascinamento della selezione, è necessario sapere quando il puntatore del mouse si trova su un elemento di destinazione. È possibile scoprirlo usando il [**messaggio TVM \_ HITTEST.**](tvm-hittest.md) Specificare l'indirizzo di una [**struttura TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) che contiene le coordinate correnti del puntatore del mouse. Quando la [**funzione SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) viene restituita, la struttura contiene un flag che indica la posizione del puntatore del mouse rispetto al controllo di visualizzazione albero. Se il puntatore si trova su un elemento nel controllo di visualizzazione albero, la struttura contiene anche l'handle per l'elemento.

È possibile indicare che un elemento è la destinazione di un'operazione di trascinamento della selezione usando il messaggio [**\_ TVM SETITEM**](tvm-setitem.md) per impostare lo stato sul valore [**\_ TVIS DROPTED.**](tree-view-control-item-states.md) Un elemento con questo stato viene disegnato nello stile utilizzato per indicare una destinazione di trascinamento della selezione.

## <a name="tree-view-control-notification-messages"></a>Tree-View di notifica di controllo

Un controllo di visualizzazione albero invia i messaggi di notifica seguenti alla relativa finestra padre sotto forma di [**messaggi WM \_ NOTIFY.**](wm-notify.md)



| Notifica                                    | Descrizione                                                                            |
|-------------------------------------------------|----------------------------------------------------------------------------------------|
| [TVN \_ BEGINDRAG](tvn-begindrag.md)             | Segnala l'inizio di un'operazione di trascinamento della selezione.                                        |
| [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md)   | Segnala l'inizio della modifica delle etichette sul posto.                                           |
| [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)           | Segnala che il pulsante destro del mouse ha avviato un'operazione di trascinamento della selezione.             |
| [TVN \_ DELETEITEM](tvn-deleteitem.md)           | Segnala l'eliminazione di un elemento specifico.                                               |
| [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md)       | Segnala la fine della modifica delle etichette.                                                      |
| [TVN \_ GETDISPINFO](tvn-getdispinfo.md)         | Richiede le informazioni necessarie al controllo di visualizzazione albero per visualizzare un elemento.           |
| [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md)       | Segnala che l'elenco di elementi figlio di un elemento padre è stato espanso o compresso.            |
| [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md)     | Segnala che l'elenco di elementi figlio di un elemento padre sta per essere espanso o compresso. |
| [TVN \_ KEYDOWN](tvn-keydown.md)                 | Segnala un evento della tastiera.                                                              |
| [TVN \_ SELCHANGED](tvn-selchanged.md)           | Segnala che la selezione è cambiata da un elemento a un altro.                       |
| [TVN \_ SELCHANGING](tvn-selchanging.md)         | Segnala che la selezione sta per essere modificata da un elemento a un altro.            |
| [TVN \_ SETDISPINFO](tvn-setdispinfo.md)         | Notifica a una finestra padre che deve aggiornare le informazioni che gestisce per un elemento. |



 

## <a name="default-tree-view-control-message-processing"></a>Elaborazione predefinita Tree-View dei messaggi di controllo

In questa sezione viene descritta l'elaborazione dei messaggi della finestra eseguita da un controllo di visualizzazione albero. I messaggi specifici dei controlli visualizzazione albero vengono illustrati in altre sezioni di questo documento, quindi non sono inclusi qui.



| Message                                            | Elaborazione eseguita                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)               | Elabora i messaggi [di \_ notifica del](en-update.md) controllo di modifica EN UPDATE e [EN \_ KILLFOCUS](en-killfocus.md) e inoltra tutte le altre notifiche del controllo di modifica alla finestra padre. Nessun valore restituito.                                                                                                                                                                                                                                                                                                |
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                 | Alloca memoria e inizializza strutture di dati interne. In caso di esito positivo, restituisce zero oppure -1 in caso contrario.                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)               | Libera tutte le risorse di sistema associate al controllo. Restituisce zero.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**WM \_ ENABLE**](/windows/desktop/winmsg/wm-enable)                 | Abilita o disabilita il controllo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)         | Cancella lo sfondo della finestra usando il colore di sfondo corrente per il controllo visualizzazione albero. Restituisce **TRUE.**                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | Restituisce una combinazione dei valori \_ DLGC WANTARROWS e DLGC \_ WANTCHARS.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Restituisce l'handle per il tipo di carattere dell'etichetta corrente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**WM \_ HSCROLL**](wm-hscroll.md)                  | Scorre il controllo di visualizzazione albero. Restituisce **TRUE se** si verifica lo scorrimento oppure **FALSE in caso** contrario.                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)             | Invia il [messaggio di notifica \_ TVN KEYDOWN](tvn-keydown.md) alla finestra padre per tutte le chiavi. Invia il [messaggio di notifica NM RETURN \_ (visualizzazione albero)](nm-return-tree-view-.md) quando l'utente preme INVIO. Sposta il cursore quando l'utente preme i tasti di direzione o pggi su, PGGI GIÙ, HOME, FINE o BACKSPACE. Scorre il controllo di visualizzazione albero quando l'utente preme CTRL in combinazione con questi tasti. Restituisce **TRUE se** viene elaborata una chiave oppure **FALSE in caso** contrario. |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)         | Ridisegna l'elemento con lo stato attivo, se presente, e invia un messaggio di notifica [NM \_ KILLFOCUS (visualizzazione albero)](nm-killfocus-tree-view.md) alla finestra padre.                                                                                                                                                                                                                                                                                                                                                                  |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) | Annulla la modifica delle etichette e, se è stato fatto doppio clic su un elemento, invia il messaggio di notifica [NM \_ DBLCLK (visualizzazione albero)](nm-dblclk-tree-view.md) alla finestra padre. Se la finestra padre restituisce 0, il controllo di visualizzazione albero attiva o disattiva lo stato espanso dell'elemento, inviando alla finestra padre i messaggi di notifica [ \_ TVN ITEMEXPANDING](tvn-itemexpanding.md) e [ \_ TVN ITEMEXPANDED.](tvn-itemexpanded.md) Nessun valore restituito.                                                                             |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | Attiva o disattiva lo stato espanso se l'utente ha fatto clic sul pulsante associato a un elemento padre. Se l'utente ha fatto clic su un'etichetta di elemento, il controllo di visualizzazione albero seleziona e imposta lo stato attivo sull'elemento. Se l'utente sposta il mouse prima di rilasciare il pulsante del mouse, il controllo di visualizzazione albero avvia un'operazione di trascinamento della selezione. Nessun valore restituito.                                                                                                                                                                          |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                      | Disegna l'area non valida del controllo di visualizzazione albero. Restituisce zero. Se il *parametro wParam* è diverso da **NULL,** il controllo presuppone che il valore sia un handle per un contesto di dispositivo (HDC) e disegna usando tale contesto di dispositivo.                                                                                                                                                                                                                                                                                      |
| [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)     | Verifica se è stato fatto clic su un elemento ed è stata avviata un'operazione di trascinamento. Se l'operazione è iniziata, invia un messaggio di notifica [ \_ TVN BEGINRDRAG](tvn-beginrdrag.md) alla finestra padre ed evidenzia l'obiettivo di rilascio. In caso contrario, invia un [messaggio di notifica nm \_ RCLICK (visualizzazione albero)](nm-rclick-tree-view.md) alla finestra padre. Nessun valore restituito.                                                                                                                                           |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)           | Ridisegna l'elemento con lo stato attivo, se presente, e invia un messaggio di notifica [NM \_ SETFOCUS](nm-setfocus.md) alla finestra padre.                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | Salva l'handle del tipo di carattere specificato e ridisegna il controllo di visualizzazione albero usando il nuovo tipo di carattere.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw)              | Imposta o cancella il flag di ridisegno. Il controllo visualizzazione albero viene ridisegnato dopo l'impostazione del flag di ridisegno. Restituisce zero.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**DIMENSIONI \_ WM**](/windows/desktop/winmsg/wm-size)                     | Ricalcola le variabili interne che dipendono dalle dimensioni dell'area client del controllo visualizzazione albero. Restituisce **TRUE.**                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**WM \_ STYLECHANGED**](/windows/desktop/winmsg/wm-stylechanged)     | Annulla la modifica delle etichette e ridisegna il controllo di visualizzazione albero usando i nuovi stili. Restituisce zero.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange)    | Ridisegna il controllo di visualizzazione albero utilizzando il nuovo colore se è impostato il flag di ridisegno. Nessun valore restituito.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**WM \_ TIMER**](/windows/desktop/winmsg/wm-timer)                   | Inizia a modificare un'etichetta di elemento. Se l'utente fa clic sull'etichetta dell'elemento con lo stato attivo, il controllo di visualizzazione albero imposta un timer anziché entrare immediatamente in modalità di modifica. Il timer consente alla visualizzazione albero di evitare di entrare in modalità di modifica se l'utente fa doppio clic sull'etichetta. Restituisce zero.                                                                                                                                                                                                                       |
| [**WM \_ VSCROLL**](wm-vscroll.md)                  | Scorre il controllo di visualizzazione albero. Restituisce **TRUE se** si verifica lo scorrimento oppure **FALSE in caso** contrario.                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ESEMPIO: CustDTv illustra il disegno personalizzato in un controllo TreeView (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 