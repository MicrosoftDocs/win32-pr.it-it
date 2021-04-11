---
title: Casella di riepilogo
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con le caselle di riepilogo. Una casella di riepilogo è una finestra di controllo che contiene un semplice elenco di elementi da cui l'utente può scegliere.
ms.assetid: vs|controls|~\controls\listboxes\listboxes.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fda5e6bb2d1d4c3c4f23e506900257c1b2ce64b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118503"
---
# <a name="list-box"></a>Casella di riepilogo

Questa sezione contiene informazioni sugli elementi di programmazione usati con le caselle di riepilogo. Una casella di riepilogo è una finestra di controllo che contiene un semplice elenco di elementi da cui l'utente può scegliere. Per gli elenchi più complessi, usare invece la [visualizzazione elenco](list-view-control-reference.md) .

### <a name="overviews"></a>Cenni preliminari



| Argomento                                    | Contenuto                                                              |
|------------------------------------------|-----------------------------------------------------------------------|
| [Informazioni sulle caselle di riepilogo](about-list-boxes.md) | Descrive le funzionalità della casella di riepilogo.<br/>                               |
| [Uso di caselle di riepilogo](using-list-boxes.md) | Viene illustrato come eseguire le attività associate alle caselle di riepilogo. <br/> |



 

### <a name="functions"></a>Funzioni



| Argomento                                    | Contenuto                                                                                                                |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)         | Sostituisce il contenuto di una casella di riepilogo con i nomi delle sottodirectory e i file in una directory specificata.<br/> |
| [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) | Recupera la selezione corrente da una casella di riepilogo a selezione singola.<br/>                                            |
| [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert)         | Disegna l'icona Inserisci nella finestra padre della casella di riepilogo di trascinamento specificata. <br/>                                  |
| [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) | Recupera le informazioni relative alla casella di riepilogo specificata.<br/>                                                          |
| [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt)     | Recupera l'indice dell'elemento in corrispondenza del punto specificato in una casella di riepilogo. <br/>                                       |
| [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist)     | Consente di modificare la casella di riepilogo a selezione singola specificata in una casella di riepilogo di trascinamento. <br/>                                         |



 

### <a name="messages"></a>Messaggi



