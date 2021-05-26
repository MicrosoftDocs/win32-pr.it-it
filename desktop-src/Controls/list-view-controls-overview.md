---
title: Informazioni List-View seguenti
description: Un controllo visualizzazione elenco è una finestra che visualizza una raccolta di elementi.
ms.assetid: 163f7778-690c-4166-b0c5-c7be1a03ae98
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 592684378b4264319d790b1e2e05eb9e0ae37f28
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424331"
---
# <a name="about-list-view-controls"></a>Informazioni List-View seguenti

Vedere [l'esempio di controllo ListView virtuale](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw).

Un controllo visualizzazione elenco è una finestra che visualizza una raccolta di elementi. I controlli visualizzazione elenco offrono diversi modi per disporre e visualizzare gli elementi e sono molto più flessibili rispetto alle semplici [caselle di riepilogo.](list-boxes.md) Ad esempio, è possibile visualizzare informazioni aggiuntive su ogni elemento nelle colonne a destra dell'icona e dell'etichetta.

-   [Stili e visualizzazioni di visualizzazione elenco](#list-view-styles-and-views)
    -   [Stili List-View estesi](#extended-list-view-styles)
-   [Stile List-View virtuale](#virtual-list-view-style)
    -   [Creazione di un controllo List-View virtuale](#creating-a-virtual-list-view-control)
    -   [Problemi di compatibilità](#compatibility-issues)
    -   [Gestione dei codici di notifica di List-View virtuali](#handling-virtual-list-view-control-notification-codes)
    -   [Gestione cache](#cache-management)
-   [Aree di lavoro visualizzazione elenco](#list-view-working-areas)
-   [Elenchi di immagini visualizzazione elenco](#list-view-image-lists)
-   [Elementi ed elementi secondari della visualizzazione elenco](#list-view-items-and-subitems)
    -   [Stati degli elementi di visualizzazione elenco](#list-view-item-states)
    -   [Elementi di callback e maschera di callback](#callback-items-and-the-callback-mask)
    -   [Posizione elemento visualizzazione elenco](#list-view-item-position)
    -   [Disposizione, ordinamento e ricerca di elementi](#arranging-sorting-and-finding-items)
-   [Colonne della visualizzazione elenco](#list-view-columns)
-   [Posizione di scorrimento della visualizzazione elenco](#list-view-scroll-position)
-   [Modifica delle etichette di visualizzazione elenco](#list-view-label-editing)
-   [Colori visualizzazione elenco](#list-view-colors)
-   [Disposizione degli elementi dell'elenco per gruppo](#arranging-list-items-by-group)
-   [Segni di inserimento](#insertion-marks)

## <a name="list-view-styles-and-views"></a>List-View stili e visualizzazioni

I controlli visualizzazione elenco possono visualizzare gli elementi in cinque visualizzazioni diverse. Lo stile della finestra del controllo specifica la visualizzazione predefinita. Gli stili di finestra aggiuntivi specificano l'allineamento degli elementi e delle funzionalità specifiche del controllo. Nella tabella seguente vengono descritte le viste.



| Nome della visualizzazione             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Visualizzazione icona             | Specificato dallo stile [**della finestra LVS \_ ICON**](list-view-window-styles.md) o passando **LV VIEW \_ \_ ICON** con il [**messaggio \_ LVM SETVIEW.**](lvm-setview.md) Ogni elemento viene visualizzato come icona a dimensione intera con un'etichetta sotto di essa. L'utente può trascinare gli elementi in qualsiasi posizione nella finestra di visualizzazione elenco.                                                                                                                                                                                                                                         |
| Visualizzazione icona piccola       | Specificato dallo stile [**della finestra LVS \_ SMALLICON**](list-view-window-styles.md) o passando **LV VIEW \_ \_ SMALLICON** con [**LVM \_ SETVIEW.**](lvm-setview.md) Ogni elemento viene visualizzato come una piccola icona con l'etichetta a destra. L'utente può trascinare gli elementi in qualsiasi posizione.                                                                                                                                                                                                                                                       |
| Visualizzazione elenco             | Specificato dallo stile [**della finestra LVS \_ LIST**](list-view-window-styles.md) o passando **LV VIEW \_ \_ LIST** con [**LVM \_ SETVIEW.**](lvm-setview.md) Ogni elemento viene visualizzato come una piccola icona con un'etichetta a destra. Gli elementi sono disposti in colonne e l'utente non può trascinarli in una posizione arbitraria.                                                                                                                                                                                                                               |
| Visualizzazione report (dettagli) | Specificato dallo stile [**della finestra LVS \_ REPORT**](list-view-window-styles.md) o passando **LV VIEW \_ \_ DETAILS** con [**LVM \_ SETVIEW**](lvm-setview.md). Ogni elemento viene visualizzato sulla propria riga, con le informazioni disposte in colonne. La colonna più a sinistra è sempre giustificata a sinistra e contiene l'icona e l'etichetta piccole. Le colonne successive contengono elementi secondari come specificato dall'applicazione. Ogni colonna ha un'intestazione, a meno che non si specifica anche lo stile della finestra [**\_ LVS NOCOLUMNHEADER.**](list-view-window-styles.md) |
| Visualizzazione affiancata             | **Versione 6 e successive.** Specificato passando **LV \_ VIEW \_ TILE** con [**LVM \_ SETVIEW**](lvm-setview.md). Ogni elemento viene visualizzato come icona di dimensioni complete con un'etichetta di una o più righe accanto.                                                                                                                                                                                                                                                                                                                                                        |



 

Le schermate seguenti usano le visualizzazioni per visualizzare quantità diverse di informazioni su ognuno dei sette animali domestici. Le visualizzazioni illustrano come possono essere visualizzate le informazioni in Windows Vista. Gli stili di visualizzazione per il controllo sono stati impostati sul tema "Explorer" usando [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).

La schermata seguente mostra la visualizzazione dei dettagli.

![Screenshot che mostra le informazioni in cinque colonne e sette righe](images/lv-detailsview.png)

Lo screenshot seguente mostra la visualizzazione icona.

![Screenshot che mostra solo il nome di ogni animale domestico e un'icona che indica la specie](images/lv-iconview.png)

La schermata seguente mostra la visualizzazione elenco.

![Screenshot che mostra, per ogni animale domestico, un'icona di grandi dimensioni accanto al testo del nome, della razza e del prezzo dell'animale](images/lv-listview.png)

Lo screenshot seguente mostra la visualizzazione affiancata.

![visualizzazione affiancata.](images/lv-tileview.png)

È possibile modificare il tipo di visualizzazione dopo aver creato un controllo visualizzazione elenco. Per recuperare e modificare lo stile della finestra, usare [**le funzioni GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) [**e SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) Per determinare gli stili della finestra della visualizzazione corrente, usare il [**valore \_ LVS TYPEMASK.**](list-view-window-styles.md)

È possibile controllare il modo in cui gli elementi vengono disposti nella visualizzazione icona o icona piccola specificando lo stile della finestra [**LVS \_ ALIGNTOP**](list-view-window-styles.md) (impostazione predefinita) o [**LVS \_ ALIGNLEFT.**](list-view-window-styles.md)

È possibile modificare l'allineamento dopo aver creato un controllo visualizzazione elenco. Per determinare l'allineamento corrente, usare il [**valore LVS \_ ALIGNMASK.**](list-view-window-styles.md)

Altri stili di finestra offrono altre opzioni, ad esempio se un utente può modificare le etichette o selezionare più di un elemento alla volta. Per un elenco completo, vedere [List-View Window Styles](list-view-window-styles.md).

### <a name="extended-list-view-styles"></a>Stili List-View estesi

Gli stili estesi dei controlli visualizzazione elenco offrono opzioni quali caselle di controllo, barre di scorrimento flat, linee griglia e rilevamento dello stato. Per un elenco completo, vedere [Stili List-View estesi.](extended-list-view-styles.md) Non è possibile accedere agli stili di visualizzazione elenco estesi in modo analogo agli stili di finestra standard. Non si usano le funzioni [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per apportare modifiche di stile estese.

Sono disponibili due messaggi che impostano e recuperano informazioni di stile estese, [**LVM \_ SETEXTENDEDLISTVIEWSTYLE**](lvm-setextendedlistviewstyle.md) [**e LVM \_ GETEXTENDEDLISTVIEWSTYLE.**](lvm-getextendedlistviewstyle.md) Invece di inviare i messaggi in modo esplicito, puoi usare le macro corrispondenti seguenti: [**\_ ListView SetExtendedListViewStyle,**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)e [**ListView \_ GetExtendedListViewStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle)

## <a name="virtual-list-view-style"></a>Stile List-View virtuale

Una visualizzazione elenco virtuale è un controllo visualizzazione elenco con lo stile [**LVS \_ OWNERDATA.**](list-view-window-styles.md) Questo stile consente al controllo di gestire milioni di elementi perché il proprietario riceve il carico di gestione dei dati degli elementi. In questo modo è possibile usare il controllo visualizzazione elenco virtuale con database di informazioni di grandi dimensioni, in cui sono già presenti metodi specifici di accesso ai dati.

Un controllo visualizzazione elenco virtuale mantiene pochissime informazioni sull'elemento stesso. Fatta eccezione per la selezione dell'elemento e le informazioni sullo stato attivo, il proprietario del controllo deve gestire tutte le informazioni sull'elemento. Altri processi richiedono informazioni sull'elemento al proprietario usando i codici di notifica [ \_ GETDISPINFO LVN.](lvn-getdispinfo.md)

Poiché questo tipo di controllo elenco è destinato a set di dati di grandi dimensioni, è consigliabile memorizzare nella cache i dati degli elementi richiesti per migliorare le prestazioni di recupero. La visualizzazione elenco fornisce un meccanismo di hint della cache per facilitare l'ottimizzazione della cache. L'hint viene implementato sotto forma di codice di notifica [ \_ ODCACHEHINT LVN.](lvn-odcachehint.md)

### <a name="creating-a-virtual-list-view-control"></a>Creazione di un controllo List-View virtuale

È possibile creare controlli visualizzazione elenco virtuali usando la [**funzione CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) specificando lo stile della finestra [**LVS \_ OWNERDATA**](list-view-window-styles.md) come parte del parametro della funzione *dwStyle.* Il passaggio dinamico da e verso lo stile **LVS \_ OWNERDATA** non è supportato.

È possibile usare lo stile [**LVS \_ OWNERDATA**](list-view-window-styles.md) in combinazione con la maggior parte degli altri stili di finestra, ad eccezione dello stile [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING.**](list-view-window-styles.md) Per impostazione predefinita, tutti i controlli visualizzazione elenco virtuale hanno lo stile [**\_ LVS AUTOARRANGE.**](list-view-window-styles.md)

Per abilitare la visualizzazione degli elementi nell'elenco, è prima necessario inviare il messaggio [**LVM \_ SETITEMCOUNT,**](lvm-setitemcount.md) in modo esplicito o tramite la macro [**\_ ListView SetItemCountEx.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex)

I messaggi seguenti non sono supportati con lo stile [**LVS \_ OWNERDATA:**](list-view-window-styles.md) [**LVM \_ ENABLEGROUPVIEW,**](lvm-enablegroupview.md) [**LVM \_ GETITEMTEXT,**](lvm-getitemtext.md) [**LVM \_ SETTILEINFO**](lvm-settileinfo.md)e [**LVM \_ MAPIDTOINDEX.**](lvm-mapidtoindex.md)

### <a name="compatibility-issues"></a>Problemi di compatibilità

Tutti e quattro gli stili di visualizzazione elenco, ovvero icona, icona piccola, elenco e visualizzazione report, supportano lo stile [**LVS \_ OWNERDATA.**](list-view-window-styles.md) I controlli visualizzazione elenco con lo stile **LVS \_ OWNERDATA** non archiviano informazioni specifiche dell'elemento. Di conseguenza, gli unici flag di stato dell'elemento validi che è possibile applicare a un elemento sono [**LVIS \_ SELECTED**](list-view-item-states.md) e [**LVIS \_ FOCUSED.**](list-view-item-states.md) Non vengono archiviate altre informazioni sullo stato. In particolare, il controllo visualizzazione elenco non mantiene le immagini di stato o di sovrapposizione per ogni elemento. Tuttavia, è possibile fare in modo che il controllo visualizzazione elenco eservi una query sull'applicazione per queste immagini inviando un [**messaggio LVM \_ SETCALLBACKMASK.**](lvm-setcallbackmask.md)

La maggior parte dei messaggi di controllo visualizzazione elenco e le macro associate sono completamente supportate. Tuttavia, alcuni messaggi presentano limitazioni o non sono supportati quando si usa lo stile [**LVS \_ OWNERDATA.**](list-view-window-styles.md) Nella tabella seguente vengono riepilogati i messaggi interessati.



| Message                                             | Limitazione                                                                                                                                                                                                                                                      |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LVM \_ ARRANGE**](lvm-arrange.md)                 | Non supporta lo stile **LVA \_ SNAPTOGRID.**                                                                                                                                                                                                                 |
| [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md)   | Imposta il conteggio degli elementi su zero e cancella tutte le variabili di selezione interne, ma non elimina effettivamente alcun elemento. Esegue un callback di notifica.                                                                                                           |
| [**LVM \_ DELETEITEM**](lvm-deleteitem.md)           | È supportato solo per l'integrità della selezione e non elimina effettivamente un elemento.                                                                                                                                                                                 |
| [**LVM \_ GETITEMSTATE**](lvm-getitemstate.md)       | Restituisce solo gli stati di stato attivo e di selezione, ovvero gli stati archiviati dal controllo visualizzazione elenco.                                                                                                                                                                |
| [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md)         | Non supporta i criteri di ricerca di visualizzazione elenco **LVNI \_ CUT,** **LVNI \_ HIDDEN** o **LVNI \_ DROP PIÙ.** Tutti gli altri criteri sono supportati.                                                                                                                     |
| [**LVM \_ GETWORKAREAS**](lvm-getworkareas.md)       | Non è supportata.                                                                                                                                                                                                                                               |
| [**LVM \_ INSERTITEM**](lvm-insertitem.md)           | È supportato solo per l'integrità della selezione.                                                                                                                                                                                                                      |
| [**LVM \_ SETITEM**](lvm-setitem.md)                 | Non è supportata. Per impostare lo stato dell'elemento, usare il [**messaggio \_ ListView SetItemState.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate)                                                                                                                                               |
| [**LVM \_ SETITEMCOUNT**](lvm-setitemcount.md)       | Imposta il numero di elementi attualmente presenti nell'elenco. Se il controllo visualizzazione elenco invia una notifica che richiede dati per qualsiasi elemento fino al set massimo, il proprietario deve essere preparato a fornire i dati. I parametri del messaggio supportano i controlli visualizzazione elenco virtuali. |
| [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) | Non è supportata.                                                                                                                                                                                                                                               |
| [**LVM \_ SETITEMSTATE**](lvm-setitemstate.md)       | Consente solo la modifica degli stati di selezione e stato attivo per l'elemento.                                                                                                                                                                                          |
| [**LVM \_ SETITEMTEXT**](lvm-setitemtext.md)         | Non è supportata. È responsabilità dell'applicazione mantenere i testi degli elementi.                                                                                                                                                                            |
| [**LVM \_ SETWORKAREAS**](lvm-setworkareas.md)       | Non è supportata.                                                                                                                                                                                                                                               |
| [**LVM \_ SORTITEMS**](lvm-sortitems.md)             | Non è supportata. È responsabilità dell'applicazione presentare gli elementi nell'ordine desiderato.                                                                                                                                                             |



 

### <a name="handling-virtual-list-view-control-notification-codes"></a>Gestione dei codici di notifica di List-View virtuali

I controlli visualizzazione elenco con lo stile [**LVS \_ OWNERDATA**](list-view-window-styles.md) inviano gli stessi codici di notifica degli altri controlli visualizzazione elenco e due controlli aggiuntivi: [LVN \_ ODCACHEHINT](lvn-odcachehint.md) e [LVN \_ ODFINDITEM.](lvn-odfinditem.md) Di seguito sono riportate le notifiche più comuni inviate dal controllo visualizzazione elenco con lo stile **LVS \_ OWNERDATA.**



|      Notifica                    |     Descrizione                         |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LVN \_ GETDISPINFO](lvn-getdispinfo.md) | Un controllo visualizzazione elenco virtuale mantiene pochissime informazioni sugli elementi in modo specifico. Di conseguenza, spesso invia il codice di notifica [ \_ LVN GETDISPINFO](lvn-getdispinfo.md) per richiedere informazioni sull'elemento. Questo messaggio viene gestito in modo molto identico agli elementi di callback in un controllo elenco standard. Poiché il numero di elementi supportati dal controllo può essere molto elevato, la memorizzazione nella cache dei dati degli elementi migliora le prestazioni. Quando si gestisce LVN GETDISPINFO, il proprietario del controllo tenta prima di tutto di fornire le informazioni sugli elementi richieste dalla cache. Per altre informazioni, vedere \_ [Gestione della cache.](#cache-management) Se l'elemento richiesto non viene memorizzato nella cache, il proprietario deve essere preparato a fornire le informazioni con altri mezzi. |
| [LVN \_ ODCACHEHINT](lvn-odcachehint.md) | Una visualizzazione elenco virtuale invia il codice di notifica [ \_ LVN ODCACHEHINT](lvn-odcachehint.md) per facilitare l'ottimizzazione della cache. Il codice di notifica fornisce valori di indice inclusivi per un intervallo di elementi che consiglia di memorizzare nella cache. Al momento della ricezione del codice di notifica, il proprietario deve essere preparato a caricare la cache con le informazioni sull'elemento per l'intervallo richiesto in modo che le informazioni siano immediatamente disponibili quando viene inviato un messaggio [ \_ LVN GETDISPINFO.](lvn-getdispinfo.md)                                                                                                                                                                                                                                   |
| [LVN \_ ODFINDITEM](lvn-odfinditem.md)   | Il [codice di notifica \_ ODFINDITEM LVN](lvn-odfinditem.md) viene inviato da un controllo di visualizzazione elenco virtuale quando il controllo richiede al proprietario di trovare un particolare elemento di callback. Il codice di notifica viene inviato quando il controllo visualizzazione elenco riceve l'accesso rapido al tasto o quando riceve un [**messaggio \_ LVM FINDITEM.**](lvm-finditem.md) Le informazioni di ricerca vengono inviate sotto forma di struttura [**LVFINDINFO,**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) che è un membro della [**struttura NMLVFINDITEM.**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) Il proprietario deve essere preparato a cercare un elemento che corrisponda alle informazioni fornite dal controllo di visualizzazione elenco. Il proprietario restituisce l'indice dell'elemento in caso di esito positivo oppure -1 se non viene trovato alcun elemento corrispondente.               |



 

### <a name="cache-management"></a>Gestione cache

Un controllo visualizzazione elenco con lo stile [**LVS \_ OWNERDATA**](list-view-window-styles.md) produce un numero elevato di codici di notifica [ \_ LVN GETDISPINFO](lvn-getdispinfo.md) e, per facilitare l'ottimizzazione della cache, un messaggio [ \_ ODCACHEHINT LVN.](lvn-odcachehint.md) I messaggi ODCACHEHINT LVN forniscono \_ informazioni sugli elementi consigliati da includere nella cache. Questi messaggi vengono inviati come [**messaggi WM \_ NOTIFY,**](wm-notify.md) con il valore *lParam* che funge da indirizzo di [**una struttura NMLVCACHEHINT.**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint)

La [**struttura NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) include due membri integer, **iFrom** e **iTo**, che rappresentano gli endpoint inclusivi di un intervallo di elementi che probabilmente saranno necessari. Il proprietario deve essere preparato a caricare la cache con le informazioni sull'elemento per ognuno degli elementi all'interno dell'intervallo consigliato.

Il controllo elenco richiede spesso informazioni sull'elemento per il primo elemento (offset 0). Il [codice di notifica \_ ODCACHEHINT LVN](lvn-odcachehint.md) potrebbe non includere sempre l'elemento 0, ma deve essere sempre incluso nella cache.

Si accede spesso agli ultimi elementi dell'elenco. Di conseguenza, il proprietario potrebbe voler mantenere una seconda cache che include gli elementi alla fine dell'elenco. L'intervallo richiesto [da \_ ODCACHEHINT LVN](lvn-odcachehint.md) può essere controllato rispetto alla cache finale per renderlo disponibile automaticamente anziché ricaricare lo stesso intervallo finale ogni volta.

## <a name="list-view-working-areas"></a>List-View di lavoro

I controlli visualizzazione elenco supportano le aree di lavoro, ovvero aree virtuali rettangolari utilizzate dal controllo visualizzazione elenco per disporre gli elementi. Un'area di lavoro non è una finestra e non può avere un bordo visibile. Per impostazione predefinita, il controllo visualizzazione elenco non ha aree di lavoro. Creando un'area di lavoro, è possibile creare un bordo vuoto a sinistra, in alto o a destra degli elementi oppure fare in modo che una barra di scorrimento orizzontale sia visualizzata quando normalmente non ne esiste uno.

Quando viene creata un'area di lavoro, gli elementi che si trovano all'interno dell'area di lavoro diventano membri dell'area di lavoro. Analogamente, se un elemento viene spostato in un'area di lavoro, l'elemento diventa un membro di tale area di lavoro. Se un elemento non si trova all'interno di alcuna area di lavoro, diventa automaticamente un membro della prima area di lavoro (indice 0). Per inserire un nuovo elemento all'interno di un'area di lavoro specifica, è necessario prima di tutto creare l'elemento e quindi usare [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) o il messaggio [**LVM \_ SETITEMPOSITION32**](lvm-setitemposition32.md) per spostarlo nell'area di lavoro desiderata.

La figura seguente è un esempio di controllo visualizzazione elenco che contiene quattro aree di lavoro, ognuna in un quadrante diverso dell'area client.

![Screenshot di un controllo visualizzazione elenco con un'area di lavoro in ogni quadrante dell'area client](images/working.jpg)

È possibile usare più aree di lavoro per creare aree diverse all'interno di un'unica visualizzazione. È possibile creare aree in un'unica visualizzazione con significati diversi. Ad esempio, una visualizzazione di un file system potrebbe avere un'area per i file di lettura/scrittura e un'altra area per i file di sola lettura. L'utente può classificare gli elementi inserendoli in aree di lavoro diverse. Se un file viene spostato nell'area di sola lettura, diventerà automaticamente di sola lettura.

Più aree di lavoro possono intersecarsi, ma tutti gli elementi che si trovano all'interno dell'intersezione diventano membri dell'area con l'indice inferiore; Pertanto, è meglio evitare questa situazione. Quando si ordinano più aree di lavoro, gli elementi vengono ordinati rispetto agli altri elementi nella stessa area di lavoro.

Il numero di aree di lavoro può essere recuperato con il messaggio [**LVM \_ GETNUMBEROFWORKAREAS.**](lvm-getnumberofworkareas.md) Le aree di lavoro vengono modificate con il messaggio [**LVM \_ SETWORKAREAS**](lvm-setworkareas.md) e possono essere recuperate con il messaggio [**LVM \_ GETWORKAREAS.**](lvm-getworkareas.md) Entrambi questi messaggi accettano l'indirizzo di una matrice di strutture [**RECT**](/previous-versions//dd162897(v=vs.85)) come *lParam* e il numero di strutture **RECT** come *wParam*. I **membri** sinistro e superiore di queste strutture specificano le coordinate dell'angolo superiore  sinistro  (origine) dell'area di lavoro e i membri destro e inferiore specificano l'angolo inferiore destro dell'area di lavoro.  Tutte le coordinate sono in coordinate client della visualizzazione elenco. Il numero massimo di aree di lavoro consentite è definito dal **valore LV \_ MAX \_ WORKAREAS.**

La modifica dell'area di lavoro non ha alcun effetto sui controlli visualizzazione elenco con la visualizzazione [**LVS \_ LIST**](list-view-window-styles.md) o [**LVS \_ REPORT,**](list-view-window-styles.md) ma le aree di lavoro verranno mantenute quando il tipo di visualizzazione viene modificato. Con le [**visualizzazioni LVS \_ ICON**](list-view-window-styles.md) e [**LVS \_ SMALLICON,**](list-view-window-styles.md) l'area di lavoro può essere modificata per modificare la modalità di visualizzazione degli elementi. Se la larghezza dell'area di lavoro (da destra a sinistra) è maggiore della larghezza client del controllo, viene eseguito il wrapping degli elementi a tale larghezza e viene visualizzata la barra di scorrimento orizzontale. Rendendo la larghezza dell'area di lavoro più stretta rispetto alla larghezza dell'area client del controllo, viene eseguito il wrapping degli elementi all'interno dell'area di lavoro e non dell'area client. Se si  **imposta** il membro sinistro o superiore su un valore positivo, gli elementi vengono visualizzati a partire dall'area di lavoro, creando uno spazio vuoto tra il bordo del controllo e gli elementi. È anche possibile creare uno spazio vuoto tra il bordo destro del controllo e gli elementi rendendo la larghezza dell'area di lavoro inferiore alla larghezza client del controllo.

## <a name="list-view-image-lists"></a>List-View di immagini

Per impostazione predefinita, un controllo visualizzazione elenco non visualizza le immagini degli elementi. Per visualizzare le immagini degli elementi, è necessario creare elenchi di immagini e associarli al controllo . Un controllo visualizzazione elenco può avere tre elenchi di immagini:

-   Elenco di immagini che contiene icone di dimensioni complete visualizzate quando il controllo è nella visualizzazione icone.
-   Elenco di immagini che contiene icone piccole visualizzate quando il controllo si trova nella visualizzazione icona piccola, nella visualizzazione elenco o nella visualizzazione report.
-   Elenco di immagini che contiene immagini di stato, visualizzate a sinistra dell'icona a dimensione intera o piccola. È possibile usare immagini di stato, ad esempio caselle di controllo selezionate e deselezionate, per indicare gli stati degli elementi definiti dall'applicazione. Le immagini di stato vengono visualizzate nella visualizzazione icona, nella visualizzazione icona piccola, nella visualizzazione elenco e nella visualizzazione report.

Gli elenchi di immagini di icone grandi e piccole possono contenere anche immagini sovrapposte, progettate per essere disegnate in modo trasparente sulle icone degli elementi.

Per usare immagini sovrapposte in un controllo visualizzazione elenco:

1.  Chiamare la [**funzione ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) per assegnare un indice di immagine di sovrimpressione a un'immagine negli elenchi di immagini di icone di piccole e grandi dimensioni. Un'immagine di sovrimpressione è identificata da un indice in base uno.
2.  Puoi associare un indice di immagine sovrapposta a un elemento quando chiami la macro [**\_ ListView InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) o [**ListView \_ SetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) Usare la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) per specificare un indice di immagine di sovrimpressione nel membro **di** stato della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dell'elemento. È inoltre necessario impostare i bit [**\_ LVIS OVERLAYMASK**](list-view-item-states.md) nel **membro stateMask.**

Se viene specificato un elenco di immagini di stato, un controllo visualizzazione elenco riserva spazio a sinistra dell'icona di ogni elemento per un'immagine di stato.

Per associare un'immagine di stato a un elemento, usare la macro [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) per specificare un indice dell'immagine di stato nel membro **di** stato della [**struttura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) L'indice identifica un'immagine nell'elenco di immagini di stato del controllo. Anche se gli indici dell'elenco immagini sono in base zero, il controllo usa indici in base uno per identificare le immagini di stato. Un indice dell'immagine di stato pari a zero indica che un elemento non dispone di un'immagine di stato.

Per impostazione predefinita, quando un controllo visualizzazione elenco viene eliminato, elimina gli elenchi di immagini assegnati. Tuttavia, se un controllo visualizzazione elenco ha lo stile di finestra [**LVS \_ SHAREIMAGELISTS,**](list-view-window-styles.md) l'applicazione è responsabile dell'eliminazione degli elenchi di immagini quando non sono più in uso. È necessario specificare questo stile se si assegnano gli stessi elenchi di immagini a più controlli visualizzazione elenco. In caso contrario, più controlli potrebbero tentare di eliminare lo stesso elenco di immagini.

## <a name="list-view-items-and-subitems"></a>List-View elementi ed elementi secondari

Ogni elemento in un controllo visualizzazione elenco ha un'icona, un'etichetta, uno stato corrente e un valore definito dall'applicazione. Usando i messaggi di visualizzazione elenco, è possibile aggiungere, modificare ed eliminare elementi, nonché recuperare informazioni sugli elementi.

Ogni elemento può avere uno o più *elementi secondari.* Un elemento secondario è una stringa che, nella visualizzazione report, viene visualizzata in una colonna separata dall'icona e dall'etichetta dell'elemento. Per specificare il testo di un elemento secondario, usare il [**messaggio LVM \_ SETITEMTEXT**](lvm-setitemtext.md) o [**LVM \_ SETITEM.**](lvm-setitem.md) Tutti gli elementi in un controllo visualizzazione elenco hanno lo stesso numero di elementi secondari. Il numero di elementi secondari è determinato dal numero di colonne nel controllo visualizzazione elenco. Quando si aggiunge una colonna a un controllo visualizzazione elenco, si specifica l'indice dell'elemento secondario associato.

La [**struttura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) definisce un elemento di visualizzazione elenco o un elemento secondario. Il **membro iItem** è l'indice in base zero dell'elemento. Il **membro iSubItem** è l'indice in base uno di un elemento secondario o zero se la struttura contiene informazioni su un elemento. I membri aggiuntivi specificano il testo, l'icona, lo stato e i dati dell'elemento dell'elemento. *I dati dell'elemento* sono un valore definito dall'applicazione associato a un elemento di visualizzazione elenco.

Per aggiungere un elemento a un controllo di visualizzazione elenco, usare il messaggio [**LVM \_ INSERTITEM,**](lvm-insertitem.md) specificando l'indirizzo di una struttura [**LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Prima di aggiungere più elementi, è possibile inviare al controllo un messaggio [**LVM \_ SETITEMCOUNT,**](lvm-setitemcount.md) specificando il numero di elementi che il controllo conterrà. Questo messaggio consente al controllo visualizzazione elenco di riallocare le strutture di dati interne una sola volta anziché ogni volta che si aggiunge un elemento. È possibile determinare il numero di elementi in un controllo visualizzazione elenco usando il messaggio [**LVM \_ GETITEMCOUNT.**](lvm-getitemcount.md) Se si aggiunge un numero elevato di elementi a un controllo visualizzazione elenco, è possibile velocizzare il processo disabilitando il ridisegno prima di aggiungere gli elementi, quindi abilitare il ridisegno dopo l'aggiunta degli elementi. Usare il [**messaggio WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw) per abilitare e disabilitare il ridisegno.

Per modificare gli attributi di un elemento di visualizzazione elenco, usare il messaggio [**\_ LVM SETITEM,**](lvm-setitem.md) specificando l'indirizzo di una [**struttura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Il **membro mask** di questa struttura specifica gli attributi dell'elemento da modificare. Ad esempio, per modificare solo il testo di un elemento o di un elemento secondario, usare il [**messaggio \_ LVM SETITEMTEXT.**](lvm-setitemtext.md)

Per recuperare informazioni su un elemento di visualizzazione elenco, usare il messaggio [**\_ LVM GETITEM,**](lvm-getitem.md) specificando l'indirizzo della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) da compilare. Il **membro mask** di questa struttura specifica gli attributi dell'elemento da recuperare. Per recuperare solo il testo di un elemento o di un elemento secondario, usare il [**messaggio LVM \_ GETITEMTEXT.**](lvm-getitemtext.md)

Per eliminare un elemento di visualizzazione elenco, usare il [**messaggio LVM \_ DELETEITEM.**](lvm-deleteitem.md) È possibile eliminare tutti gli elementi in un controllo visualizzazione elenco usando il [**messaggio LVM \_ DELETEALLITEMS.**](lvm-deleteallitems.md)

### <a name="list-view-item-states"></a>List-View stati degli elementi

Lo stato di un elemento è un valore che specifica la disponibilità dell'elemento, indica le azioni dell'utente o riflette in altro modo lo stato dell'elemento. Un controllo visualizzazione elenco modifica alcuni bit di stato, ad esempio quando l'utente seleziona un elemento. Un'applicazione può modificare altri bit di stato per disabilitare o nascondere l'elemento o per specificare un'immagine di sovrimpressione o un'immagine di stato. Per altre informazioni sulle immagini sovrapposte e le immagini di stato, vedere [List-View Image Lists](#list-view-image-lists).

Lo stato di un elemento viene specificato dal **membro di** stato della [**struttura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Quando si specifica o si modifica lo stato di un elemento, il **membro stateMask** specifica quali bit di stato è necessario modificare. È possibile modificare lo stato di un elemento usando il [**messaggio \_ LVM SETITEMSTATE.**](lvm-setitemstate.md) È possibile specificare lo stato di un elemento quando viene creato o quando si modificano gli attributi usando il messaggio [**\_ LVM SETITEM.**](lvm-setitem.md) Per determinare lo stato corrente di un elemento, usare il [**messaggio LVM \_ GETITEMSTATE**](lvm-getitemstate.md) o [**LVM \_ GETITEM.**](lvm-getitem.md)

Per impostare l'immagine di sovrimpressione di un elemento, il membro **stateMask** della  struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deve includere il valore [**LVIS \_ OVERLAYMASK**](list-view-item-states.md) e il membro di stato deve includere l'indice in base uno dell'immagine sovrapposta spostata a sinistra di 8 bit usando la macro [**INDEXTOOVERLAYMASK.**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) L'indice può essere zero per non specificare alcuna immagine di sovrimpressione.

Per impostare l'immagine di stato di un elemento, il membro **stateMask** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deve includere il valore [**LVIS \_ STATEIMAGEMASK**](list-view-item-states.md) e il membro di stato deve includere l'indice in base uno dell'immagine di stato spostata a sinistra di 12 bit usando la macro [**INDEXTOSTATEIMAGEMASK.**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask)  L'indice può essere zero per non specificare alcuna immagine di stato.

### <a name="callback-items-and-the-callback-mask"></a>Elementi di callback e maschera di callback

Per ogni elemento, un controllo visualizzazione elenco archivia in genere il testo dell'etichetta, l'indice dell'elenco immagini delle icone dell'elemento e un set di flag di bit per lo stato dell'elemento. È possibile definire elementi di callback o modificare la maschera di callback del controllo per indicare che l'applicazione, anziché il controllo, archivia alcune o tutte queste informazioni. È possibile usare i callback se l'applicazione archivia alcune di queste informazioni.

Un *elemento di callback* in un controllo visualizzazione elenco è un elemento per il quale l'applicazione archivia l'indice di testo o icona o entrambi. È possibile definire elementi di callback quando si invia il [**messaggio LVM \_ INSERTITEM**](lvm-insertitem.md) per aggiungere un elemento al controllo visualizzazione elenco. Se l'applicazione archivia il testo per l'elemento o l'elemento secondario, impostare il membro **pszText** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dell'elemento su **LPSTR \_ TEXTCALLBACK**. Se l'applicazione archivia l'indice delle icone per un elemento, impostare il membro **iImage** della struttura **LVITEM** dell'elemento su **I \_ IMAGECALLBACK.**

La *maschera di callback* di un controllo visualizzazione elenco è un set di flag di bit che specificano gli stati degli elementi per i quali l'applicazione, anziché il controllo, archivia i dati correnti. La maschera di callback si applica a tutti gli elementi del controllo, a differenza della designazione dell'elemento di callback, che si applica a un elemento specifico. La maschera di callback è zero per impostazione predefinita, vale a dire che il controllo visualizzazione elenco archivia tutte le informazioni sullo stato degli elementi. Dopo aver creato un controllo visualizzazione elenco e aver inizializzato i relativi elementi, è possibile inviare il messaggio [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) per modificare la maschera di callback. Per recuperare la maschera di callback corrente, inviare il [**messaggio LVM \_ GETCALLBACKMASK.**](lvm-getcallbackmask.md)

Quando un controllo visualizzazione elenco deve visualizzare o ordinare un elemento di visualizzazione elenco per il quale l'applicazione archivia informazioni di callback, il controllo invia il codice di notifica [ \_ LVN GETDISPINFO](lvn-getdispinfo.md) alla finestra padre del controllo. Questo messaggio specifica una struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) che contiene il tipo di informazioni necessarie e identifica l'elemento o l'elemento secondario da recuperare. La finestra padre deve elaborare LVN \_ GETDISPINFO per fornire i dati richiesti.

Se il controllo visualizzazione elenco rileva una modifica nelle informazioni di callback di un elemento, ad esempio una modifica nel testo, nell'icona o nelle informazioni sullo stato, il controllo invia un codice di notifica [ \_ LVN SETDISPINFO](lvn-setdispinfo.md) per notificare la modifica.

Se si modificano gli attributi o i bit di stato di un elemento di callback, si usa il messaggio [**LVM \_ UPDATE**](lvm-update.md) per forzare il controllo a ridisegnare l'elemento. Questo messaggio fa sì che il controllo disporrà gli elementi se ha lo stile [**LVS \_ AUTOARRANGE.**](list-view-window-styles.md) È possibile usare [**il messaggio LVM \_ REDRAWITEMS**](lvm-redrawitems.md) per ridisegnare un intervallo di elementi invalidando le parti corrispondenti dell'area client del controllo visualizzazione elenco.

Usando in modo efficace gli elementi di callback e la maschera di callback, è possibile assicurarsi che ogni attributo dell'elemento sia mantenuto in un'unica posizione. Questa operazione può semplificare l'applicazione, ma l'unico spazio salvato è la memoria che altrimenti sarebbe necessaria per archiviare le etichette degli elementi e il testo degli elementi secondari.

### <a name="list-view-item-position"></a>List-View posizione dell'elemento

Ogni elemento della visualizzazione elenco ha una posizione e una dimensione, che è possibile recuperare e impostare usando i messaggi. È anche possibile determinare quale elemento, se presente, si trova in una posizione specificata. La posizione degli elementi della visualizzazione elenco viene specificata nelle coordinate *di* visualizzazione , che sono coordinate client offset dalla posizione di scorrimento.

Per recuperare e impostare la posizione di un elemento, usare i messaggi [**LVM \_ GETITEMPOSITION**](lvm-getitemposition.md) e [**LVM \_ SETITEMPOSITION.**](lvm-setitemposition.md) **LVM \_ GETITEMPOSITION funziona** per tutte le viste, ma **LVM \_ SETITEMPOSITION** funziona solo per le visualizzazioni icona e icona piccola.

È possibile determinare quale elemento, se presente, si trova in una posizione specifica usando il [**messaggio LVM \_ HITTEST.**](lvm-hittest.md)

Per recuperare il rettangolo di delimitazione per un elemento dell'elenco o solo per l'icona o l'etichetta, usare il messaggio [**LVM \_ GETITEMRECT.**](lvm-getitemrect.md)

### <a name="arranging-sorting-and-finding-items"></a>Disposizione, ordinamento e ricerca di elementi

È possibile usare i messaggi di visualizzazione elenco per disporre e ordinare gli elementi e per trovare gli elementi in base ai relativi attributi o posizioni. La disposizione riposiziona gli elementi in modo che siano allineati in una griglia, ma gli indici degli elementi non cambiano. L'ordinamento modifica la sequenza di elementi (e i relativi indici corrispondenti) e quindi li riposiziona di conseguenza. È possibile disporre gli elementi solo nelle visualizzazioni icona e icona piccola, ma è possibile ordinare gli elementi in qualsiasi visualizzazione. Per trovare gli elementi, inviare messaggi di visualizzazione elenco che specificano la posizione o la proprietà di un elemento.

Per disporre gli elementi, usare il [**messaggio LVM \_ ARRANGE.**](lvm-arrange.md) È possibile assicurarsi che gli elementi siano disposti in qualsiasi momento specificando lo stile della finestra [**LVS \_ AUTOARRANGE.**](list-view-window-styles.md)

Per ordinare gli elementi, usare il [**messaggio \_ LVM SORTITEMS.**](lvm-sortitems.md) Quando si esegue l'ordinamento usando questo messaggio, si specifica una funzione di callback definita dall'applicazione chiamata dal controllo visualizzazione elenco per confrontare l'ordine relativo di due elementi qualsiasi. Il controllo passa alla funzione di confronto i dati dell'elemento associati a ognuno dei due elementi. I dati dell'elemento sono il valore specificato nel membro **lParam** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dell'elemento quando è stato inserito nell'elenco. Specificando i dati degli elementi appropriati e fornendo una funzione di confronto appropriata, è possibile ordinare gli elementi in base all'etichetta, a qualsiasi elemento secondario o a qualsiasi altra proprietà. Si noti che l'ordinamento degli elementi non riordina gli elementi secondari corrispondenti. Quando gli elementi vengono riordinati, vengono trasportati gli elementi secondari corrispondenti; in altre informazioni, le righe intere vengono mantenute insieme. Per ordinare le colonne separatamente l'una dall'altra, scollegando gli elementi secondari dai relativi elementi, è necessario rigenerare le colonne dopo l'ordinamento usando [**LVM \_ SETITEM**](lvm-setitem.md).

È possibile assicurarsi che un controllo visualizzazione elenco sia sempre ordinato specificando lo stile della finestra [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING.**](list-view-window-styles.md) I controlli con questi stili usano il testo dell'etichetta degli elementi per ordinarli in ordine crescente o decrescente. Non è possibile fornire una funzione di confronto quando si usano questi stili di finestra. Se un controllo visualizzazione elenco ha uno di questi stili, un messaggio [**LVM \_ INSERTITEM**](lvm-insertitem.md) avrà esito negativo se si tenta di inserire un elemento con **LPSTR \_ TEXTCALLBACK** come membro **pszText** della struttura [**LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)

È possibile trovare un elemento di visualizzazione elenco con proprietà specifiche usando il [**messaggio \_ LVM FINDITEM.**](lvm-finditem.md) È possibile trovare un elemento di visualizzazione elenco che si trova in uno stato specificato e ha una relazione specificata con un determinato elemento usando il [**messaggio LVM \_ GETNEXTITEM.**](lvm-getnextitem.md) Ad esempio, è possibile recuperare l'elemento selezionato successivo a destra di un elemento specificato.

## <a name="list-view-columns"></a>List-View colonne

Le colonne controllano la modalità di visualizzazione degli elementi e dei relativi elementi secondari nella visualizzazione report. Ogni colonna ha un titolo e una larghezza ed è associata a un elemento secondario specifico. l'elemento secondario zero è l'icona e l'etichetta dell'elemento. Gli attributi di una colonna sono definiti da una [**struttura LVCOLUMN.**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)

Per aggiungere una colonna a un controllo visualizzazione elenco, usare il [**messaggio LVM \_ INSERTCOLUMN.**](lvm-insertcolumn.md) Per eliminare una colonna, usare il [**messaggio LVM \_ DELETECOLUMN.**](lvm-deletecolumn.md)

> [!Note]  
> L'eliminazione della colonna zero di un controllo visualizzazione elenco è supportata solo ComCtl32.dll versione 6 e successive. La versione 5 supporta anche l'eliminazione della colonna zero, ma solo dopo aver utilizzato [**CCM \_ SETVERSION**](ccm-setversion.md) per impostare la versione su 5 o versione successiva. Le versioni precedenti alla versione 5 non supportano l'eliminazione della colonna zero.

 

È possibile recuperare e modificare le proprietà di una colonna esistente usando i messaggi [**LVM \_ GETCOLUMN**](lvm-getcolumn.md) e [**LVM \_ SETCOLUMN.**](lvm-setcolumn.md) Per recuperare o modificare la larghezza di una colonna, usare i messaggi [**LVM \_ GETCOLUMNWIDTH**](lvm-getcolumnwidth.md) e [**LVM \_ SETCOLUMNWIDTH.**](lvm-setcolumnwidth.md)

A meno che non venga specificato lo stile della finestra [**\_ LVS NOCOLUMNHEADER,**](list-view-window-styles.md) le intestazioni di colonna vengono visualizzate nella visualizzazione report. L'utente può fare clic su un'intestazione di colonna, causando l'invio di un codice di notifica [**\_ LVN COLUMNCLICK**](lvn-columnclick.md) alla finestra padre. In genere, la finestra padre ordina il controllo visualizzazione elenco in base alla colonna specificata quando si fa clic. L'utente può anche trascinare le guide di colonna tra le intestazioni per ridimensionare le colonne.

I controlli visualizzazione elenco possono visualizzare immagini accanto ai titoli delle colonne. Per implementare questa funzionalità, specificare il valore **LVCF \_ IMAGE** e assegnare l'indice dell'immagine al membro **iImage** nella [**struttura LVCOLUMN.**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)

I controlli visualizzazione elenco possono impostare l'ordine di visualizzazione delle colonne. Per implementare questa funzionalità, specificare il **valore LVCF \_ ORDER** e assegnare l'ordine delle colonne al membro **iOrder** nella struttura [**LVCOLUMN.**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) L'ordine delle colonne è in base zero ed è in ordine da sinistra a destra. Ad esempio, zero indica la colonna più a sinistra.

## <a name="list-view-scroll-position"></a>List-View posizione di scorrimento

A meno che non venga specificato lo stile della finestra [**\_ LVS NOSCROLL,**](list-view-window-styles.md) è possibile scorrere un controllo visualizzazione elenco per visualizzare più elementi di quelli che possono rientrare nell'area client del controllo. È possibile recuperare la posizione di scorrimento di un controllo visualizzazione elenco e le informazioni correlate, scorrere un controllo visualizzazione elenco in base a una quantità specificata o scorrere un controllo visualizzazione elenco in modo che un elemento di elenco specificato sia visibile.

Nella visualizzazione icona o nella visualizzazione icona piccola, la posizione di scorrimento corrente è definita dall'origine *della visualizzazione.* L'origine della visualizzazione è il set di coordinate, relative all'area visibile del controllo visualizzazione elenco, che corrispondono alle coordinate di visualizzazione (0, 0). Per recuperare l'origine della visualizzazione corrente, usare il [**messaggio LVM \_ GETORIGIN.**](lvm-getorigin.md) Questo messaggio deve essere usato solo nella visualizzazione icona o icona piccola. restituisce un errore nella visualizzazione elenco o report.

Nella visualizzazione elenco o report la posizione di scorrimento corrente è definita *dall'indice superiore.* L'indice superiore è l'indice del primo elemento visibile nel controllo visualizzazione elenco. Per recuperare l'indice principale corrente, usare il [**messaggio LVM \_ GETTOPINDEX.**](lvm-gettopindex.md) Questo messaggio restituisce un risultato valido solo nella visualizzazione elenco o report. restituisce zero nella visualizzazione icona o icona piccola.

È possibile usare il messaggio [**LVM \_ GETVIEWRECT**](lvm-getviewrect.md) per recuperare il rettangolo di delimitazione di tutti gli elementi in un controllo visualizzazione elenco, rispetto all'area visibile del controllo.

Il [**messaggio LVM \_ GETCOUNTPERPAGE**](lvm-getcountperpage.md) restituisce il numero di elementi che rientrano in una pagina del controllo di visualizzazione elenco. Questo messaggio restituisce un risultato valido solo nelle visualizzazioni elenco e report. nelle visualizzazioni icona e icona piccola, restituisce il numero totale di elementi.

Per scorrere un controllo visualizzazione elenco di una quantità specifica, usare il [**messaggio LVM \_ SCROLL.**](lvm-scroll.md) Usando il [**messaggio LVM \_ ENSUREVISIBLE,**](lvm-ensurevisible.md) è possibile scorrere il controllo di visualizzazione elenco, se necessario, per assicurarsi che un elemento specificato sia visibile.

## <a name="list-view-label-editing"></a>List-View di etichette

Un controllo visualizzazione elenco con lo stile della finestra [**\_ LVS EDITLABELS**](list-view-window-styles.md) consente a un utente di modificare le etichette degli elementi sul posto. L'utente inizia a modificare facendo clic sull'etichetta di un elemento con lo stato attivo. In alternativa, un'applicazione può iniziare a modificare automaticamente usando il [**messaggio LVM \_ EDITLABEL.**](lvm-editlabel.md) Il controllo visualizzazione elenco invia una notifica alla finestra padre quando inizia la modifica e quando viene annullata o completata. Al termine della modifica, la finestra padre è responsabile dell'aggiornamento dell'etichetta dell'elemento, se appropriato.

Quando inizia la modifica delle etichette, [viene](edit-controls.md) creato, posizionato e inizializzato un controllo di modifica. Prima della visualizzazione, il controllo visualizzazione elenco invia alla finestra padre un codice di notifica [LVN \_ BEGINLABELEDIT.](lvn-beginlabeledit.md) Se è necessario modificare il processo di modifica delle etichette, è possibile implementare un gestore per questa notifica.

Un uso per un gestore [di notifica LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) è controllare le etichette che l'utente può modificare. Per impedire la modifica delle etichette, restituire un valore diverso da zero. Per personalizzare la modifica delle etichette, fare in modo che il gestore di notifica recuperi un handle per il controllo di modifica inviando un messaggio [**LVM \_ GETEDITCONTROL**](lvm-geteditcontrol.md) al controllo visualizzazione elenco. Dopo aver creato tale handle, è possibile personalizzare il controllo di modifica inviando i soliti messaggi EM \_ XXX. Ad esempio, per limitare la quantità di testo che un utente può immettere, inviare al controllo di modifica un [**messaggio EM \_ LIMITTEXT.**](em-limittext.md) È possibile modificare il testo predefinito del controllo di modifica con [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta). È anche possibile sottoclassare il controllo di modifica per intercettare ed eliminare i caratteri non validi.

Quando la modifica delle etichette viene annullata o completata, un controllo visualizzazione elenco invia alla finestra padre un codice di notifica [ \_ LVN ENDLABELEDIT.](lvn-endlabeledit.md) Il *parametro lParam* è l'indirizzo di una [**struttura NMLVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) Il **membro dell'elemento** di questa struttura è una [**struttura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) il cui **membro iItem** identifica l'elemento. Se la modifica viene annullata, il **membro pszText** della struttura **LVITEM** è **NULL.** in caso **contrario, pszText** è l'indirizzo del testo modificato. La finestra padre è responsabile dell'aggiornamento dell'etichetta dell'elemento se vuole mantenere la nuova etichetta.

## <a name="list-view-colors"></a>List-View colori

Un'applicazione può recuperare e impostare tre colori per un controllo visualizzazione elenco.



| Color                   | Messaggi usati per recuperare e impostare i colori                                                             |
|-------------------------|------------------------------------------------------------------------------------------------------|
| Colore del testo              | [**LVM \_ GETTEXTCOLOR**](lvm-gettextcolor.md), [ **LVM \_ SETTEXTCOLOR**](lvm-settextcolor.md)         |
| Colore di sfondo del testo   | [**LVM \_ GETTEXTBKCOLOR**](lvm-gettextbkcolor.md), [ **LVM \_ SETTEXTBKCOLOR**](lvm-settextbkcolor.md) |
| Colore di sfondo della finestra | [**LVM \_ GETBKCOLOR**](lvm-getbkcolor.md), [ **LVM \_ SETBKCOLOR**](lvm-setbkcolor.md)                 |



 

Per personalizzare l'aspetto di un controllo visualizzazione elenco in modo più significativo, usare [NM \_ CUSTOMDRAW (visualizzazione elenco)](nm-customdraw-list-view.md) o gli stili di visualizzazione (vedere [Stili](themes-overview.md) di visualizzazione e Abilitazione [degli stili di visualizzazione).](cookbook-overview.md)

## <a name="arranging-list-items-by-group"></a>Disposizione degli elementi dell'elenco per gruppo

Le funzionalità di raggruppamento del controllo visualizzazione elenco consentono di raggruppare visivamente set di elementi correlati logicamente. I gruppi possono essere creati in base alle proprietà degli elementi, agli attributi o ad altre caratteristiche. Questi gruppi sono in genere separati sullo schermo da un'intestazione orizzontale che contiene il nome del gruppo. Lo screenshot seguente mostra gli elementi raggruppati.

![screenshot di un controllo visualizzazione elenco, con cani in un gruppo e gatti in un altro gruppo](images/lv-groups.png)

La struttura [**LVGROUP viene**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) utilizzata per archiviare informazioni su un gruppo, ad esempio il testo dell'intestazione e del piè di pagina, lo stato corrente del gruppo e così via. L'API di raggruppamento include messaggi che consentono di gestire i gruppi e gli elementi del gruppo aggiungendo elementi ai gruppi, aggiungendo gruppi alle visualizzazioni, ordinando gli elementi del gruppo ed eseguire query sui gruppi per le dimensioni degli elementi e altre informazioni. Ad esempio, è possibile impostare e recuperare i parametri di visualizzazione per ogni gruppo usando le macro [**\_ ListView SetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupmetrics) e [**ListView \_ GetGroupMetrics.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupmetrics)

Il raggruppamento è disponibile in tutte le visualizzazioni, ad eccezione della visualizzazione elenco. Non è disponibile nei controlli con lo stile [**LVS \_ OWNERDATA.**](list-view-window-styles.md)

Per altre informazioni, vedere [Using List-View Controls](using-list-view-controls.md).

## <a name="insertion-marks"></a>Segni di inserimento

I segni di inserimento mostrano agli utenti dove verranno posizionati gli elementi trascinati. I segni di inserimento vengono attualmente visualizzati quando l'utente trascina un elemento nel menu **Start** o Avvio veloce barra. Il segno di inserimento funziona anche per gli elenchi impostati su autoarrange. Quando un utente trascina un elemento in un punto intermedio tra due elementi, il segno di inserimento indica la nuova posizione prevista dell'elemento. La schermata seguente mostra un segno di inserimento.

![Screenshot che mostra un segno di inserimento quando si trascina un file tra due altri in un controllo visualizzazione elenco](images/insertmark.png)

Gli elementi API del segno di inserimento consentono il posizionamento dei segni di inserimento fornendo messaggi e flag che eseguono il rilevamento degli hit, che specificano la posizione e l'aspetto del segno di inserimento in base all'elemento e che eseguono una query per informazioni sulle dimensioni e sull'aspetto correnti del segno di inserimento.

## <a name="see-also"></a>Vedi anche

* [Esempio di controllo ListView virtuale](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)
