---
title: Informazioni sui controlli List-View
description: Un controllo visualizzazione elenco è una finestra che consente di visualizzare una raccolta di elementi.
ms.assetid: 163f7778-690c-4166-b0c5-c7be1a03ae98
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: fe1b953bf7d7204a3afffcfa0bc5aa5af9bf94fa
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323893"
---
# <a name="about-list-view-controls"></a>Informazioni sui controlli List-View

Vedere l' [esempio di controllo ListView virtuale](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw).

Un controllo visualizzazione elenco è una finestra che consente di visualizzare una raccolta di elementi. I controlli elenco-visualizzazione forniscono diversi modi per disporre e visualizzare gli elementi e sono molto più flessibili rispetto alle semplici [caselle di riepilogo](list-boxes.md). Ad esempio, è possibile visualizzare informazioni aggiuntive su ogni elemento in colonne a destra dell'icona e dell'etichetta.

-   [Stili e visualizzazioni di visualizzazione elenco](#list-view-styles-and-views)
    -   [Stili List-View estesi](#extended-list-view-styles)
-   [Stile List-View virtuale](#virtual-list-view-style)
    -   [Creazione di un controllo List-View virtuale](#creating-a-virtual-list-view-control)
    -   [Problemi di compatibilità](#compatibility-issues)
    -   [Gestione dei codici di notifica del controllo List-View virtuale](#handling-virtual-list-view-control-notification-codes)
    -   [Gestione della cache](#cache-management)
-   [Area di lavoro visualizzazione elenco](#list-view-working-areas)
-   [Elenchi di immagini visualizzazione elenco](#list-view-image-lists)
-   [Elementi e elementi secondari della visualizzazione elenco](#list-view-items-and-subitems)
    -   [Stato degli elementi della visualizzazione elenco](#list-view-item-states)
    -   [Elementi di callback e maschera di callback](#callback-items-and-the-callback-mask)
    -   [Posizione elemento visualizzazione elenco](#list-view-item-position)
    -   [Disposizione, ordinamento e ricerca di elementi](#arranging-sorting-and-finding-items)
-   [Colonne visualizzazione elenco](#list-view-columns)
-   [Posizione di scorrimento visualizzazione elenco](#list-view-scroll-position)
-   [Modifica dell'etichetta visualizzazione elenco](#list-view-label-editing)
-   [Colori visualizzazione elenco](#list-view-colors)
-   [Disposizione degli elementi dell'elenco per gruppo](#arranging-list-items-by-group)
-   [Segni di inserimento](#insertion-marks)

## <a name="list-view-styles-and-views"></a>Stili e visualizzazioni List-View

I controlli elenco-visualizzazione possono visualizzare elementi in cinque visualizzazioni diverse. Lo stile della finestra del controllo specifica la visualizzazione predefinita. Gli stili aggiuntivi della finestra specificano l'allineamento degli elementi e delle funzionalità specifiche del controllo. Nella tabella seguente vengono descritte le visualizzazioni.



| Nome della visualizzazione             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Visualizzazione icone             | Specificato dallo stile della finestra dell' [**\_ icona LVS**](list-view-window-styles.md) o passando **l' \_ \_ icona di visualizzazione LV** con il messaggio di [**\_ visualizzazione LVM**](lvm-setview.md) . Ogni elemento viene visualizzato come icona a dimensione intera con un'etichetta sotto di essa. L'utente può trascinare gli elementi in qualsiasi posizione nella finestra elenco-visualizzazione.                                                                                                                                                                                                                                         |
| Visualizzazione icona piccola       | Specificato dallo stile della finestra [**\_ SMALLICON di LVS**](list-view-window-styles.md) o passando **la \_ vista LV \_ SMALLICON** con la [**\_ vista LVM**](lvm-setview.md). Ogni elemento viene visualizzato come piccola icona con l'etichetta a destra. L'utente può trascinare gli elementi in qualsiasi posizione.                                                                                                                                                                                                                                                       |
| Visualizzazione elenco             | Specificata dallo stile della finestra [**\_ elenco LVS**](list-view-window-styles.md) o passando l' **\_ \_ elenco di visualizzazioni LV** con la [**\_ visualizzazione LVM**](lvm-setview.md). Ogni elemento viene visualizzato come icona piccola con un'etichetta a destra. Gli elementi sono disposti in colonne e l'utente non può trascinarli in una posizione arbitraria.                                                                                                                                                                                                                               |
| Visualizzazione report (Dettagli) | Specificata dallo stile della finestra del [**\_ report LVS**](list-view-window-styles.md) o passando **\_ \_ i dettagli della visualizzazione LV** con la [**\_ visualizzazione LVM**](lvm-setview.md). Ogni elemento viene visualizzato in una riga a se stante, con le informazioni disposte in colonne. La colonna più a sinistra viene sempre giustificata e contiene l'icona e l'etichetta di piccole dimensioni. Le colonne successive contengono elementi secondari specificati dall'applicazione. Ogni colonna ha un'intestazione, a meno che non si specifichi anche lo stile della finestra [**\_ nocolumnheader LVS**](list-view-window-styles.md) . |
| Visualizzazione affiancata             | **Versione 6 e successive.** Specificata passando il **\_ \_ riquadro di visualizzazione LV** con la [**\_ visualizzazione LVM**](lvm-setview.md). Ogni elemento viene visualizzato come icona a dimensione intera con un'etichetta di una o più righe accanto.                                                                                                                                                                                                                                                                                                                                                        |



 

Le schermate seguenti usano le visualizzazioni per visualizzare quantità diverse di informazioni su ognuno dei sette animali domestici. Le visualizzazioni dimostrano come potrebbero essere visualizzate le informazioni in Windows Vista. Gli stili di visualizzazione per il controllo sono stati impostati sul tema "Explorer" tramite [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).

Lo screenshot seguente mostra la visualizzazione dettagli.

![screenshot che mostra le informazioni in cinque colonne e sette righe](images/lv-detailsview.png)

Lo screenshot seguente mostra la visualizzazione icona.

![screenshot che mostra solo il nome di ogni animale e un'icona che indica la specie](images/lv-iconview.png)

Lo screenshot seguente mostra la visualizzazione elenco.

![screenshot che mostra, per ogni animale domestico, un'icona grande accanto al testo del nome, della razza e del prezzo dell'animale.](images/lv-listview.png)

Lo screenshot seguente mostra la visualizzazione affiancata.

![visualizzazione affiancata.](images/lv-tileview.png)

È possibile modificare il tipo di visualizzazione dopo aver creato un controllo visualizzazione elenco. Per recuperare e modificare lo stile della finestra, usare le funzioni [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) . Per determinare gli stili della finestra corrente, usare il valore [**\_ TYPEMASK di LVS**](list-view-window-styles.md) .

È possibile controllare il modo in cui gli elementi sono disposti nell'icona o nella visualizzazione icona piccola specificando lo stile della finestra [**LVS \_ ALIGNTOP**](list-view-window-styles.md) (impostazione predefinita) o [**LVS \_ ALIGNLEFT**](list-view-window-styles.md) .

È possibile modificare l'allineamento dopo aver creato un controllo visualizzazione elenco. Per determinare l'allineamento corrente, usare il [**valore \_ ALIGNMASK di LVS**](list-view-window-styles.md) .

Gli stili aggiuntivi della finestra forniscono altre opzioni, ad esempio se un utente può modificare le etichette o selezionare più di un elemento alla volta. Per un elenco completo, vedere [stili della finestra visualizzazione elenco](list-view-window-styles.md).

### <a name="extended-list-view-styles"></a>Stili List-View estesi

Gli stili del controllo visualizzazione elenco esteso forniscono opzioni quali caselle di controllo, barre di scorrimento Flat, linee griglia e rilevamento a caldo. Per un elenco completo, vedere [stili di List-View estese](extended-list-view-styles.md). Non è possibile accedere agli stili estesi di visualizzazione elenco nello stesso modo degli stili di finestra standard. Non vengono utilizzate le funzioni [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per apportare modifiche di stile estese.

Sono disponibili due messaggi che impostano e recuperano informazioni di stile estese, [**LVM \_ SETEXTENDEDLISTVIEWSTYLE**](lvm-setextendedlistviewstyle.md) e [**LVM \_ GETEXTENDEDLISTVIEWSTYLE**](lvm-getextendedlistviewstyle.md). Anziché inviare i messaggi in modo esplicito, è possibile usare le macro corrispondenti seguenti: [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle), [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)e [**ListView \_ GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle).

## <a name="virtual-list-view-style"></a>Stile List-View virtuale

Una visualizzazione elenco virtuale è un controllo di visualizzazione elenco con lo stile [**\_ OWNERDATA di LVS**](list-view-window-styles.md) . Questo stile consente al controllo di gestire milioni di elementi, perché il proprietario riceve il carico di gestione dei dati dell'elemento. In questo modo è possibile usare il controllo elenco virtuale con database di grandi dimensioni, in cui sono già disponibili metodi specifici per l'accesso ai dati.

Un controllo di visualizzazione elenco virtuale mantiene le informazioni relative all'elemento stesso. Ad eccezione delle informazioni sulla selezione e lo stato attivo, il proprietario del controllo deve gestire tutte le informazioni sugli elementi. Altri elaborano le informazioni sull'elemento richiesta dal proprietario usando i codici di notifica di [LVN \_ GETDISPINFO](lvn-getdispinfo.md) .

Poiché questo tipo di controllo elenco è destinato a set di dati di grandi dimensioni, è consigliabile memorizzare nella cache i dati degli elementi richiesti per migliorare le prestazioni del recupero. La visualizzazione elenco fornisce un meccanismo di hint per la cache che facilita l'ottimizzazione della cache. L'hint viene implementato sotto forma di codice di [notifica \_ ODCACHEHINT LVN](lvn-odcachehint.md) .

### <a name="creating-a-virtual-list-view-control"></a>Creazione di un controllo List-View virtuale

È possibile creare controlli di visualizzazione elenco virtuali usando la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando lo stile della finestra [**LVS \_ OWNERDATA**](list-view-window-styles.md) come parte del parametro della funzione *dwStyle* . Il cambio dinamico da e verso lo **stile \_ OWNERDATA di LVS** non è supportato.

È possibile usare lo [**stile \_ OWNERDATA di LVS**](list-view-window-styles.md) in combinazione con la maggior parte degli stili della finestra, ad eccezione dello stile [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) . Tutti i controlli elenco virtuale visualizzano per impostazione predefinita lo stile [**LVS \_ AutoArrange**](list-view-window-styles.md) .

Per consentire la visualizzazione degli elementi nell'elenco, è necessario prima inviare il messaggio [**LVM \_ SETITEMCOUNT**](lvm-setitemcount.md) , in modo esplicito o tramite la macro [**\_ SetItemCountEx di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) .

I messaggi seguenti non sono supportati con lo [**stile \_ OWNERDATA di LVS**](list-view-window-styles.md) : [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md), [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md), [**LVM \_ SETTILEINFO**](lvm-settileinfo.md)e [**LVM \_ MAPIDTOINDEX**](lvm-mapidtoindex.md).

### <a name="compatibility-issues"></a>Problemi di compatibilità

Tutti e quattro gli stili di visualizzazione elenco (icona, piccola icona, elenco e visualizzazione report) supportano lo stile [**\_ OWNERDATA LVS**](list-view-window-styles.md) . I controlli di visualizzazione elenco con stile **\_ OWNERDATA LVS** non archiviano informazioni specifiche dell'elemento. Pertanto, gli unici flag di stato degli elementi validi che è possibile applicare a un elemento sono [**lvis \_ selezionati**](list-view-item-states.md) e [**lvis sono \_ incentrati**](list-view-item-states.md). Nessun'altra informazione sullo stato è archiviata. In particolare, il controllo elenco-visualizzazione non mantiene le immagini di stato o sovrapposizione per ogni elemento. Tuttavia, è possibile fare in modo che il controllo elenco-visualizzazione query l'applicazione per queste immagini inviando un messaggio [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) .

La maggior parte dei messaggi di controllo visualizzazione elenco e le macro associate sono completamente supportati. Tuttavia, alcuni messaggi presentano limitazioni o non sono supportati quando si usa lo stile [**\_ OWNERDATA di LVS**](list-view-window-styles.md) . Nella tabella seguente vengono riepilogati i messaggi interessati.



| Message                                             | Limitazione                                                                                                                                                                                                                                                      |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_disposizione LVM**](lvm-arrange.md)                 | Non supporta lo stile **\_ SNAPTOGRID LVA** .                                                                                                                                                                                                                 |
| [**\_DELETEALLITEMS LVM**](lvm-deleteallitems.md)   | Imposta il numero di elementi su zero e cancella tutte le variabili di selezione interne, ma non elimina effettivamente alcun elemento. Esegue un callback di notifica.                                                                                                           |
| [**\_DeleteItem LVM**](lvm-deleteitem.md)           | È supportato solo per l'integrità della selezione e non elimina effettivamente un elemento.                                                                                                                                                                                 |
| [**\_GETITEMSTATE LVM**](lvm-getitemstate.md)       | Restituisce solo gli Stati di attivazione e selezione, ovvero gli stati archiviati dal controllo visualizzazione elenco.                                                                                                                                                                |
| [**\_GETNEXTITEM LVM**](lvm-getnextitem.md)         | Non supporta i criteri di ricerca di visualizzazione elenco **LVNI \_ Cut**, **LVNI \_ Hidden** o **LVNI \_ DROPHILITED**. Sono supportati tutti gli altri criteri.                                                                                                                     |
| [**\_GETWORKAREAS LVM**](lvm-getworkareas.md)       | Non è supportata.                                                                                                                                                                                                                                               |
| [**INSERTITEM (LVM) \_**](lvm-insertitem.md)           | È supportato solo per l'integrità della selezione.                                                                                                                                                                                                                      |
| [**ELEMENTO per LVM \_**](lvm-setitem.md)                 | Non è supportata. Per impostare lo stato dell'elemento, utilizzare il messaggio [**ListView \_ SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) .                                                                                                                                               |
| [**\_SETITEMCOUNT LVM**](lvm-setitemcount.md)       | Imposta il numero di elementi attualmente presenti nell'elenco. Se il controllo elenco-visualizzazione Invia una notifica che richiede dati per qualsiasi elemento fino al set massimo, il proprietario deve essere pronto a fornire tali dati. I parametri del messaggio supportano i controlli visualizzazione elenco virtuale. |
| [**\_SETITEMPOSITION LVM**](lvm-setitemposition.md) | Non è supportata.                                                                                                                                                                                                                                               |
| [**\_SETITEMSTATE LVM**](lvm-setitemstate.md)       | Consente di modificare solo gli Stati di selezione e di stato attivo per l'elemento.                                                                                                                                                                                          |
| [**\_SETITEMTEXT LVM**](lvm-setitemtext.md)         | Non è supportata. È responsabilità dell'applicazione gestire i testi degli articoli.                                                                                                                                                                            |
| [**\_SETWORKAREAS LVM**](lvm-setworkareas.md)       | Non è supportata.                                                                                                                                                                                                                                               |
| [**\_SORTITEMS LVM**](lvm-sortitems.md)             | Non è supportata. È responsabilità dell'applicazione presentare gli elementi nell'ordine desiderato.                                                                                                                                                             |



 

### <a name="handling-virtual-list-view-control-notification-codes"></a>Gestione dei codici di notifica del controllo List-View virtuale

I controlli List-View con lo stile [**LVS \_ OWNERDATA**](list-view-window-styles.md) inviano gli stessi codici di notifica degli altri controlli visualizzazione elenco e altri due: [LVN \_ ODCACHEHINT](lvn-odcachehint.md) e [LVN \_ ODFINDITEM](lvn-odfinditem.md). Di seguito sono riportate le notifiche più comuni inviate dal controllo elenco-visualizzazione con lo stile **\_ OWNERDATA di LVS** .



|                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_GETDISPINFO LVN](lvn-getdispinfo.md) | Un controllo di visualizzazione elenco virtuale mantiene autonomamente le informazioni sugli elementi. Di conseguenza, invia spesso il codice di notifica [LVN \_ GETDISPINFO](lvn-getdispinfo.md) per richiedere informazioni sugli elementi. Questo messaggio viene gestito in modo analogo agli elementi di callback in un controllo elenco standard. Poiché il numero di elementi supportati dal controllo può essere molto elevato, la memorizzazione nella cache dei dati degli elementi migliora le prestazioni. Quando si gestisce LVN \_ GETDISPINFO, il proprietario del controllo tenta innanzitutto di fornire le informazioni sull'elemento richieste dalla cache. per ulteriori informazioni, vedere la pagina relativa alla [gestione della cache](#cache-management). Se l'elemento richiesto non è memorizzato nella cache, il proprietario deve essere preparato per fornire le informazioni in altro modo. |
| [\_ODCACHEHINT LVN](lvn-odcachehint.md) | Una visualizzazione elenco virtuale invia il codice di notifica [LVN \_ ODCACHEHINT](lvn-odcachehint.md) per semplificare l'ottimizzazione della cache. Il codice di notifica fornisce valori di indice inclusivi per un intervallo di elementi che è consigliabile memorizzare nella cache. Al momento della ricezione del codice di notifica, il proprietario deve essere pronto a caricare la cache con le informazioni sugli elementi per l'intervallo richiesto, in modo che le informazioni saranno immediatamente disponibili quando viene inviato un messaggio [LVN \_ GETDISPINFO](lvn-getdispinfo.md) .                                                                                                                                                                                                                                   |
| [\_ODFINDITEM LVN](lvn-odfinditem.md)   | Il codice di notifica [ \_ ODFINDITEM di LVN](lvn-odfinditem.md) viene inviato da un controllo di visualizzazione elenco virtuale quando il controllo richiede al proprietario di trovare un particolare elemento di callback. Il codice di notifica viene inviato quando il controllo elenco-visualizzazione riceve l'accesso rapido alla chiave o quando riceve un messaggio [**\_ FINDITEM LVM**](lvm-finditem.md) . Le informazioni di ricerca vengono inviate sotto forma di una struttura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , che è un membro della struttura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) . Il proprietario deve essere pronto a cercare un elemento che corrisponda alle informazioni fornite dal controllo visualizzazione elenco. Il proprietario restituisce l'indice dell'elemento in caso di esito positivo, oppure-1 se non viene trovato alcun elemento corrispondente.               |



 

### <a name="cache-management"></a>Gestione della cache

Un controllo di visualizzazione elenco con lo stile [**LVS \_ OWNERDATA**](list-view-window-styles.md) genera un numero elevato di codici di notifica [LVN \_ GETDISPINFO](lvn-getdispinfo.md) e, per semplificare l'ottimizzazione della cache, un messaggio [LVN \_ ODCACHEHINT](lvn-odcachehint.md) . \_I messaggi LVN ODCACHEHINT forniscono informazioni sugli elementi consigliati da includere nella cache. Questi messaggi vengono inviati come messaggi di [**\_ notifica WM**](wm-notify.md) , con il valore *lParam* che funge da indirizzo di una struttura [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) .

La struttura [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) include due membri integer, **iFrom** e **Ito**, che rappresentano gli endpoint inclusivi di un intervallo di elementi che probabilmente saranno necessari. Il proprietario deve essere pronto a caricare la cache con le informazioni sull'elemento per ognuno degli elementi compresi nell'intervallo consigliato.

Il controllo elenco spesso richiede informazioni sugli elementi per il primo elemento (offset 0). Il codice di notifica [ \_ ODCACHEHINT di LVN](lvn-odcachehint.md) potrebbe non sempre includere l'elemento 0, ma deve sempre essere incluso nella cache.

Si accede spesso agli ultimi elementi dell'elenco. Il proprietario potrebbe pertanto voler contenere una seconda cache che includa gli elementi alla fine dell'elenco. L'intervallo richiesto da [LVN \_ ODCACHEHINT](lvn-odcachehint.md) può essere controllato rispetto alla cache finale per renderlo disponibile automaticamente anziché ricaricare ogni volta lo stesso intervallo di fine.

## <a name="list-view-working-areas"></a>Aree di lavoro List-View

I controlli elenco-visualizzazione supportano le aree di lavoro, che sono aree virtuali rettangolari utilizzate dal controllo elenco-visualizzazione per disporre gli elementi. Un'area di lavoro non è una finestra e non può avere un bordo visibile. Per impostazione predefinita, il controllo elenco-visualizzazione non contiene aree di lavoro. Creando un'area di lavoro, è possibile creare un bordo vuoto a sinistra, in alto o a destra degli elementi o causare la visualizzazione di una barra di scorrimento orizzontale quando normalmente non ne esiste una.

Quando viene creata un'area di lavoro, gli elementi che si trovano all'interno dell'area di lavoro diventano membri dell'area di lavoro. Analogamente, se un elemento viene spostato in un'area di lavoro, l'elemento diventa un membro dell'area di lavoro. Se un elemento non si trova all'interno di un'area di lavoro, diventa automaticamente membro della prima area di lavoro (indice 0). Per inserire un nuovo elemento in un'area di lavoro specifica, è innanzitutto necessario creare l'elemento e quindi usare il messaggio [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) o [**LVM \_ SETITEMPOSITION32**](lvm-setitemposition32.md) per spostarlo nell'area di lavoro desiderata.

L'illustrazione seguente è un esempio di controllo visualizzazione elenco che contiene quattro aree di lavoro, ognuna in un quadrante diverso dell'area client.

![Screenshot di un controllo visualizzazione elenco con un'area di lavoro in ogni quadrante dell'area client](images/working.jpg)

È possibile usare più aree di lavoro per creare aree diverse all'interno di una sola visualizzazione. È possibile creare aree in una singola visualizzazione con significati diversi. Ad esempio, una vista di un file system potrebbe avere un'area per i file di lettura/scrittura e un'altra area per i file di sola lettura. L'utente può categorizzare gli elementi inserendoli in aree di lavoro diverse. Se un file viene spostato nell'area di sola lettura, verrà automaticamente reso di sola lettura.

È possibile intersecare più aree di lavoro, ma tutti gli elementi che si trovano all'interno dell'intersezione diventano membri dell'area con l'indice inferiore; Pertanto, è preferibile evitare questa situazione. Quando si ordinano più aree di lavoro, gli elementi vengono ordinati rispetto agli altri elementi nella stessa area di lavoro.

Il numero di aree di lavoro può essere recuperato con il messaggio [**LVM \_ GETNUMBEROFWORKAREAS**](lvm-getnumberofworkareas.md) . Le aree di lavoro vengono modificate con il messaggio [**LVM \_ SETWORKAREAS**](lvm-setworkareas.md) e possono essere recuperate con il messaggio [**LVM \_ GETWORKAREAS**](lvm-getworkareas.md) . Entrambi questi messaggi accettano l'indirizzo di una matrice di strutture [**Rect**](/previous-versions//dd162897(v=vs.85)) come *lParam* e il numero di strutture **Rect** come *wParam*. I membri **sinistro** e **superiore** di queste strutture specificano le coordinate dell'angolo superiore sinistro (l'origine) dell'area di lavoro e i membri **destro** e **inferiore** specificano l'angolo inferiore destro dell'area di lavoro. Tutte le coordinate si trovano nelle coordinate client della visualizzazione elenco. Il numero massimo di aree di lavoro consentito è definito dal valore **LV \_ Max \_ WORKAREAS** .

La modifica dell'area di lavoro non ha alcun effetto sui controlli visualizzazione elenco che includono l' [**\_ elenco LVS**](list-view-window-styles.md) o la visualizzazione [**\_ report LVS**](list-view-window-styles.md) , ma le aree di lavoro verranno mantenute quando viene modificato il tipo di visualizzazione. Con l' [**\_ icona LVS**](list-view-window-styles.md) e le visualizzazioni [**\_ SMALLICON di LVS**](list-view-window-styles.md) , l'area di lavoro può essere modificata per modificare la modalità di visualizzazione degli elementi. Se si imposta la larghezza dell'area di lavoro (destra-sinistra) maggiore della larghezza del client del controllo, viene eseguito il wrapper degli elementi a tale larghezza e la barra di scorrimento orizzontale da visualizzare. Se la larghezza dell'area di lavoro è più stretta rispetto alla larghezza dell'area client del controllo, gli elementi vengono racchiusi nell'area di lavoro e non nell'area client. Impostando il membro **sinistro** o **superiore** su un valore positivo, gli elementi vengono visualizzati a partire dall'area di lavoro, creando uno spazio vuoto tra il bordo del controllo e gli elementi. È anche possibile creare uno spazio vuoto tra il bordo destro del controllo e gli elementi, rendendo la larghezza dell'area di lavoro minore della larghezza del client del controllo.

## <a name="list-view-image-lists"></a>Elenchi di immagini List-View

Per impostazione predefinita, un controllo di visualizzazione elenco non Visualizza le immagini dell'elemento. Per visualizzare le immagini degli elementi, è necessario creare elenchi di immagini e associarli al controllo. Un controllo visualizzazione elenco può avere tre elenchi di immagini:

-   Elenco di immagini che contiene le icone a dimensione intera visualizzate quando il controllo è in visualizzazione icone.
-   Elenco di immagini che contiene icone piccole visualizzate quando il controllo è in visualizzazione icona piccola, visualizzazione elenco o visualizzazione report.
-   Elenco di immagini che contiene le immagini di stato, che vengono visualizzate a sinistra dell'icona a dimensione intera o piccola. È possibile utilizzare immagini di stato, ad esempio caselle di controllo selezionate e deselezionate, per indicare gli Stati degli elementi definiti dall'applicazione. Le immagini di stato vengono visualizzate in visualizzazione icone, visualizzazione icone piccole, visualizzazione elenco e visualizzazione report.

Gli elenchi di immagini icona di dimensioni ridotte e di dimensioni ridotte possono contenere anche *immagini sovrapposte*, progettate per essere disegnate in modo trasparente sulle icone degli elementi.

Per usare le immagini sovrapposte in un controllo visualizzazione elenco:

1.  Chiamare la funzione [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) per assegnare un indice di immagine sovrapposta a un'immagine negli elenchi di immagini con dimensioni ridotte e di dimensioni ridotte. Un'immagine sovrapposta è identificata da un indice in base uno.
2.  È possibile associare un indice di immagine sovrapposta a un elemento quando si chiama la macro [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) o [**ListView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) . Usare la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) per specificare un indice di immagine sovrapposto nel membro di **stato** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dell'elemento. È anche necessario impostare i bit [**lvis \_ OVERLAYMASK**](list-view-item-states.md) nel membro **stateMask** .

Se viene specificato un elenco di immagini di stato, un controllo visualizzazione elenco riserva spazio a sinistra dell'icona di ogni elemento per un'immagine di stato.

Per associare un'immagine di stato a un elemento, usare la macro [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) per specificare un indice dell'immagine di stato nel membro di **stato** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . L'indice identifica un'immagine nell'elenco di immagini dello stato del controllo. Anche se gli indici dell'elenco immagini sono in base zero, il controllo Usa indici basati su uno per identificare le immagini di stato. Un indice immagine di stato zero indica che un elemento non ha un'immagine di stato.

Per impostazione predefinita, quando un controllo visualizzazione elenco viene eliminato definitivamente, Elimina gli elenchi di immagini assegnati. Tuttavia, se un controllo di visualizzazione elenco dispone dello stile della finestra [**LVS \_ SHAREIMAGELISTS**](list-view-window-styles.md) , l'applicazione è responsabile dell'eliminazione degli elenchi di immagini quando non sono più in uso. È necessario specificare questo stile se si assegnano gli stessi elenchi di immagini a più controlli visualizzazione elenco; in caso contrario, più controlli potrebbero tentare di eliminare definitivamente lo stesso elenco di immagini.

## <a name="list-view-items-and-subitems"></a>List-View elementi e elementi secondari

Ogni elemento in un controllo di visualizzazione elenco ha un'icona, un'etichetta, uno stato corrente e un valore definito dall'applicazione. Utilizzando i messaggi di visualizzazione elenco, è possibile aggiungere, modificare ed eliminare elementi, nonché recuperare informazioni sugli elementi.

Ogni elemento può avere uno o più *elementi secondari*. Un elemento secondario è una stringa che, in visualizzazione report, viene visualizzata in una colonna distinta dall'icona e dall'etichetta dell'elemento. Per specificare il testo di un elemento secondario, usare il messaggio [**LVM \_ SETITEMTEXT**](lvm-setitemtext.md) o [**LVM \_**](lvm-setitem.md) . Tutti gli elementi di un controllo visualizzazione elenco presentano lo stesso numero di elementi secondari. Il numero di elementi secondari è determinato dal numero di colonne nel controllo elenco-visualizzazione. Quando si aggiunge una colonna a un controllo visualizzazione elenco, si specifica l'indice dell'elemento secondario associato.

La struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) definisce un elemento di visualizzazione elenco o un elemento secondario. Il membro **iItem** è l'indice in base zero dell'elemento. Il membro **iSubItem** è l'indice in base uno di un elemento secondario o zero se la struttura contiene informazioni su un elemento. I membri aggiuntivi specificano il testo, l'icona, lo stato e i dati dell'elemento. *I dati dell'elemento* sono un valore definito dall'applicazione associato a un elemento della visualizzazione elenco.

Per aggiungere un elemento a un controllo di visualizzazione elenco, usare il messaggio [**LVM \_ INSERTITEM**](lvm-insertitem.md) , specificando l'indirizzo di una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Prima di aggiungere più elementi, è possibile inviare al controllo un messaggio [**LVM \_ SETITEMCOUNT**](lvm-setitemcount.md) , specificando il numero di elementi che il controllo conterrà infine. Questo messaggio consente al controllo di visualizzazione elenco di riallocare le strutture di dati interne solo una volta anziché ogni volta che si aggiunge un elemento. È possibile determinare il numero di elementi in un controllo visualizzazione elenco usando il messaggio [**LVM \_ GETITEMCOUNT**](lvm-getitemcount.md) . Se si aggiunge un numero elevato di elementi a un controllo visualizzazione elenco, è possibile velocizzare il processo disabilitando il ridisegno prima di aggiungere gli elementi, quindi abilitare il ridisegno dopo l'aggiunta degli elementi. Usare il messaggio [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw) per abilitare e disabilitare il ridisegno.

Per modificare gli attributi di un elemento della visualizzazione elenco, usare il messaggio [**LVM \_ SetItem**](lvm-setitem.md) , specificando l'indirizzo di una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Il membro **mask** della struttura specifica gli attributi dell'elemento che si desidera modificare. Ad esempio, per modificare solo il testo di un elemento o di un elemento secondario, usare il messaggio [**LVM \_ SETITEMTEXT**](lvm-setitemtext.md) .

Per recuperare informazioni su un elemento della visualizzazione elenco, usare il messaggio [**LVM \_ GetItem**](lvm-getitem.md) , specificando l'indirizzo della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) da compilare. Il membro **mask** della struttura specifica gli attributi dell'elemento da recuperare. Per recuperare solo il testo di un elemento o di un elemento secondario, usare il messaggio [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md) .

Per eliminare un elemento della visualizzazione elenco, usare il messaggio [**LVM \_ DeleteItem**](lvm-deleteitem.md) . È possibile eliminare tutti gli elementi di un controllo di visualizzazione elenco usando il messaggio [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) .

### <a name="list-view-item-states"></a>Stati elemento List-View

Lo stato di un elemento è un valore che specifica la disponibilità dell'elemento, indica le azioni dell'utente o in caso contrario riflette lo stato dell'elemento. Un controllo visualizzazione elenco modifica alcuni bit di stato, ad esempio quando l'utente seleziona un elemento. Un'applicazione potrebbe modificare altri bit di stato per disabilitare o nascondere l'elemento o per specificare un'immagine sovrapposta o un'immagine di stato. Per ulteriori informazioni sulle immagini sovrapposte e le immagini di stato, vedere elenchi di immagini di [visualizzazione elenco](#list-view-image-lists).

Lo stato di un elemento è specificato dal membro di **stato** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Quando si specifica o si modifica lo stato di un elemento, il membro **stateMask** specifica quali bit di stato è necessario modificare. È possibile modificare lo stato di un elemento usando il messaggio [**LVM \_ SETITEMSTATE**](lvm-setitemstate.md) . È possibile specificare lo stato di un elemento quando lo si crea o quando si modificano gli attributi usando [**il \_ messaggio LVM**](lvm-setitem.md) . Per determinare lo stato corrente di un elemento, usare il messaggio [**LVM \_ GETITEMSTATE**](lvm-getitemstate.md) o [**LVM \_ GetItem**](lvm-getitem.md) .

Per impostare l'immagine sovrapposta di un elemento, il membro **stateMask** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deve includere il valore [**\_ OVERLAYMASK di lvis**](list-view-item-states.md) e il membro **state** deve includere l'indice in base uno dell'immagine sovrapposta spostata a 8 bit a sinistra utilizzando la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) . L'indice può essere zero per specificare Nessuna immagine sovrapposta.

Per impostare l'immagine di stato di un elemento, il membro **stateMask** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deve includere il valore [**\_ STATEIMAGEMASK di lvis**](list-view-item-states.md) e il membro di **stato** deve includere l'indice in base uno dell'immagine dello stato spostato a sinistra di 12 bit utilizzando la macro [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) . L'indice può essere zero per specificare un'immagine di stato.

### <a name="callback-items-and-the-callback-mask"></a>Elementi di callback e maschera di callback

Per ogni elemento, un controllo visualizzazione elenco in genere archivia il testo dell'etichetta, l'indice dell'elenco di immagini delle icone dell'elemento e un set di flag di bit per lo stato dell'elemento. È possibile definire elementi di callback o modificare la maschera di callback del controllo per indicare che l'applicazione, anziché il controllo, archivia alcune o tutte queste informazioni. È possibile usare i callback se l'applicazione archivia alcune di queste informazioni.

Un *elemento di callback* in un controllo visualizzazione elenco è un elemento per il quale l'applicazione archivia il testo o l'indice dell'icona o entrambi. È possibile definire gli elementi di callback quando si invia il messaggio [**\_ INSERTITEM INSERTITEM**](lvm-insertitem.md) per aggiungere un elemento al controllo List-View. Se l'applicazione archivia il testo per l'elemento o l'elemento secondario, impostare il membro **pszText** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dell'elemento su **LPSTR \_ TEXTCALLBACK**. Se l'applicazione archivia l'indice dell'icona per un elemento, impostare il membro **IImage** della struttura **LVITEM** dell'elemento su **\_ IMAGECALLBACK**.

La *maschera di callback* di un controllo visualizzazione elenco è un set di flag di bit che specificano gli Stati degli elementi per i quali l'applicazione, anziché il controllo, archivia i dati correnti. La maschera di callback viene applicata a tutti gli elementi del controllo, a differenza della designazione dell'elemento di callback che si applica a un elemento specifico. Per impostazione predefinita, la maschera di callback è zero, il che significa che il controllo elenco-visualizzazione archivia tutte le informazioni sullo stato dell'elemento. Dopo aver creato un controllo visualizzazione elenco e aver inizializzato gli elementi, è possibile inviare il messaggio [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) per modificare la maschera di callback. Per recuperare la maschera di callback corrente, inviare il messaggio [**LVM \_ GETCALLBACKMASK**](lvm-getcallbackmask.md) .

Quando un controllo visualizzazione elenco deve visualizzare o ordinare un elemento della visualizzazione elenco per il quale l'applicazione archivia le informazioni di callback, il controllo Invia il codice di notifica [LVN \_ GETDISPINFO](lvn-getdispinfo.md) alla finestra padre del controllo. Questo messaggio specifica una struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) che contiene il tipo di informazioni richieste e identifica l'elemento o l'elemento secondario da recuperare. La finestra padre deve elaborare LVN \_ GETDISPINFO per fornire i dati richiesti.

Se il controllo elenco-visualizzazione rileva una modifica nelle informazioni di callback di un elemento, ad esempio una modifica delle informazioni sul testo, sull'icona o sullo stato, il controllo Invia un codice di notifica [LVN \_ SETDISPINFO](lvn-setdispinfo.md) per notificare la modifica.

Se si modificano gli attributi o i bit di stato di un elemento di callback, si usa il messaggio di [**\_ aggiornamento LVM**](lvm-update.md) per forzare il controllo a ridisegnare l'elemento. Questo messaggio fa anche in modo che il controllo organizzi gli elementi se dispone dello stile di [**\_ disdisposizione LVS**](list-view-window-styles.md) . È possibile usare il messaggio [**LVM \_ REDRAWITEMS**](lvm-redrawitems.md) per ricreare un intervallo di elementi invalidando le parti corrispondenti dell'area client del controllo visualizzazione elenco.

Utilizzando in modo efficace gli elementi di callback e la maschera di callback, è possibile assicurarsi che ogni attributo dell'elemento venga mantenuto in una sola posizione. Questa operazione può semplificare l'applicazione, ma l'unico spazio salvato è la memoria che altrimenti sarebbe necessaria per archiviare le etichette degli elementi e il testo dell'elemento secondario.

### <a name="list-view-item-position"></a>Posizione dell'elemento List-View

Ogni elemento della visualizzazione elenco ha una posizione e una dimensione che è possibile recuperare e impostare usando i messaggi. È anche possibile determinare quale elemento, se presente, si trova in una posizione specificata. La posizione degli elementi della visualizzazione elenco è specificata nelle *coordinate della visualizzazione*, ovvero le coordinate client vengono sfalsate in base alla posizione di scorrimento.

Per recuperare e impostare la posizione di un elemento, usare i messaggi [**LVM \_ GETITEMPOSITION**](lvm-getitemposition.md) e [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) . **LVM \_ GETITEMPOSITION** funziona per tutte le visualizzazioni, ma **LVM \_ SETITEMPOSITION** funziona solo per icone e icone piccole.

È possibile determinare quale elemento, se presente, si trova in una determinata posizione usando il messaggio di [**LVM \_ HITTEST**](lvm-hittest.md) .

Per recuperare il rettangolo di delimitazione per una voce di elenco o solo per la relativa icona o etichetta, usare il messaggio [**LVM \_ GETITEMRECT**](lvm-getitemrect.md) .

### <a name="arranging-sorting-and-finding-items"></a>Disposizione, ordinamento e ricerca di elementi

È possibile usare i messaggi di visualizzazione elenco per disporre e ordinare gli elementi e per trovare gli elementi in base ai relativi attributi o posizioni. Disposizione degli elementi di riposizionamento da allineare in una griglia, ma gli indici degli elementi non cambiano. L'ordinamento modifica la sequenza di elementi (e gli indici corrispondenti), quindi li riposiziona di conseguenza. È possibile disporre gli elementi solo nelle visualizzazioni icona e icone piccole, ma è possibile ordinare gli elementi in qualsiasi visualizzazione. Per trovare gli elementi, è possibile inviare messaggi di visualizzazione elenco che specificano una proprietà o un percorso di elemento.

Per disporre gli elementi, usare il messaggio di [**\_ disposizione LVM**](lvm-arrange.md) . È possibile verificare che gli elementi siano disposti sempre specificando lo stile della finestra [**LVS \_ AutoArrange**](list-view-window-styles.md) .

Per ordinare gli elementi, usare il messaggio [**LVM \_ SORTITEMS**](lvm-sortitems.md) . Quando si esegue l'ordinamento usando questo messaggio, si specifica una funzione di callback definita dall'applicazione che il controllo di visualizzazione elenco chiama per confrontare l'ordine relativo di due elementi. Il controllo passa alla funzione di confronto i dati dell'elemento associati a ognuno dei due elementi. I dati dell'elemento corrispondono al valore specificato nel membro **lParam** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dell'elemento quando è stato inserito nell'elenco. Specificando i dati dell'elemento appropriati e fornendo una funzione di confronto appropriata, è possibile ordinare gli elementi in base all'etichetta, a qualsiasi elemento secondario o a qualsiasi altra proprietà. Si noti che gli elementi di ordinamento non riordinano gli elementi secondari corrispondenti. Quando gli elementi vengono riordinati, gli elementi secondari corrispondenti vengono trasportati con loro. ovvero intere righe vengono mantenute insieme. Per ordinare separatamente le colonne, scollegando gli elementi secondari dagli elementi, è necessario rigenerare le colonne dopo aver eseguito l'ordinamento utilizzando l' [**\_ elemento LVM**](lvm-setitem.md).

È possibile assicurarsi che un controllo visualizzazione elenco venga sempre ordinato specificando lo stile della finestra [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) . I controlli con questi stili utilizzano il testo dell'etichetta degli elementi per ordinarli in ordine crescente o decrescente. Non è possibile fornire una funzione di confronto quando si usano questi stili di finestra. Se un controllo visualizzazione elenco ha uno di questi stili, un messaggio [**\_ INSERTITEM INSERTITEM**](lvm-insertitem.md) non riuscirà se si tenta di inserire un elemento con **LPSTR \_ TEXTCALLBACK** come membro **pszText** della relativa struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

È possibile trovare un elemento della visualizzazione elenco con proprietà specifiche usando il messaggio [**LVM \_ FINDITEM**](lvm-finditem.md) . È possibile trovare un elemento della visualizzazione elenco che si trova in uno stato specificato e ha una relazione specificata con un determinato elemento usando il messaggio [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) . Ad esempio, è possibile recuperare il successivo elemento selezionato a destra di un elemento specificato.

## <a name="list-view-columns"></a>Colonne List-View

Le colonne controllano il modo in cui gli elementi e i relativi elementi secondari vengono visualizzati in visualizzazione report. Ogni colonna ha un titolo e una larghezza ed è associata a un elemento secondario specifico; l'elemento secondario zero è l'icona e l'etichetta dell'elemento. Gli attributi di una colonna sono definiti da una struttura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) .

Per aggiungere una colonna a un controllo visualizzazione elenco, usare il messaggio [**LVM \_ INSERTCOLUMN**](lvm-insertcolumn.md) . Per eliminare una colonna, usare il messaggio [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) .

> [!Note]  
> L'eliminazione della colonna zero di un controllo visualizzazione elenco è supportata solo in ComCtl32.dll versione 6 e successive. La versione 5 supporta anche l'eliminazione della colonna zero, ma solo dopo l'uso di [**CCM \_ Subversion**](ccm-setversion.md) per impostare la versione su 5 o versioni successive. Le versioni precedenti alla 5 non supportano l'eliminazione della colonna zero.

 

È possibile recuperare e modificare le proprietà di una colonna esistente usando i messaggi [**LVM \_ GetColumn**](lvm-getcolumn.md) e [**LVM \_ secolumn**](lvm-setcolumn.md) . Per recuperare o modificare la larghezza di una colonna, usare i messaggi [**LVM \_ GETCOLUMNWIDTH**](lvm-getcolumnwidth.md) e [**LVM \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) .

A meno che non venga specificato lo stile della finestra [**\_ nocolumnheader LVS**](list-view-window-styles.md) , le intestazioni di colonna vengono visualizzate in visualizzazione report. L'utente può fare clic su un'intestazione di colonna, causando l'invio di un codice di notifica [**LVN \_ COLUMNCLICK**](lvn-columnclick.md) alla finestra padre. In genere, la finestra padre Ordina il controllo di visualizzazione elenco in base alla colonna specificata quando si verifica questo clic. L'utente può inoltre trascinare le guide delle colonne tra le intestazioni per ridimensionarle.

I controlli elenco-visualizzazione possono visualizzare immagini accanto ai titoli delle colonne. Per implementare questa funzionalità, specificare il valore dell' **\_ immagine LVCF** e assegnare l'indice dell'immagine al membro **IImage** nella struttura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) .

I controlli elenco-visualizzazione possono impostare l'ordine in cui vengono visualizzate le colonne. Per implementare questa funzionalità, specificare il valore dell' **\_ ordine LVCF** e assegnare l'ordine delle colonne al membro **iOrder** nella struttura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) . L'ordine delle colonne è in base zero ed è in ordine da sinistra a destra. Ad esempio, zero indica la colonna più a sinistra.

## <a name="list-view-scroll-position"></a>Posizione di scorrimento List-View

A meno che non sia specificato lo stile della finestra [**\_ NoScroll LVS**](list-view-window-styles.md) , è possibile scorrere un controllo elenco-visualizzazione per visualizzare più elementi rispetto a quelli che possono essere inseriti nell'area client del controllo. È possibile recuperare la posizione di scorrimento di un controllo di visualizzazione elenco e le informazioni correlate, scorrere un controllo visualizzazione elenco in base a una quantità specificata o scorrere un controllo elenco-visualizzazione in modo che un elemento elenco specificato sia visibile.

Nella visualizzazione icone o nella visualizzazione icone piccole, la posizione di scorrimento corrente è definita dall' *origine della visualizzazione*. L'origine della vista è il set di coordinate, relativo all'area visibile del controllo di visualizzazione elenco, che corrisponde alle coordinate della vista (0,0). Per recuperare l'origine della visualizzazione corrente, usare il messaggio [**LVM \_ getOrigin**](lvm-getorigin.md) . Questo messaggio deve essere usato solo nell'icona o nella visualizzazione icona piccola; viene restituito un errore nella visualizzazione elenco o report.

Nella visualizzazione elenco o report la posizione di scorrimento corrente è definita dall' *indice superiore*. L'indice superiore è l'indice del primo elemento visibile nel controllo di visualizzazione elenco. Per recuperare l'indice principale corrente, usare il messaggio [**LVM \_ GETTOPINDEX**](lvm-gettopindex.md) . Questo messaggio restituisce un risultato valido solo nella visualizzazione elenco o report; restituisce zero nell'icona o nella visualizzazione icona piccola.

È possibile usare il messaggio [**LVM \_ GETVIEWRECT**](lvm-getviewrect.md) per recuperare il rettangolo di delimitazione di tutti gli elementi in un controllo visualizzazione elenco, rispetto all'area visibile del controllo.

Il [**messaggio \_ GETCOUNTPERPAGE di LVM**](lvm-getcountperpage.md) restituisce il numero di elementi che rientrano in una pagina del controllo di visualizzazione elenco. Questo messaggio restituisce un risultato valido solo nelle visualizzazioni elenco e report; nelle visualizzazioni icona e icone piccole restituisce il numero totale di elementi.

Per scorrere un controllo di visualizzazione elenco in base a un importo specifico, usare il messaggio di [**\_ scorrimento LVM**](lvm-scroll.md) . Usando il messaggio [**LVM \_ ENSUREVISIBLE**](lvm-ensurevisible.md) , è possibile scorrere il controllo visualizzazione elenco, se necessario, per assicurarsi che un elemento specificato sia visibile.

## <a name="list-view-label-editing"></a>Modifica dell'etichetta List-View

Un controllo di visualizzazione elenco con lo stile della finestra [**\_ EDITLABELS LVS**](list-view-window-styles.md) consente all'utente di modificare le etichette degli elementi sul posto. L'utente inizia la modifica facendo clic sull'etichetta di un elemento con lo stato attivo. In alternativa, un'applicazione può iniziare a modificare automaticamente usando il messaggio [**LVM \_ EDITLABEL**](lvm-editlabel.md) . Il controllo elenco-visualizzazione notifica alla finestra padre quando ha inizio la modifica e quando viene annullata o completata. Al termine della modifica, la finestra padre è responsabile dell'aggiornamento dell'etichetta dell'elemento, se appropriato.

Quando viene avviata la modifica dell'etichetta, viene creato, posizionato e inizializzato un [controllo di modifica](edit-controls.md) . Prima che venga visualizzato, il controllo elenco-visualizzazione Invia la finestra padre di un codice di notifica [ \_ BEGINLABELEDIT LVN](lvn-beginlabeledit.md) . Se è necessario modificare il processo di modifica delle etichette, è possibile implementare un gestore per la notifica.

Un gestore di notifiche [ \_ BEGINLABELEDIT LVN](lvn-beginlabeledit.md) consente di controllare le etichette che possono essere modificate dall'utente. Per evitare la modifica dell'etichetta, restituire un valore diverso da zero. Per personalizzare la modifica delle etichette, fare in modo che il gestore di notifiche recuperi un handle per il controllo di modifica inviando un messaggio [**\_ GETEDITCONTROL LVM**](lvm-geteditcontrol.md) al controllo List-View. Una volta ottenuto tale handle, è possibile personalizzare il controllo di modifica inviando i normali \_ messaggi em xxx. Ad esempio, per limitare la quantità di testo che un utente può immettere, inviare il controllo di modifica un messaggio [**\_ LIMITTEXT em**](em-limittext.md) . È possibile modificare il testo predefinito del controllo di modifica con [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta). È anche possibile sottoclassare il controllo Edit per intercettare e rimuovere i caratteri non validi.

Quando la modifica delle etichette viene annullata o completata, un controllo elenco-visualizzazione Invia la finestra padre a un codice di notifica [ \_ ENDLABELEDIT LVN](lvn-endlabeledit.md) . Il parametro *lParam* è l'indirizzo di una struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Il membro dell' **elemento** di questa struttura è una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) il cui membro **iItem** identifica l'elemento. Se la modifica viene annullata, il membro **pszText** della struttura **LVITEM** è **null**. in caso contrario, **pszText** è l'indirizzo del testo modificato. La finestra padre è responsabile dell'aggiornamento dell'etichetta dell'elemento se desidera che la nuova etichetta venga mantenuta.

## <a name="list-view-colors"></a>Colori List-View

Un'applicazione può recuperare e impostare tre colori per un controllo visualizzazione elenco.



| Colore                   | Messaggi utilizzati per recuperare e impostare i colori                                                             |
|-------------------------|------------------------------------------------------------------------------------------------------|
| Colore del testo              | [**LVM \_ GETTEXTCOLOR**](lvm-gettextcolor.md), [ **LVM \_ SETTEXTCOLOR**](lvm-settextcolor.md)         |
| Colore di sfondo del testo   | [**LVM \_ GETTEXTBKCOLOR**](lvm-gettextbkcolor.md), [ **LVM \_ SETTEXTBKCOLOR**](lvm-settextbkcolor.md) |
| Colore di sfondo della finestra | [**LVM \_ GETBKCOLOR**](lvm-getbkcolor.md), [ **LVM \_ SETBKCOLOR**](lvm-setbkcolor.md)                 |



 

Per personalizzare l'aspetto di un controllo di visualizzazione elenco in modo più significativo, usare [nm \_ CUSTOMDRAW (visualizzazione elenco)](nm-customdraw-list-view.md) o usare gli stili di visualizzazione (vedere [stili visivi](themes-overview.md) e [Abilitazione degli stili di visualizzazione](cookbook-overview.md)).

## <a name="arranging-list-items-by-group"></a>Disposizione degli elementi dell'elenco per gruppo

Le funzionalità di raggruppamento del controllo visualizzazione elenco consentono di raggruppare visivamente i set di elementi correlati logicamente. I gruppi possono essere creati in base alle proprietà degli elementi, agli attributi o ad altre caratteristiche. Questi gruppi vengono in genere separati sullo schermo da un'intestazione orizzontale che contiene il nome del gruppo. Lo screenshot seguente Mostra gli elementi raggruppati.

![Screenshot di un controllo visualizzazione elenco, con cani in un gruppo e gatti in un altro gruppo](images/lv-groups.png)

Utilizzare la struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) per archiviare le informazioni su un gruppo, ad esempio il testo dell'intestazione e del piè di pagina, lo stato corrente del gruppo e così via. L'API di raggruppamento include messaggi che consentono di gestire gruppi ed elementi di gruppo aggiungendo elementi ai gruppi, aggiungendo gruppi alle visualizzazioni, ordinando gli elementi del gruppo ed eseguendo query sui gruppi per le dimensioni degli elementi e altre informazioni. Ad esempio, è possibile impostare e recuperare i parametri di visualizzazione per ogni gruppo usando le macro [**ListView \_ SetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupmetrics) e [**ListView \_ GetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupmetrics) .

Il raggruppamento è disponibile in tutte le visualizzazioni ad eccezione della visualizzazione elenco. Non è disponibile nei controlli con lo stile [**\_ OWNERDATA di LVS**](list-view-window-styles.md) .

Per ulteriori informazioni, vedere [utilizzo dei controlli List-View](using-list-view-controls.md).

## <a name="insertion-marks"></a>Segni di inserimento

I contrassegni di inserimento mostrano gli utenti in cui verranno inseriti gli elementi trascinati. Segni di inserimento attualmente visualizzati quando l'utente trascina un elemento nel menu **Start** o nella barra avvio veloce. Il segno di inserimento funziona anche per gli elenchi impostati per la disposizione. Quando un utente trascina un elemento in un punto intermedio tra due elementi, il segno di inserimento indica la nuova posizione prevista dell'elemento. Lo screenshot seguente mostra un segno di inserimento.

![screenshot che mostra un segno di inserimento durante il trascinamento di un file tra altri due in un controllo visualizzazione elenco](images/insertmark.png)

Gli elementi dell'API del contrassegno di inserimento consentono di posizionare i segni di inserimento fornendo messaggi e flag che eseguono il rilevamento dei passaggi, che specificano la posizione e l'aspetto del contrassegno di inserimento per elemento e la query per ottenere informazioni sulle dimensioni e sull'aspetto correnti del segno di inserimento.

## <a name="see-also"></a>Vedi anche

* [Esempio di controllo ListView virtuale](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)