| Argomento                                                     | Contenuto                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AddFile lb**](lb-addfile.md)                         | Aggiunge il nome file specificato a una casella di riepilogo contenente un elenco di directory. <br/>                                                                                                                                                                                     |
| [**\_ADDSTRING lb**](lb-addstring.md)                     | Aggiunge una stringa a una casella di riepilogo. <br/>                                                                                                                                                                                                                                      |
| [**\_DELETESTRING lb**](lb-deletestring.md)               | Elimina una stringa in una casella di riepilogo. <br/>                                                                                                                                                                                                                                   |
| [**\_dir lb**](lb-dir.md)                                 | Aggiunge nomi all'elenco visualizzato da una casella di riepilogo. <br/>                                                                                                                                                                                                                   |
| [**\_FindString lb**](lb-findstring.md)                   | Trova la prima stringa in una casella di riepilogo che inizia con la stringa specificata. <br/>                                                                                                                                                                                       |
| [**\_FINDEXACTSTRING lb**](lb-findstringexact.md)         | Trova la prima stringa della casella di riepilogo che corrisponde esattamente alla stringa specificata, ad eccezione del fatto che la ricerca non fa distinzione tra maiuscole e minuscole. <br/>                                                                                                                                          |
| [**\_GETANCHORINDEX lb**](lb-getanchorindex.md)           | Ottiene l'indice dell'elemento di ancoraggio, ovvero l'elemento da cui inizia una selezione multipla. <br/>                                                                                                                                                                       |
| [**\_GETCARETINDEX lb**](lb-getcaretindex.md)             | Recupera l'indice dell'elemento con il rettangolo di attivazione in una casella di riepilogo a selezione multipla. L'elemento può essere selezionato o meno. <br/>                                                                                                                               |
| [**CONTEGGIO di LB \_**](lb-getcount.md)                       | Ottiene il numero di elementi in una casella di riepilogo. <br/>                                                                                                                                                                                                                           |
| [**LB \_ GETcursel**](lb-getcursel.md)                     | Ottiene l'indice dell'elemento attualmente selezionato, se presente, in una casella di riepilogo a selezione singola. <br/>                                                                                                                                                                            |
| [**\_GETHORIZONTALEXTENT lb**](lb-gethorizontalextent.md) | Ottiene la larghezza, in pixel, in cui è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole) se nella casella di riepilogo è presente una barra di scorrimento orizzontale. <br/>                                                                                                                       |
| [**\_GETITEMDATA lb**](lb-getitemdata.md)                 | Ottiene il valore definito dall'applicazione associato all'elemento della casella di riepilogo specificato. <br/>                                                                                                                                                                                   |
| [**\_GETITEMHEIGHT lb**](lb-getitemheight.md)             | Ottiene l'altezza degli elementi in una casella di riepilogo. <br/>                                                                                                                                                                                                                           |
| [**\_GETITEMRECT lb**](lb-getitemrect.md)                 | Ottiene le dimensioni del rettangolo che delimita un elemento della casella di riepilogo come attualmente visualizzato nella casella di riepilogo. <br/>                                                                                                                                                    |
| [**\_GETLISTBOXINFO lb**](lb-getlistboxinfo.md)           | Ottiene il numero di elementi per colonna in una casella di riepilogo specificata. <br/>                                                                                                                                                                                                      |
| [**LB \_ GETlocale**](lb-getlocale.md)                     | Ottiene le impostazioni locali correnti della casella di riepilogo. <br/>                                                                                                                                                                                                                          |
| [**\_GETSEL lb**](lb-getsel.md)                           | Ottiene lo stato di selezione di un elemento. <br/>                                                                                                                                                                                                                              |
| [**\_GETSELCOUNT lb**](lb-getselcount.md)                 | Ottiene il numero totale di elementi selezionati in una casella di riepilogo a selezione multipla. <br/>                                                                                                                                                                                         |
| [**\_GETSELITEMS lb**](lb-getselitems.md)                 | Riempie un buffer con una matrice di Integer che specificano i numeri degli elementi selezionati in una casella di riepilogo a selezione multipla. <br/>                                                                                                                                        |
| [**GetText LB \_**](lb-gettext.md)                         | Ottiene una stringa da una casella di riepilogo. <br/>                                                                                                                                                                                                                                    |
| [**\_GETTEXTLEN lb**](lb-gettextlen.md)                   | Ottiene la lunghezza di una stringa in una casella di riepilogo. <br/>                                                                                                                                                                                                                        |
| [**\_GETTOPINDEX lb**](lb-gettopindex.md)                 | Ottiene l'indice del primo elemento visibile in una casella di riepilogo. <br/>                                                                                                                                                                                                           |
| [**\_INITSTORAGE lb**](lb-initstorage.md)                 | Alloca memoria per archiviare gli elementi della casella di riepilogo. Questo messaggio viene usato prima che un'applicazione aggiunga un numero elevato di elementi a una casella di riepilogo.<br/>                                                                                                                                |
| [**\_INSERTSTRING lb**](lb-insertstring.md)               | Inserisce i dati di una stringa o di un elemento in una casella di riepilogo. A differenza del messaggio [**lb \_ ADDSTRING**](lb-addstring.md) , il messaggio [**lb \_ INSERTSTRING**](lb-insertstring.md) non determina l'ordinamento di un elenco con lo stile di [**\_ ordinamento lbs**](list-box-styles.md) . <br/> |
| [**\_ITEMFROMPOINT lb**](lb-itemfrompoint.md)             | Ottiene l'indice in base zero dell'elemento più vicino al punto specificato in una casella di riepilogo.<br/>                                                                                                                                                                                   |
| [**\_ResetContent lb**](lb-resetcontent.md)               | Rimuove tutti gli elementi da una casella di riepilogo. <br/>                                                                                                                                                                                                                                |
| [**\_SELECTSTRING lb**](lb-selectstring.md)               | Cerca un elemento in una casella di riepilogo che inizia con i caratteri di una stringa specificata. <br/>                                                                                                                                                                            |
| [**\_SELITEMRANGE lb**](lb-selitemrange.md)               | Consente di selezionare o deselezionare uno o più elementi consecutivi in una casella di riepilogo a selezione multipla. <br/>                                                                                                                                                                              |
| [**\_SELITEMRANGEEX lb**](lb-selitemrangeex.md)           | Seleziona uno o più elementi consecutivi in una casella di riepilogo a selezione multipla. <br/>                                                                                                                                                                                           |
| [**\_SETANCHORINDEX lb**](lb-setanchorindex.md)           | Imposta l'elemento di ancoraggio, ovvero l'elemento da cui inizia una selezione multipla. Una selezione multipla si estende a tutti gli elementi dall'elemento di ancoraggio all'elemento del punto di inserimento.<br/>                                                                                                        |
| [**\_SETCARETINDEX lb**](lb-setcaretindex.md)             | Imposta il rettangolo di attivazione sull'elemento in corrispondenza dell'indice specificato in una casella di riepilogo a selezione multipla. Se l'elemento non è visibile, viene spostato nella visualizzazione. <br/>                                                                                                               |
| [**\_SETCOLUMNWIDTH lb**](lb-setcolumnwidth.md)           | Imposta la larghezza, in pixel, di tutte le colonne in una casella di riepilogo a più colonne. <br/>                                                                                                                                                                                          |
| [**\_conteggio lb**](lb-setcount.md)                       | Imposta il numero di elementi in una casella di riepilogo creata con lo stile [**\_ NoData lbs**](list-box-styles.md) e non viene creato con lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) . <br/>                                                          |
| [**di \_ lb**](lb-setcursel.md)                     | Seleziona una stringa e la scorre nella visualizzazione, se necessario. <br/>                                                                                                                                                                                                          |
| [**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md) | Imposta la larghezza, in pixel, in base alla quale è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole). <br/>                                                                                                                                                               |
| [**\_SETITEMDATA lb**](lb-setitemdata.md)                 | Imposta un valore associato all'elemento specificato in una casella di riepilogo. <br/>                                                                                                                                                                                            |
| [**\_SETITEMHEIGHT lb**](lb-setitemheight.md)             | Imposta l'altezza, in pixel, degli elementi in una casella di riepilogo. <br/>                                                                                                                                                                                                               |
| [**\_impostazioni locali lb**](lb-setlocale.md)                     | Imposta le impostazioni locali correnti della casella di riepilogo. <br/>                                                                                                                                                                                                                          |
| [**\_SETSEL lb**](lb-setsel.md)                           | Seleziona una stringa in una casella di riepilogo a selezione multipla. <br/>                                                                                                                                                                                                                |
| [**\_SETTABSTOPS lb**](lb-settabstops.md)                 | Imposta le posizioni di interruzione di tabulazione in una casella di riepilogo. <br/>                                                                                                                                                                                                                        |
| [**\_SETTOPINDEX lb**](lb-settopindex.md)                 | Assicura che l'elemento specificato in una casella di riepilogo sia visibile. <br/>                                                                                                                                                                                                         |



 

### <a name="notifications"></a>Notifiche



| Argomento                                             | Contenuto                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_DBLCLK LBN](lbn-dblclk.md)                     | Notifica all'applicazione che l'utente ha fatto doppio clic su un elemento in una casella di riepilogo. <br/>                                                                                                                                                                                                                                         |
| [\_ERRSPACE LBN](lbn-errspace.md)                 | Notifica all'applicazione che la casella di riepilogo non può allocare memoria sufficiente per soddisfare una richiesta specifica. <br/>                                                                                                                                                                                                                     |
| [\_KILLFOCUS LBN](lbn-killfocus.md)               | Notifica all'applicazione che la casella di riepilogo ha perso lo stato attivo della tastiera. <br/>                                                                                                                                                                                                                                                  |
| [\_SELCANCEL LBN](lbn-selcancel.md)               | Notifica all'applicazione che l'utente ha annullato la selezione in una casella di riepilogo. <br/>                                                                                                                                                                                                                                         |
| [\_selChange LBN](lbn-selchange.md)               | Notifica all'applicazione che la selezione in una casella di riepilogo è stata modificata. <br/>                                                                                                                                                                                                                                                   |
| [LBN \_ SetFocus](lbn-setfocus.md)                 | Notifica all'applicazione che la casella di riepilogo ha ricevuto lo stato attivo. <br/>                                                                                                                                                                                                                                              |
| [**\_CHARTOITEM WM**](wm-chartoitem.md)           | Inviato da una casella di riepilogo con lo stile [**\_ WANTKEYBOARDINPUT lbs**](list-box-styles.md) al relativo proprietario in risposta a un messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) . <br/>                                                                                                                                        |
| [**\_CTLCOLORLISTBOX WM**](wm-ctlcolorlistbox.md) | Inviato alla finestra padre di una casella di riepilogo prima che il sistema disegni la casella di riepilogo. Rispondendo a questo messaggio, la finestra padre può impostare il testo e i colori di sfondo della casella di riepilogo usando l'handle del contesto del dispositivo di visualizzazione specificato. <br/>                                                                              |
| [**\_DeleteItem WM**](wm-deleteitem.md)           | Inviato al proprietario di una casella di riepilogo o di una casella combinata quando la casella di riepilogo o la casella combinata viene distrutta o quando gli elementi vengono rimossi dal messaggio [**lb \_ DELETESTRING**](lb-deletestring.md), [**lb \_ ResetContent**](lb-resetcontent.md), [**CB \_ DELETESTRING**](cb-deletestring.md)o [**CB \_ ResetContent**](cb-resetcontent.md) . <br/> |
| [**\_VKEYTOITEM WM**](wm-vkeytoitem.md)           | Inviato da una casella di riepilogo con lo stile [**\_ WANTKEYBOARDINPUT di lbs**](list-box-styles.md) al suo proprietario in risposta a un messaggio del [**\_ KeyDown di WM**](/windows/desktop/inputdev/wm-keydown) . <br/>                                                                                                                                  |
| [\_BEGINDRAG DL](dl-begindrag.md)                 | Notifica alla finestra padre della casella di riepilogo di trascinamento che l'utente ha fatto clic con il pulsante sinistro del mouse su un elemento. <br/>                                                                                                                                                                                                                   |
| [\_CANCELDRAG DL](dl-canceldrag.md)               | Segnala che l'utente ha annullato un'operazione di trascinamento facendo clic con il pulsante destro del mouse o premendo il tasto ESC. <br/>                                                                                                                                                                                                          |
| [\_trascinamento DL](dl-dragging.md)                   | Segnala che l'utente ha spostato il mouse durante il trascinamento di un elemento. <br/>                                                                                                                                                                                                                                                        |
| [DL \_ eliminato](dl-dropped.md)                     | Segnala che l'utente ha completato un'operazione di trascinamento rilasciando il pulsante sinistro del mouse. <br/>                                                                                                                                                                                                                                 |



 

### <a name="structures"></a>Strutture



| Argomento                                        | Contenuto                                                                                                                                                               |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) | Contiene informazioni su una casella di riepilogo o un elemento casella combinata eliminata.<br/>                                                                                            |
| [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)         | Contiene informazioni su un evento di trascinamento. Il puntatore a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) viene passato come parametro *lParam* del messaggio dell'elenco di trascinamento. <br/> |



 

### <a name="constants"></a>Costanti



| Argomento                                  | Contenuto                                                                |
|----------------------------------------|-------------------------------------------------------------------------|
| [Stili casella di riepilogo](list-box-styles.md) | Vengono descritti gli stili della finestra che definiscono un controllo casella di riepilogo. <br/> |



 

 

