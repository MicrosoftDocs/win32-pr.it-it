---
description: Questa panoramica illustra le funzionalità delle finestre, ad esempio tipi di finestra, stati, dimensioni e posizione.
ms.assetid: 8318c22f-85a2-490e-8233-ee1e234890d9
title: Funzionalità delle finestre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9437ab95d12ccc56cdf5e87af2127f4c34ad6def7f07f4e79246a2ad591a5ae8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110681"
---
# <a name="window-features"></a>Funzionalità delle finestre

Questa panoramica illustra le funzionalità delle finestre, ad esempio tipi di finestra, stati, dimensioni e posizione.

-   [Tipi di finestre](#window-types)
    -   [Elementi sovrapposti Windows](#overlapped-windows)
    -   [Popup Windows](#pop-up-windows)
    -   [Elementi Windows](#child-windows)
        -   [Posizionamento](#positioning)
        -   [Ritaglio](#clipping)
        -   [Relazione con la finestra padre](#relationship-to-parent-window)
        -   [Messaggi](#size-and-position-messages)
    -   [Livelli Windows](#layered-windows)
    -   [Solo messaggi Windows](#message-only-windows)
-   [Relazioni tra finestre](#window-relationships)
    -   [Primo piano e sfondo Windows](#foreground-and-background-windows)
    -   [Proprietà Windows](#owned-windows)
    -   [Ordine Z](#z-order)
-   [Finestra Mostra stato](#window-show-state)
    -   [Finestra attiva](#active-window)
    -   [Disabilitato Windows](#disabled-windows)
    -   [Visibilità della finestra](#window-visibility)
    -   [Ridotta a icona, ingrandita e ripristinata Windows](#minimized-maximized-and-restored-windows)
-   [Dimensioni e posizione della finestra](#window-size-and-position)
    -   [Dimensioni e posizione predefinite](#default-size-and-position)
    -   [Dimensioni rilevamento](#tracking-size)
    -   [Comandi di sistema](#system-commands)
    -   [Funzioni di dimensione e posizione](#size-and-position-functions)
    -   [Messaggi di dimensioni e posizione](#size-and-position-messages)
-   [Animazione della finestra](#window-animation)
-   [Layout e mirroring della finestra](#window-layout-and-mirroring)
    -   [Finestre di dialogo e finestre di messaggio per il mirroring](#mirroring-dialog-boxes-and-message-boxes)
    -   [Mirroring dei contesti di dispositivo non associati a una finestra](#mirroring-device-contexts-not-associated-with-a-window)
-   [Distruzione della finestra](#window-destruction)

## <a name="window-types"></a>Tipi di finestre

Questa sezione contiene gli argomenti seguenti che descrivono i tipi di finestra.

-   [Elementi sovrapposti Windows](#overlapped-windows)
-   [Popup Windows](#pop-up-windows)
-   [Elementi Windows](#child-windows)
-   [Livelli Windows](#layered-windows)
-   [Solo messaggi Windows](#message-only-windows)

### <a name="overlapped-windows"></a>Elementi sovrapposti Windows

Una *finestra sovrapposta* è una finestra di primo livello (finestra non figlio) con barra del titolo, bordo e area client; è destinato a fungere da finestra principale di un'applicazione. Può anche avere un menu della finestra, pulsanti di riduzione a icona e ingrandimento e barre di scorrimento. Una finestra sovrapposta usata come finestra principale include in genere tutti questi componenti.

Specificando lo stile [**WS \_ OVERLAPPED**](window-styles.md) o **WS \_ OVERLAPPEDWINDOW** nella [**funzione CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) un'applicazione crea una finestra sovrapposta. Se si usa lo **stile WS \_ OVERLAPPED,** la finestra ha una barra del titolo e un bordo. Se si usa lo **stile WS \_ OVERLAPPEDWINDOW,** la finestra ha una barra del titolo, un bordo di ridimensionamento, un menu della finestra e pulsanti di riduzione a icona e ingrandimento.

### <a name="pop-up-windows"></a>Popup Windows

Una *finestra popup è* un tipo speciale di finestra sovrapposta usata per finestre di dialogo, finestre di messaggio e altre finestre temporanee che vengono visualizzate all'esterno della finestra principale di un'applicazione. Le barre del titolo sono facoltative per le finestre popup. In caso contrario, le finestre popup sono uguali alle finestre sovrapposte dello [**stile WS \_ OVERLAPPED.**](window-styles.md)

Per creare una finestra popup, specificare lo [**stile \_ WS POPUP**](window-styles.md) in [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Per includere una barra del titolo, specificare lo **stile WS \_ CAPTION.** Usare lo **stile WS \_ POPUPWINDOW** per creare una finestra popup con un bordo e un menu della finestra. Lo **stile WS \_ CAPTION** deve essere combinato con lo **stile \_ WS POPUPWINDOW** per rendere visibile il menu della finestra.

### <a name="child-windows"></a>Elementi Windows

Una *finestra figlio* ha lo stile [**\_ WS CHILD**](window-styles.md) ed è limitata all'area client della finestra padre. Un'applicazione usa in genere finestre figlio per dividere l'area client di una finestra padre in aree funzionali. Per creare una finestra figlio, specificare lo **stile \_ WS CHILD** nella funzione [**CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)

Una finestra figlio deve avere una finestra padre. La finestra padre può essere una finestra sovrapposta, una finestra popup o anche un'altra finestra figlio. La finestra padre viene specificata quando si chiama [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Se si specifica lo [**stile WS \_ CHILD**](window-styles.md) in **CreateWindowEx** ma non si specifica una finestra padre, il sistema non crea la finestra.

Una finestra figlio ha un'area client ma non altre funzionalità, a meno che non siano richieste in modo esplicito. Un'applicazione può richiedere una barra del titolo, un menu della finestra, pulsanti di riduzione a icona e ingrandimento, un bordo e barre di scorrimento per una finestra figlio, ma una finestra figlio non può avere un menu. Se l'applicazione specifica un handle di menu, quando registra la classe della finestra figlio o crea la finestra figlio, l'handle di menu viene ignorato. Se non viene specificato alcuno stile del bordo, il sistema crea una finestra senza bordo. Un'applicazione può usare finestre figlio senza bordo per dividere l'area client di una finestra padre mantenendo le divisioni invisibili all'utente.

In questa sezione vengono illustrati gli aspetti seguenti delle finestre figlio:

-   [Posizionamento](#positioning)
-   [Ritaglio](#clipping)
-   [Relazione con la finestra padre](#relationship-to-parent-window)
-   [Messaggi](#size-and-position-messages)

#### <a name="positioning"></a>Posizionamento

Il sistema posiziona sempre una finestra figlio rispetto all'angolo superiore sinistro dell'area client della finestra padre. Nessuna parte di una finestra figlio viene mai visualizzata all'esterno dei bordi della finestra padre. Se un'applicazione crea una finestra figlio più grande della finestra padre o posiziona una finestra figlio in modo che parte o tutta la finestra figlio si estenda oltre i bordi della finestra padre, il sistema ritaglia la finestra figlio. ciò significa che la parte esterna all'area client della finestra padre non viene visualizzata. Le azioni che interessano la finestra padre possono influire anche sulla finestra figlio, come indicato di seguito.



| Finestra padre | Finestra figlio                                                                                                             |
|---------------|--------------------------------------------------------------------------------------------------------------------------|
| Eliminata     | Eliminato prima che la finestra padre venga distrutta.                                                                         |
| Nascosto        | Nascosto prima che la finestra padre sia nascosta. Una finestra figlio è visibile solo quando la finestra padre è visibile.             |
| trasferito         | Spostato con l'area client della finestra padre. La finestra figlio è responsabile del disegno dell'area client dopo lo spostamento. |
| Mostrato         | Viene visualizzato dopo la visualizzazione della finestra padre.                                                                                  |



 

#### <a name="clipping"></a>Ritaglio

Il sistema non ritaglia automaticamente una finestra figlio dall'area client della finestra padre. Ciò significa che la finestra padre viene disegnata sulla finestra figlio se esegue un disegno nella stessa posizione della finestra figlio. Tuttavia, il sistema ritaglia la finestra figlio dall'area client della finestra padre se la finestra padre ha lo [**stile \_ WS CLIPCHILDREN.**](window-styles.md) Se la finestra figlio viene ritagliata, la finestra padre non può disegnare su di essa.

Una finestra figlio può sovrapporsi ad altre finestre figlio nella stessa area client. Una finestra figlio che condivide la stessa finestra padre di una o più altre finestre figlio è detta finestra *di pari livello.* Le finestre di pari livello possono essere disegnate nell'area client dell'altra, a meno che una delle finestre figlio non abbia lo [**stile \_ WS CLIPSIBLINGS.**](window-styles.md) Se una finestra figlio ha questo stile, qualsiasi parte della finestra di pari livello che si trova all'interno della finestra figlio viene ritagliata.

Se una finestra ha lo [**stile WS \_ CLIPCHILDREN**](window-styles.md) o **WS \_ CLIPSIBLINGS,** si verifica una lieve perdita di prestazioni. Ogni finestra occupa risorse di sistema, quindi un'applicazione non deve usare finestre figlio in modo indiscriminato. Per ottenere prestazioni ottimali, un'applicazione che deve dividere logicamente la finestra principale deve eseguire questa operazione nella routine della finestra principale anziché usando le finestre figlio.

#### <a name="relationship-to-parent-window"></a>Relazione con la finestra padre

Un'applicazione può modificare la finestra padre di una finestra figlio esistente chiamando la [**funzione SetParent.**](/windows/win32/api/winuser/nf-winuser-setparent) In questo caso, il sistema rimuove la finestra figlio dall'area client della finestra padre precedente e la sposta nell'area client della nuova finestra padre. Se **SetParent** specifica un handle **NULL,** la finestra del desktop diventa la nuova finestra padre. In questo caso, la finestra figlio viene disegnata sul desktop, all'esterno dei bordi di qualsiasi altra finestra. La [**funzione GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) recupera un handle per la finestra padre di una finestra figlio.

La finestra padre clinea una parte della relativa area client a una finestra figlio e la finestra figlio riceve tutto l'input da quest'area. La classe della finestra non deve essere la stessa per ognuna delle finestre figlio della finestra padre. Ciò significa che un'applicazione può riempire una finestra padre con finestre figlio che hanno un aspetto diverso ed eseguono attività diverse. Ad esempio, una finestra di dialogo può contenere molti tipi di controlli, ognuno dei quali è una finestra figlio che accetta tipi diversi di dati dall'utente.

Una finestra figlio ha una sola finestra padre, ma un elemento padre può avere un numero qualsiasi di finestre figlio. Ogni finestra figlio, a sua volta, può avere finestre figlio. In questa catena di finestre ogni finestra figlio è denominata finestra discendente della finestra padre originale. Un'applicazione usa [**la funzione IsChild**](/windows/win32/api/winuser/nf-winuser-ischild) per individuare se una determinata finestra è una finestra figlio o una finestra discendente di una determinata finestra padre.

La [**funzione EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) enumera le finestre figlio di una finestra padre. **EnumChildWindows** passa quindi l'handle a ogni finestra figlio a una funzione di callback definita dall'applicazione. Vengono enumerate anche le finestre discendenti della finestra padre specificata.

#### <a name="messages"></a>Messaggi

Il sistema passa i messaggi di input di una finestra figlio direttamente alla finestra figlio. I messaggi non vengono passati attraverso la finestra padre. L'unica eccezione è se la finestra figlio è stata disabilitata dalla [**funzione EnableWindow.**](/windows/win32/api/winuser/nf-winuser-enablewindow) In questo caso, il sistema passa tutti i messaggi di input che sarebbero passati alla finestra figlio alla finestra padre. In questo modo la finestra padre può esaminare i messaggi di input e abilitare la finestra figlio, se necessario.

Una finestra figlio può avere un identificatore integer univoco. Gli identificatori di finestra figlio sono importanti quando si lavora con le finestre di controllo. Un'applicazione indirizza l'attività di un controllo inviando messaggi. L'applicazione usa l'identificatore della finestra figlio del controllo per indirizzare i messaggi al controllo. Inoltre, un controllo invia messaggi di notifica alla relativa finestra padre. Un messaggio di notifica include l'identificatore della finestra figlio del controllo, che l'elemento padre usa per identificare il controllo che ha inviato il messaggio. Un'applicazione specifica l'identificatore della finestra figlio per altri tipi di finestre figlio impostando il parametro *hMenu* della [**funzione CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) su un valore anziché su un handle di menu.

### <a name="layered-windows"></a>Livelli Windows

L'uso di una finestra su più livelli può migliorare significativamente le prestazioni e gli effetti visivi per una finestra con una forma complessa, ne aggiunge un'animazione o vuole usare effetti di fusione alfa. Il sistema compone e ridisegna automaticamente le finestre su più livelli e le finestre delle applicazioni sottostanti. Di conseguenza, il rendering delle finestre su più livelli viene eseguito senza problemi, senza lo sfarfallio tipico delle aree della finestra complesse. Inoltre, le finestre su più livelli possono essere parzialmente traslucido, ad esempio con alpha blended.

Per creare una finestra su più livelli, specificare lo stile della finestra estesa **WS \_ EX \_ LAYERED** quando si chiama la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) oppure chiamare la [**funzione SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) per impostare **WS \_ EX \_** SU più livelli dopo la creazione della finestra. Dopo la **chiamata a CreateWindowEx,** la finestra su più livelli non diventa visibile fino a quando non viene chiamata la funzione [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) o [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow) per questa finestra.

> [!Note]  
> A partire Windows 8, **WS \_ EX \_ LAYERED** può essere usato con finestre figlio e finestre di primo livello. Le Windows precedenti supportano **WS \_ EX a \_ livelli** solo per le finestre di primo livello.

 

Per impostare il livello di opacità o la chiave di colore di trasparenza per una determinata finestra su più livelli, chiama [**SetLayeredWindowAttributes.**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) Dopo la chiamata, il sistema potrebbe comunque chiedere alla finestra di disegnare quando la finestra viene visualizzata o ridimensionata. Tuttavia, poiché il sistema archivia l'immagine di una finestra su più livelli, il sistema non chiederà alla finestra di disegnare se parti di essa vengono rivelate in seguito a uno spostamento della finestra relativa sul desktop. Le applicazioni legacy non devono ristrutturare il codice di disegno se vogliono aggiungere effetti di traslucidità o trasparenza per una finestra, perché il sistema reindirizza il disegno di finestre che ha chiamato **SetLayeredWindowAttributes** nella memoria fuori schermo e lo ricomporre per ottenere l'effetto desiderato.

Per un'animazione più veloce ed efficiente o se sono necessari valori alfa per pixel, [**chiamare UpdateLayeredWindow.**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow) **UpdateLayeredWindow** deve essere usato principalmente quando l'applicazione deve fornire direttamente la forma e il contenuto di una finestra su più livelli, senza usare il meccanismo di reindirizzamento fornito dal sistema tramite [**SetLayeredWindowAttributes.**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) Inoltre, l'uso di **UpdateLayeredWindow** usa direttamente la memoria in modo più efficiente, perché il sistema non richiede la memoria aggiuntiva necessaria per archiviare l'immagine della finestra reindirizzata. Per ottenere la massima efficienza nell'animazione delle finestre, chiama **UpdateLayeredWindow** per modificare la posizione e le dimensioni di una finestra su più livelli. Si noti che dopo la chiamata a **SetLayeredWindowAttributes,** le chiamate **updateLayeredWindow** successive avranno esito negativo fino a quando il bit dello stile di livelli non viene cancellato e impostato nuovamente.

L'hit testing di una finestra su più livelli si basa sulla forma e sulla trasparenza della finestra. Ciò significa che le aree della finestra con una chiave di colore o il cui valore alfa è zero consentiranno il passaggio dei messaggi del mouse. Tuttavia, se la finestra su più livelli ha lo stile della finestra estesa **WS \_ EX \_ TRANSPARENT,** la forma della finestra su più livelli verrà ignorata e gli eventi del mouse verranno passati ad altre finestre sotto la finestra su più livelli.

### <a name="message-only-windows"></a>Message-Only Windows

Una *finestra di solo messaggio* consente di inviare e ricevere messaggi. Non è visibile, non ha un ordine Z, non può essere enumerato e non riceve messaggi trasmessi. La finestra invia semplicemente messaggi.

Per creare una finestra solo messaggio, specificare la costante [HWND \_ MESSAGE](#message-only-windows) o un handle per una finestra di solo messaggio esistente nel *parametro hWndParent* della [**funzione CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) È anche possibile modificare una finestra esistente in una finestra di solo messaggio specificando HWND MESSAGE nel \_ *parametro hWndNewParent* della [**funzione SetParent.**](/windows/win32/api/winuser/nf-winuser-setparent)

Per trovare finestre solo messaggi, specificare [HWND \_ MESSAGE](#message-only-windows) nel *parametro hwndParent* della [**funzione FindWindowEx.**](/windows/win32/api/winuser/nf-winuser-findwindowexa) **FindWindowEx** cerca anche le finestre solo messaggi e le finestre di primo livello se entrambi i parametri *hwndParent* e *hwndChildAfter* sono **NULL.**

## <a name="window-relationships"></a>Relazioni tra finestre

Esistono diversi modi in cui una finestra può essere correlata all'utente o a un'altra finestra. Una finestra può essere una finestra di proprietà, una finestra in primo piano o una finestra di sfondo. Una finestra ha anche un ordine Z rispetto ad altre finestre. Per altre informazioni, vedere i seguenti argomenti:

-   [Primo piano e Sfondo Windows](#foreground-and-background-windows)
-   [Proprietà Windows](#owned-windows)
-   [Ordine Z](#z-order)

### <a name="foreground-and-background-windows"></a>Primo piano e Sfondo Windows

Ogni processo può avere più thread di esecuzione e ogni thread può creare finestre. Il thread che ha creato la finestra con cui l'utente sta attualmente lavorando è denominato thread in primo piano e la finestra è denominata *finestra in primo piano.* Tutti gli altri thread sono thread in background e le finestre create dai thread in background sono denominate *finestre in background.*

Ogni thread ha un livello di priorità che determina la quantità di tempo della CPU ricevuta dal thread. Anche se un'applicazione può impostare il livello di priorità dei thread, in genere il thread in primo piano ha un livello di priorità leggermente superiore rispetto ai thread in background. Poiché ha una priorità più alta, il thread in primo piano riceve più tempo della CPU rispetto ai thread in background. Il thread in primo piano ha una priorità di base normale di 9; un thread in background ha una priorità di base normale di 7.

L'utente imposta la finestra in primo piano facendo clic su una finestra o usando la combinazione di tasti ALT+TAB o ALT+ESC. Per recuperare un handle per la finestra in primo piano, usa [**la funzione GetForegroundWindow.**](/windows/win32/api/winuser/nf-winuser-getforegroundwindow) Per verificare se la finestra dell'applicazione è in primo piano, confrontare l'handle restituito da **GetForegroundWindow** con quello della finestra dell'applicazione.

Un'applicazione imposta la finestra in primo piano usando [**la funzione SetForegroundWindow.**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow)

Il sistema limita i processi che possono impostare la finestra in primo piano. Un processo può impostare la finestra in primo piano solo se:

- Tutte le condizioni seguenti sono vere:
  - Il processo che chiama **SetForegroundWindow** appartiene a un'applicazione desktop, non a un'app UWP o a un'app Windows Store progettata per Windows 8 o 8.1.
  - Il processo in primo piano non ha disabilitato le chiamate a **SetForegroundWindow** da una chiamata precedente alla [**funzione LockSetForegroundWindow.**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow)
  - Il timeout del blocco in primo piano è scaduto (vedere [ **SPI_GETFOREGROUNDLOCKTIMEOUT** in **SystemParametersInfo).**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa#SPI_GETFOREGROUNDLOCKTIMEOUT)
  - Non è attivo alcun menu.
- Inoltre, almeno una delle condizioni seguenti è vera:
  - Il processo chiamante è il processo in primo piano.
  - Il processo chiamante è stato avviato dal processo in primo piano.
  - Attualmente non è presente alcuna finestra in primo piano e pertanto non è disponibile alcun processo in primo piano.
  - Il processo chiamante ha ricevuto l'ultimo evento di input.
  - È in corso il debug del processo in primo piano o del processo chiamante.

È possibile che a un processo sia negato il diritto di impostare la finestra in primo piano anche se soddisfa queste condizioni.

Un processo che può impostare la finestra in primo piano può consentire a un altro processo di impostare la finestra in primo piano chiamando la funzione [**AllowSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow) o chiamando la [**funzione BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) con il flag **\_ ALLOWSFW di BSF.** Il processo in primo piano può disabilitare le chiamate a [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) chiamando la [**funzione LockSetForegroundWindow.**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow)

### <a name="owned-windows"></a>Proprietà Windows

Una finestra sovrapposta o popup può essere di proprietà di un'altra finestra sovrapposta o popup. Il fatto di essere di proprietà pone diversi vincoli in una finestra.

-   Una finestra di proprietà è sempre sopra il proprietario nell'ordine z.
-   Il sistema elimina automaticamente una finestra di proprietà quando il proprietario viene eliminato.
-   Una finestra di proprietà viene nascosta quando il proprietario è ridotto a icona.

Solo una finestra sovrapposta o popup può essere una finestra proprietaria. una finestra figlio non può essere una finestra proprietaria. Un'applicazione crea una finestra di proprietà specificando l'handle di finestra del proprietario come parametro *hwndParent* di [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) quando crea una finestra con lo stile [**WS \_ OVERLAPPED**](window-styles.md) o **WS \_ POPUP.** Il *parametro hwndParent* deve identificare una finestra sovrapposta o popup. Se *hwndParent identifica* una finestra figlio, il sistema assegna la proprietà alla finestra padre di primo livello della finestra figlio. Dopo aver creato una finestra di proprietà, un'applicazione non può trasferire la proprietà della finestra in un'altra finestra.

Le finestre di dialogo e le finestre di messaggio sono finestre di proprietà per impostazione predefinita. Un'applicazione specifica la finestra proprietaria quando si chiama una funzione che crea una finestra di dialogo o una finestra di messaggio.

Un'applicazione può usare [**la funzione GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) con il flag **GW \_ OWNER** per recuperare un handle per il proprietario di una finestra.

### <a name="z-order"></a>Ordine Z

*L'ordine z* di una finestra indica la posizione della finestra in uno stack di finestre sovrapposte. Questo stack di finestre è orientato lungo un asse immaginario, l'asse z, che si estende verso l'esterno dello schermo. La finestra nella parte superiore dell'ordine Z si sovrappone a tutte le altre finestre. La finestra nella parte inferiore dell'ordine Z è sovrapposta a tutte le altre finestre.

Il sistema gestisce l'ordine z in un singolo elenco. Aggiunge finestre all'ordine z a seconda che siano finestre di primo livello, finestre di primo livello o finestre figlio. Una *finestra in primo piano* si sovrappone a tutte le altre finestre non in primo piano, indipendentemente dal fatto che si tratta della finestra attiva o in primo piano. Una finestra in primo piano ha lo **stile WS \_ EX \_ TOPMOST.** Tutte le finestre in primo piano vengono visualizzate nell'ordine Z prima di qualsiasi finestra non in primo piano. Una finestra figlio viene raggruppata con il relativo elemento padre in ordine Z.

Quando un'applicazione crea una finestra, il sistema la inserisce nella parte superiore dell'ordine Z per le finestre dello stesso tipo. Puoi usare la [**funzione BringWindowToTop**](/windows/win32/api/winuser/nf-winuser-bringwindowtotop) per portare una finestra all'inizio dell'ordine Z per le finestre dello stesso tipo. È possibile ridisporre l'ordine z usando [**le funzioni SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) [**e DeferWindowPos.**](/windows/win32/api/winuser/nf-winuser-deferwindowpos)

L'utente modifica l'ordine Z attivando un'altra finestra. Il sistema posiziona la finestra attiva nella parte superiore dell'ordine Z per le finestre dello stesso tipo. Quando una finestra viene visualizzata nella parte superiore dell'ordine Z, si verificano anche le finestre figlio. È possibile usare la [**funzione GetTopWindow**](/windows/win32/api/winuser/nf-winuser-gettopwindow) per cercare tutte le finestre figlio di una finestra padre e restituire un handle alla finestra figlio più alta nell'ordine Z. La [**funzione GetNextWindow**](/windows/win32/api/winuser/nf-winuser-getnextwindow) recupera un handle per la finestra successiva o precedente nell'ordine Z.

## <a name="window-show-state"></a>Finestra Mostra stato

In qualsiasi momento, una finestra può essere attiva o inattiva. nascosto o visibile; e ridotta a icona, ingrandita o ripristinata. Queste qualità vengono definite collettivamente come *finestra di visualizzazione dello stato*. Negli argomenti seguenti viene illustrato lo stato di visualizzazione della finestra:

-   [Finestra attiva](#active-window)
-   [Disabilitato Windows](#disabled-windows)
-   [Visibilità delle finestre](#window-visibility)
-   [Riduzione a icona, ingrandita e ripristinata Windows](#minimized-maximized-and-restored-windows)

### <a name="active-window"></a>Finestra attiva

Una *finestra attiva* è la finestra di primo livello dell'applicazione con cui l'utente sta attualmente lavorando. Per consentire all'utente di identificare facilmente la finestra attiva, il sistema la posiziona nella parte superiore dell'ordine z e modifica il colore della barra del titolo e del bordo nei colori della finestra attiva definiti dal sistema. Solo una finestra di primo livello può essere una finestra attiva. Quando l'utente utilizza una finestra figlio, il sistema attiva la finestra padre di primo livello associata alla finestra figlio.

Nel sistema è attiva una sola finestra di primo livello alla volta. L'utente attiva una finestra di primo livello facendo clic su di essa (o su una delle finestre figlio) o usando la combinazione di tasti ALT+ESC o ALT+TAB. Un'applicazione attiva una finestra di primo livello chiamando la [**funzione SetActiveWindow.**](/windows/win32/api/winuser/nf-winuser-setactivewindow) Altre funzioni possono causare l'attivazione da parte del sistema di un'altra finestra di primo livello, tra cui [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos), [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos), [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement)e [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow). Anche se un'applicazione può attivare una finestra di primo livello diversa in qualsiasi momento, per evitare di confondere l'utente, è consigliabile farlo solo in risposta a un'azione dell'utente. Un'applicazione usa [**la funzione GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) per recuperare un handle per la finestra attiva.

Quando l'attivazione cambia da una finestra di primo livello di un'applicazione alla finestra di primo livello di un'altra, il sistema invia un messaggio [**WM \_ ACTIVATEAPP**](wm-activateapp.md) a entrambe le applicazioni, notificando la modifica. Quando l'attivazione cambia in un'altra finestra di primo livello nella stessa applicazione, il sistema invia a entrambe le finestre un [**messaggio WM \_ ACTIVATE.**](../inputdev/wm-activate.md)

### <a name="disabled-windows"></a>Disabilitato Windows

Una finestra può essere disabilitata. Una *finestra disabilitata* non riceve input da tastiera o mouse dall'utente, ma può ricevere messaggi da altre finestre, da altre applicazioni e dal sistema. Un'applicazione disabilita in genere una finestra per impedire all'utente di usarla. Ad esempio, un'applicazione può disabilitare un pulsante di comando in una finestra di dialogo per impedire all'utente di sceglierlo. Un'applicazione può abilitare una finestra disabilitata in qualsiasi momento. L'abilitazione di una finestra ripristina l'input normale.

Per impostazione predefinita, una finestra viene abilitata al momento della creazione. Un'applicazione può tuttavia [**specificare lo stile WS \_ DISABLED**](window-styles.md) per disabilitare una nuova finestra. Un'applicazione abilita o disabilita una finestra esistente usando la [**funzione EnableWindow.**](/windows/win32/api/winuser/nf-winuser-enablewindow) Il sistema invia un [**messaggio WM \_ ENABLE**](wm-enable.md) a una finestra quando lo stato abilitato sta per cambiare. Un'applicazione può determinare se una finestra è abilitata usando la [**funzione IsWindowEnabled.**](/windows/win32/api/winuser/nf-winuser-iswindowenabled)

Quando una finestra figlio è disabilitata, il sistema passa i messaggi di input del mouse dell'elemento figlio alla finestra padre. L'elemento padre utilizza i messaggi per determinare se abilitare la finestra figlio. Per altre informazioni, vedere [Input del mouse.](../inputdev/mouse-input.md)

Solo una finestra alla volta può ricevere l'input da tastiera. si dice che la finestra abbia lo stato attivo della tastiera. Se un'applicazione usa la [**funzione EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) per disabilitare una finestra di attivazione della tastiera, la finestra perde lo stato attivo oltre a essere disabilitata. **EnableWindow imposta** quindi lo stato attivo della tastiera **su NULL,** ovvero nessuna finestra ha lo stato attivo. Se una finestra figlio o un'altra finestra discendente ha lo stato attivo, la finestra discendente perde lo stato attivo quando la finestra padre è disabilitata. Per altre informazioni, vedere [Input da tastiera.](../inputdev/keyboard-input.md)

### <a name="window-visibility"></a>Visibilità delle finestre

Una finestra può essere visibile o nascosta. Il sistema visualizza *una finestra visibile* sullo schermo. Nasconde una finestra *nascosta non* disegnarla. Se una finestra è visibile, l'utente può fornire input alla finestra e visualizzarne l'output. Una finestra nascosta è disabilitata. Può elaborare messaggi dal sistema o da altre finestre ma non può elaborare input di utenti o visualizzare output. Un'applicazione imposta lo stato di visibilità di una finestra durante la creazione della finestra. In un secondo momento, l'applicazione può modificare lo stato di visibilità.

Una finestra è visibile quando lo [**stile WS \_ VISIBLE**](window-styles.md) è impostato per la finestra. Per impostazione predefinita, la [**funzione CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) crea una finestra nascosta a meno che l'applicazione non specifichi lo **stile WS \_ VISIBLE.** In genere, un'applicazione imposta lo **stile WS \_ VISIBLE** dopo aver creato una finestra per nascondere all'utente i dettagli del processo di creazione. Ad esempio, un'applicazione può mantenere nascosta una nuova finestra mentre personalizza l'aspetto della finestra. Se lo **stile WS \_ VISIBLE** è specificato in **CreateWindowEx,** il sistema invia il messaggio [**WM \_ SHOWWINDOW**](wm-showwindow.md) alla finestra dopo aver creato la finestra, ma prima di visualizzarla.

Un'applicazione può determinare se una finestra è visibile usando la [**funzione IsWindowVisible.**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) Un'applicazione può mostrare (rendere visibile) o nascondere una finestra usando la funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow), [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos), [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos)o [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) o [**SetWindowLong.**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) Queste funzioni mostrano o nascondono una finestra impostando o rimuovendo lo [**stile WS \_ VISIBLE**](window-styles.md) per la finestra. Inviano anche il [**messaggio WM \_ SHOWWINDOW**](wm-showwindow.md) alla finestra prima di mostrarlo o nasconderlo.

Quando una finestra proprietaria viene ridotta a icona, il sistema nasconde automaticamente le finestre di proprietà associate. Analogamente, quando viene ripristinata una finestra proprietaria, il sistema mostra automaticamente le finestre di proprietà associate. In entrambi i casi, il sistema invia il [**messaggio WM \_ SHOWWINDOW**](wm-showwindow.md) alle finestre di proprietà prima di nasconderle o mostrarle. In alcuni casi, un'applicazione potrebbe dover nascondere le finestre di proprietà senza dover ridurre a icona o nascondere il proprietario. In questo caso, l'applicazione usa [**la funzione ShowOwnedPopups.**](/windows/win32/api/winuser/nf-winuser-showownedpopups) Questa funzione imposta o rimuove lo [**stile WS \_ VISIBLE**](window-styles.md) per tutte le finestre di proprietà e invia il messaggio **WM \_ SHOWWINDOW** alle finestre di proprietà prima di nasconderle o mostrarle. Nascondere una finestra proprietaria non ha alcun effetto sullo stato di visibilità delle finestre di proprietà.

Quando una finestra padre è visibile, sono visibili anche le finestre figlio associate. Analogamente, quando la finestra padre è nascosta, vengono nascoste anche le relative finestre figlio. La riduzione al minimo della finestra padre non ha alcun effetto sullo stato di visibilità delle finestre figlio. ciò significa che le finestre figlio vengono ridotte a icona insieme all'elemento padre, ma lo stile [**WS \_ VISIBLE**](window-styles.md) non viene modificato.

Anche se una finestra ha lo stile [**WS \_ VISIBLE,**](window-styles.md) l'utente potrebbe non essere in grado di visualizzare la finestra sullo schermo. È possibile che altre finestre si sovrappongano completamente o che siano state spostate oltre il bordo dello schermo. Inoltre, una finestra figlio visibile è soggetta alle regole di ritaglio stabilite dalla relazione padre-figlio. Se la finestra padre della finestra non è visibile, non sarà visibile. Se la finestra padre si sposta oltre il bordo dello schermo, viene spostata anche la finestra figlio perché viene disegnata una finestra figlio rispetto all'angolo superiore sinistro dell'elemento padre. Ad esempio, un utente può spostare la finestra padre contenente la finestra figlio abbastanza lontano dal bordo dello schermo che l'utente potrebbe non essere in grado di visualizzare la finestra figlio, anche se la finestra figlio e la relativa finestra padre hanno entrambi lo stile **WS \_ VISIBLE.**

### <a name="minimized-maximized-and-restored-windows"></a>Ridotta a icona, ingrandita e ripristinata Windows

Una *finestra ingrandita* è una finestra con lo [**stile \_ WS MAXIMIZE.**](window-styles.md) Per impostazione predefinita, il sistema visualizza una finestra ingrandita in modo da riempire lo schermo oppure, in caso di una finestra figlia, l'area client della finestra padre. Anche se le dimensioni di una finestra possono essere impostate sulla stessa dimensione di una finestra ingrandita, una finestra ingrandita è leggermente diversa. Il sistema sposta automaticamente la barra del titolo della finestra nella parte superiore dello schermo o nella parte superiore dell'area client della finestra padre. Inoltre, il sistema disabilita il bordo di ridimensionamento della finestra e la funzionalità di posizionamento della finestra della barra del titolo (in modo che l'utente non possa spostare la finestra trascinando la barra del titolo).

Una *finestra ridotta* a icona è una finestra con lo stile [**WS \_ MINIMIZE.**](window-styles.md) Per impostazione predefinita, il sistema riduce una finestra alle dimensioni del pulsante della barra delle attività e la sposta sulla barra delle attività. Una *finestra ripristinata* è una finestra che è stata ripristinata alle dimensioni e alla posizione precedenti, cio? le dimensioni che aveva prima di essere ridotta a icona o ingrandita.

Se un'applicazione specifica lo stile [**WS \_ MAXIMIZE**](window-styles.md) o **WS \_ MINIMIZE** nella [**funzione CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) la finestra viene inizialmente ingrandita o ridotta a icona. Dopo aver creato una finestra, un'applicazione può usare la [**funzione CloseWindow**](/windows/win32/api/winuser/nf-winuser-closewindow) per ridurre a icona la finestra. La [**funzione ArrangeIconicWindows**](/windows/win32/api/winuser/nf-winuser-arrangeiconicwindows) dispone le icone sul desktop oppure dispone le finestre figlio ridotte a icona di una finestra padre nella finestra padre. La [**funzione OpenIcon**](/windows/win32/api/winuser/nf-winuser-openicon) ripristina le dimensioni e la posizione precedenti di una finestra ridotta a icona.

La [**funzione ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) può ridurre a icona, ingrandire o ripristinare una finestra. Può anche impostare gli stati di visibilità e attivazione della finestra. La [**funzione SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) include la stessa funzionalità di **ShowWindow**, ma può eseguire l'override delle posizioni predefinite ridotte a icona, ingrandite e ripristinate della finestra.

Le [**funzioni IsZoomed**](/windows/win32/api/winuser/nf-winuser-iszoomed) [**e IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) determinano rispettivamente se una determinata finestra è ingrandita o ridotta a icona. La [**funzione GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) recupera le posizioni ridotte a icona, ingrandite e ripristinate per la finestra e determina anche lo stato di visualizzazione della finestra.

Quando il sistema riceve un comando per ingrandire o ripristinare una finestra ridotta a icona, invia alla finestra un messaggio [**WM \_ QUERYOPEN.**](wm-queryopen.md) Se la routine della finestra restituisce **FALSE,** il sistema ignora il comando di ingrandimento o ripristino.

Il sistema imposta automaticamente le dimensioni e la posizione di una finestra ingrandita in base alle impostazioni predefinite definite dal sistema per una finestra ingrandita. Per eseguire l'override di queste impostazioni predefinite, un'applicazione può chiamare la funzione [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) o elaborare il messaggio [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) ricevuto da una finestra quando il sistema sta per ingrandire la finestra. **WM \_ GETMINMAXINFO include** un puntatore a [**una struttura MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) contenente i valori utilizzati dal sistema per impostare le dimensioni e la posizione ingrandite. La sostituzione di questi valori sostituisce le impostazioni predefinite.

## <a name="window-size-and-position"></a>Dimensioni e posizione della finestra

Le dimensioni e la posizione di una finestra sono espresse come rettangolo di delimitazione, espresso in coordinate relative alla schermata o alla finestra padre. Le coordinate di una finestra di primo livello sono relative all'angolo superiore sinistro dello schermo. le coordinate di una finestra figlio sono relative all'angolo superiore sinistro della finestra padre. Un'applicazione specifica le dimensioni iniziali e la posizione di una finestra quando crea la finestra, ma può modificare le dimensioni e la posizione della finestra in qualsiasi momento. Per altre informazioni, vedere [Forme riempite.](../gdi/filled-shapes.md)

Questa sezione contiene i seguenti argomenti:

-   [Dimensioni e posizione predefinite](#default-size-and-position)
-   [Dimensioni rilevamento](#tracking-size)
-   [Comandi di sistema](#system-commands)
-   [Funzioni di dimensione e posizione](#size-and-position-functions)
-   [Messaggi di dimensioni e posizione](#size-and-position-messages)

### <a name="default-size-and-position"></a>Dimensioni e posizione predefinite

Un'applicazione può consentire al sistema di calcolare le dimensioni iniziali o la posizione di una finestra di primo livello specificando CW \_ USEDEFAULT in [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Se l'applicazione imposta le coordinate della finestra su CW USEDEFAULT e non ha creato altre finestre di primo livello, il sistema imposta la posizione della nuova finestra rispetto all'angolo superiore sinistro dello schermo; in caso contrario, imposta la posizione relativa alla posizione della finestra di primo livello creata più di recente \_ dall'applicazione. Se i parametri width e height sono impostati su CW USEDEFAULT, il sistema calcola le \_ dimensioni della nuova finestra. Se l'applicazione ha creato altre finestre di primo livello, il sistema basa le dimensioni della nuova finestra sulle dimensioni della finestra di primo livello creata più di recente dell'applicazione. Se si specifica CW USEDEFAULT durante la creazione di una finestra popup o figlio, il sistema imposta le dimensioni minime predefinite della \_ finestra.

### <a name="tracking-size"></a>Dimensioni rilevamento

Il sistema mantiene una dimensione di rilevamento minima e massima per una finestra dello stile [**\_ WS THICKFRAME.**](window-styles.md) Una finestra con questo stile ha un bordo di ridimensionamento. Le *dimensioni minime di rilevamento* sono le dimensioni minime della finestra che è possibile produrre trascinando il bordo di ridimensionamento della finestra. Analogamente, le dimensioni *massime di rilevamento* sono le dimensioni della finestra più grandi che è possibile produrre trascinando il bordo di ridimensionamento.

Le dimensioni di rilevamento minimo e massimo di una finestra vengono impostate su valori predefiniti definiti dal sistema quando il sistema crea la finestra. Un'applicazione può individuare le impostazioni predefinite ed eseguirne l'override elaborando il [**messaggio WM \_ GETMINMAXINFO.**](wm-getminmaxinfo.md) Per altre informazioni, vedere [Messaggi di dimensioni e posizione](#size-and-position-messages).

### <a name="system-commands"></a>Comandi di sistema

Un'applicazione con un menu finestra può modificare le dimensioni e la posizione di tale finestra inviando comandi di sistema. I comandi di sistema vengono generati quando l'utente sceglie i comandi dal menu della finestra. Un'applicazione può emulare l'azione dell'utente inviando [**un messaggio \_ SYSCOMMAND WM**](../menurc/wm-syscommand.md) alla finestra. I comandi di sistema seguenti influiscono sulle dimensioni e sulla posizione di una finestra.



| Comando      | Descrizione                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SC \_ CLOSE    | Chiude la finestra. Questo comando invia un [**messaggio WM \_ CLOSE**](wm-close.md) alla finestra. La finestra esegue tutti i passaggi necessari per pulire e distruggere se stessa. |
| \_INGRANDISCI SC | Ingrandisce la finestra.                                                                                                                                                |
| RIDUZIONE A \_ ICONA SC | Riduce a icona la finestra.                                                                                                                                                |
| SC \_ MOVE     | Sposta la finestra.                                                                                                                                                    |
| SC \_ RESTORE  | Ripristina le dimensioni e la posizione precedenti di una finestra ridotta a icona o ingrandita.                                                                                          |
| DIMENSIONI \_ SC     | Avvia un comando size. Per modificare le dimensioni della finestra, usare il mouse o la tastiera.                                                                                  |



 

### <a name="size-and-position-functions"></a>Funzioni di dimensione e posizione

Dopo aver creato una finestra, un'applicazione può impostare le dimensioni o la posizione della finestra chiamando una delle diverse funzioni, tra cui [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement), [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow), [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)e [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos). **SetWindowPlacement imposta** la posizione ridotta a icona di una finestra, la posizione ingrandita, le dimensioni ripristinate e la posizione e lo stato di visualizzazione. Le **funzioni MoveWindow** **e SetWindowPos** sono simili. entrambi impostano le dimensioni o la posizione di una singola finestra dell'applicazione. La **funzione SetWindowPos** include un set di flag che influiscono sullo stato di visualizzazione della finestra. **MoveWindow** non include questi flag. Usare le funzioni [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos), **DeferWindowPos** e [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos) per impostare contemporaneamente la posizione di diverse finestre, tra cui le dimensioni, la posizione, la posizione nell'ordine z e lo stato di visualizzazione.

Un'applicazione può recuperare le coordinate del rettangolo di delimitazione di una finestra usando la [**funzione GetWindowRect.**](/windows/win32/api/winuser/nf-winuser-getwindowrect) **GetWindowRect** riempie una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) con le coordinate degli angoli superiore sinistro e inferiore destro della finestra. Le coordinate sono relative all'angolo superiore sinistro dello schermo, anche per una finestra figlio. La [**funzione ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) o [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) esegue il mapping delle coordinate dello schermo del rettangolo di delimitazione di una finestra figlio alle coordinate relative all'area client della finestra padre.

La [**funzione GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) recupera le coordinate dell'area client di una finestra. **GetClientRect** riempie una struttura [**RECT**](/previous-versions//dd162897(v=vs.85)) con le coordinate degli angoli superiore sinistro e inferiore destro dell'area client, ma le coordinate sono relative all'area client stessa. Ciò significa che le coordinate dell'angolo superiore sinistro di un'area client sono sempre (0,0) e le coordinate dell'angolo inferiore destro sono la larghezza e l'altezza dell'area client.

La [**funzione CascadeWindows**](/windows/win32/api/winuser/nf-winuser-cascadewindows) propaga le finestre sul desktop o sovrappone le finestre figlio della finestra padre specificata. La [**funzione TileWindows**](/windows/win32/api/winuser/nf-winuser-tilewindows) affianca le finestre sul desktop o affianca le finestre figlio della finestra padre specificata.

### <a name="size-and-position-messages"></a>Messaggi di dimensioni e posizione

Il sistema invia il [**messaggio WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) a una finestra la cui dimensione o posizione sta per cambiare. Ad esempio, il messaggio viene inviato  quando  l'utente fa clic su Sposta o Dimensioni dal menu della finestra o fa clic sul bordo di ridimensionamento o sulla barra del titolo. il messaggio viene inviato anche quando un'applicazione chiama [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) per spostare o ridimensionare la finestra. **WM \_ GETMINMAXINFO** include un puntatore a una struttura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) contenente le dimensioni e la posizione ingrandite predefinite per la finestra, nonché le dimensioni di rilevamento minime e massime predefinite. Un'applicazione può eseguire l'override delle impostazioni predefinite elaborando **WM \_ GETMINMAXINFO** e impostando i membri appropriati di **MINMAXINFO**. Una finestra deve avere lo [**stile \_ WS THICKFRAME**](window-styles.md) o **WS \_ CAPTION** per ricevere **WM \_ GETMINMAXINFO**. Una finestra con lo **stile \_ WS THICKFRAME** riceve questo messaggio durante il processo di creazione della finestra, nonché quando viene spostata o ridimensionata.

Il sistema invia il [**messaggio WM \_ WINDOWPOSCHANGING**](wm-windowposchanging.md) a una finestra la cui dimensione, posizione, posizione nell'ordine z o stato di visualizzazione sta per cambiare. Questo messaggio include un puntatore a una struttura [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) che specifica le nuove dimensioni, posizione, posizione nell'ordine z e stato di visualizzazione della finestra. Impostando i membri di **WINDOWPOS**, un'applicazione può influire sulle nuove dimensioni, posizione e aspetto della finestra.

Dopo aver modificato le dimensioni, la posizione, la posizione nell'ordine z o lo stato di visualizzazione di una finestra, il sistema invia il messaggio [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) alla finestra. Questo messaggio include un puntatore a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) che informa la finestra delle nuove dimensioni, posizione, posizione nell'ordine z e stato di visualizzazione. L'impostazione dei membri **della struttura WINDOWPOS** passata con **WM \_ WINDOWPOSCHANGED** non ha alcun effetto sulla finestra. Una finestra che deve elaborare i messaggi WM SIZE e [**WM \_ MOVE**](wm-move.md) deve passare **WM \_ WINDOWPOSCHANGED** alla funzione [**DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) In caso contrario, il sistema non invia messaggi **WM \_** [**\_ SIZE**](wm-size.md) e **WM \_ MOVE** alla finestra.

Il sistema invia il [**messaggio \_ WM NCCALCSIZE**](wm-nccalcsize.md) a una finestra quando la finestra viene creata o ridimensionata. Il sistema usa il messaggio per calcolare le dimensioni dell'area client di una finestra e la posizione dell'area client rispetto all'angolo superiore sinistro della finestra. In genere, una finestra passa questo messaggio alla routine della finestra predefinita. Tuttavia, questo messaggio può essere utile nelle applicazioni che personalizzano l'area non client di una finestra o mantengono parti dell'area client quando la finestra viene ridimensionata. Per altre informazioni, vedere [Disegno e disegno.](../gdi/painting-and-drawing.md)

## <a name="window-animation"></a>Animazione finestra

È possibile produrre effetti speciali quando si visualizzano o nascondono finestre usando la [**funzione AnimateWindow.**](/windows/win32/api/winuser/nf-winuser-animatewindow) Quando la finestra viene animata in questo modo, il sistema scorrerà, scorrerà o dissolvenza della finestra, a seconda dei flag specificati in una chiamata a **AnimateWindow.**

Per impostazione predefinita, il sistema usa *l'animazione a rullo*. Con questo effetto, la finestra appare aperta (che mostra la finestra) o chiusa (nascondendo la finestra). È possibile usare il *parametro dwFlags* per specificare se la finestra viene visualizzata orizzontalmente, verticalmente o diagonalmente.

Quando si specifica il flag **AW \_ SLIDE,** il sistema usa l'animazione *a scorrimento*. Con questo effetto, la finestra viene visualizzata (che mostra la finestra) o esce dalla visualizzazione (nascondendo la finestra). È possibile usare il *parametro dwFlags* per specificare se la finestra scorre orizzontalmente, verticalmente o diagonalmente.

Quando si specifica il flag **AW \_ BLEND,** il sistema usa una *dissolvenza con alpha blended.*

È anche possibile usare il flag **AW \_ CENTER** per fare in modo che una finestra venga compressa verso l'interno o espansa verso l'esterno.

## <a name="window-layout-and-mirroring"></a>Layout e mirroring delle finestre

Il layout della finestra definisce la disposizione di testo e Windows Graphics Device Interface (GDI) in una finestra o in un contesto di dispositivo (DC). Alcune lingue, ad esempio inglese, francese e tedesco, richiedono un layout da sinistra a destra. Altre lingue, ad esempio arabo ed ebraico, richiedono un layout da destra a sinistra (RTL). Il layout della finestra si applica al testo, ma influisce anche sugli altri elementi GDI della finestra, tra cui bitmap, icone, posizione dell'origine, pulsanti, controlli albero a cascata e se la coordinata orizzontale aumenta man mano che si passa a sinistra o a destra. Ad esempio, dopo che un'applicazione ha impostato il layout RTL, l'origine viene posizionata sul bordo destro della finestra o del dispositivo e il numero che rappresenta la coordinata orizzontale aumenta man mano che ci si sposta a sinistra. Tuttavia, non tutti gli oggetti sono interessati dal layout di una finestra. Ad esempio, il layout per finestre di dialogo, finestre di messaggio e contesti di dispositivo non associati a una finestra, ad esempio i controller di dominio metafile e stampanti, deve essere gestito separatamente. Le specifiche sono indicate più avanti in questo argomento.

Le funzioni finestra consentono di specificare o modificare il layout della finestra nelle versioni in arabo ed ebraico Windows. Si noti che la modifica a un layout RTL (noto anche come mirroring) non è supportata per le finestre con lo stile [CS \_ OWNDC](about-window-classes.md) o per un controller di dominio con la modalità grafica GM \_ ADVANCED.

Per impostazione predefinita, il layout della finestra è da sinistra a destra(LTR). Per impostare il layout della finestra RTL, [**chiamare CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) con lo stile **WS \_ EX \_ LAYOUTRTL.** Inoltre, per impostazione predefinita, una finestra figlio, ovvero una finestra creata con lo stile [**WS \_ CHILD**](window-styles.md) e con un parametro *hWnd* padre valido nella chiamata a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o **CreateWindowEx,** ha lo stesso layout del relativo elemento padre. Per disabilitare l'ereditarietà del mirroring in tutte le finestre figlio, specificare **WS \_ EX \_ NOINHERITLAYOUT** nella chiamata **a CreateWindowEx.** Si noti che il mirroring non viene ereditato dalle finestre di proprietà (quelle create senza lo stile **WS \_ CHILD)** o quelle create con il parametro *hWnd* padre in **CreateWindowEx** impostato su **NULL.** Per disabilitare l'ereditarietà del mirroring per una singola finestra, elaborare il messaggio [**\_ WM NCCREATE**](wm-nccreate.md) con [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) per disattivare il flag **WS EX \_ \_ LAYOUTRTL.** Questa elaborazione si aggiunge a qualsiasi altra elaborazione necessaria. Nel frammento di codice seguente viene illustrato come eseguire questa operazione.


```
SetWindowLong (hWnd, 
               GWL_EXSTYLE, 
               GetWindowLong(hWnd,GWL_EXSTYLE) & ~WS_EX_LAYOUTRTL))
```



È possibile impostare il layout predefinito su RTL chiamando [**SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout)(LAYOUT \_ RTL). Tutte le finestre create dopo la chiamata verranno rispecchiate, ma le finestre esistenti non saranno interessate. Per disattivare il mirroring predefinito, **chiamare SetProcessDefaultLayout**(0).

Si noti che [**SetProcessDefaultLayout rispecchia**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout) i controller di dominio solo delle finestre con mirroring. Per eseguire il mirroring di qualsiasi controller di [**dominio, chiamare SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(hdc, LAYOUT \_ RTL). Per altre informazioni, vedere la discussione sul mirroring dei contesti di dispositivo non associati alle finestre, disponibile più avanti in questo argomento.

Anche le bitmap e le icone in una finestra speculare vengono rispecchiate per impostazione predefinita. Tuttavia, non è necessario eseguire il mirroring di tutti questi elementi. Ad esempio, quelli con testo, un logo aziendale o un orologio analogico non devono essere rispecchiati. Per disabilitare il mirroring delle bitmap, chiamare [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) con il \_ bit LAYOUT BITMAPORIENTATIONPRESERVED impostato in *dwLayout*. Per disabilitare il mirroring in un controller di dominio, **chiamare SetLayout**(hdc, 0).

Per eseguire una query sul layout predefinito corrente, [**chiamare GetProcessDefaultLayout.**](/windows/win32/api/winuser/nf-winuser-getprocessdefaultlayout) In caso di esito positivo, *pdwDefaultLayout contiene* LAYOUT \_ RTL o 0. Per eseguire una query delle impostazioni di layout del contesto di dispositivo, [**chiamare GetLayout**](/windows/win32/api/wingdi/nf-wingdi-getlayout). In caso di esito positivo, **GetLayout** restituisce un **valore DWORD** che indica le impostazioni di layout in base alle impostazioni dei bit LAYOUT RTL e \_ LAYOUT \_ BITMAPORIENTATIONPRESERVED.

Dopo aver creato una finestra, è possibile modificare il layout usando la [**funzione SetWindowLong.**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) Ad esempio, questa operazione è necessaria quando l'utente modifica la lingua dell'interfaccia utente di una finestra esistente da arabo o ebraico a tedesco. Tuttavia, quando si modifica il layout di una finestra esistente, è necessario invalidare e aggiornare la finestra per garantire che il contenuto della finestra sia disegnato sullo stesso layout. L'esempio di codice seguente è il codice di esempio che modifica il layout della finestra in base alle esigenze:


```
// Using ANSI versions of GetWindowLong and SetWindowLong because Unicode
// is not needed for these calls

lExStyles = GetWindowLongA(hWnd, GWL_EXSTYLE);

// Check whether new layout is opposite the current layout
if (!!(pLState -> IsRTLLayout) != !!(lExStyles & WS_EX_LAYOUTRTL))
{
    // the following lines will update the window layout

    lExStyles ^= WS_EX_LAYOUTRTL;        // toggle layout
    SetWindowLongA(hWnd, GWL_EXSTYLE, lExStyles);
    InvalidateRect(hWnd, NULL, TRUE);    // to update layout in the client area
}
```



Nel mirroring, è consigliabile pensare in termini di "vicino" e "lontano" anziché "sinistro" e "destro". La mancata riuscita di questa operazione può causare problemi. Una procedura di codifica comune che causa problemi in una finestra con mirroring si verifica quando si esegue il mapping tra le coordinate dello schermo e le coordinate del client. Ad esempio, le applicazioni usano spesso codice simile al seguente per posizionare un controllo in una finestra:


```
// DO NOT USE THIS IF APPLICATION MIRRORS THE WINDOW

// get coordinates of the window in screen coordinates
GetWindowRect(hControl, (LPRECT) &rControlRect);  

// map screen coordinates to client coordinates in dialog
ScreenToClient(hDialog, (LPPOINT) &rControlRect.left); 
ScreenToClient(hDialog, (LPPOINT) &rControlRect.right);
```



Ciò causa problemi di mirroring perché il bordo sinistro del rettangolo diventa il bordo destro in una finestra con mirroring e viceversa. Per evitare questo problema, sostituire le [**chiamate ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) con una chiamata a [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) come indicato di seguito:


```
// USE THIS FOR MIRRORING

GetWindowRect(hControl, (LPRECT) &rControlRect);
MapWindowPoints(NULL, hDialog, (LPPOINT) &rControlRect, 2)
```



Questo codice funziona perché, nelle piattaforme che supportano il mirroring, [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) viene modificato per scambiare le coordinate del punto sinistro e destro quando si esegue il mirroring della finestra client. Per altre informazioni, vedere la sezione Osservazioni di **MapWindowPoints.**

Un'altra pratica comune che può causare problemi nelle finestre con mirroring è il posizionamento di oggetti in una finestra client usando offset nelle coordinate dello schermo anziché coordinate client. Ad esempio, il codice seguente usa la differenza nelle coordinate dello schermo come posizione x nelle coordinate del client per posizionare un controllo in una finestra di dialogo.


```
// OK if LTR layout and mapping mode of client is MM_TEXT,
// but WRONG for a mirrored dialog 

RECT rdDialog;
RECT rcControl;

HWND hControl = GetDlgItem(hDlg, IDD_CONTROL);
GetWindowRect(hDlg, &rcDialog);             // gets rect in screen coordinates
GetWindowRect(hControl, &rcControl);
MoveWindow(hControl,
           rcControl.left - rcDialog.left,  // uses x position in client coords
           rcControl.top - rcDialog.top,
           nWidth,
           nHeight,
           FALSE);
```



Questo codice è valido quando la finestra di dialogo ha un layout da sinistra a destra e la modalità di mapping del client è MM TEXT, perché la nuova posizione x nelle coordinate del client corrisponde alla differenza nei bordi sinistro del controllo e della finestra di dialogo nelle coordinate dello \_ schermo. Tuttavia, in una finestra di dialogo con mirroring, sinistra e destra sono invertte, quindi è consigliabile usare [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) come indicato di seguito:


```
RECT rcDialog;
RECT rcControl;

HWND hControl - GetDlgItem(hDlg, IDD_CONTROL);
GetWindowRect(hControl, &rcControl);

// MapWindowPoints works correctly in both mirrored and non-mirrored windows.
MapWindowPoints(NULL, hDlg, (LPPOINT) &rcControl, 2);

// Now rcControl is in client coordinates.
MoveWindow(hControl, rcControl.left, rcControl.top, nWidth, nHeight, FALSE)
```



### <a name="mirroring-dialog-boxes-and-message-boxes"></a>Finestre di dialogo e finestre di messaggio per il mirroring

Le finestre di dialogo e le finestre di messaggio non ereditano il layout, pertanto è necessario impostare il layout in modo esplicito. Per eseguire il mirroring di una finestra di messaggio, [**chiamare MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) o [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) con **\_ l'opzione MB RTLREADING.** Per eseguire il layout di una finestra di dialogo da destra a sinistra, usare lo stile esteso WS EX LAYOUTRTL nella struttura del modello di finestra di dialogo \_ \_ [**DLGTEMPLATEEX**](../dlgbox/dlgtemplateex.md). Le finestre delle proprietà sono un caso speciale di finestre di dialogo. Ogni scheda viene considerata come una finestra di dialogo separata, pertanto è necessario includere lo stile \_ WS EX LAYOUTRTL in ogni scheda di cui si vuole eseguire \_ il mirroring.

### <a name="mirroring-device-contexts-not-associated-with-a-window"></a>Mirroring dei contesti di dispositivo non associati a una finestra

I controller di dominio non associati a una finestra, ad esempio i controller di dominio metafile o stampanti, non ereditano il layout, pertanto è necessario impostare il layout in modo esplicito. Per modificare il layout del contesto di dispositivo, usare la [**funzione SetLayout.**](/windows/win32/api/wingdi/nf-wingdi-setlayout)

La [**funzione SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) viene usata raramente con le finestre. In genere, le finestre ricevono un controller di dominio associato solo durante l'elaborazione [**di un messaggio WM \_ PAINT.**](../gdi/wm-paint.md) In alcuni casi, un programma crea un controller di dominio per una finestra chiamando [**GetDC**](/windows/win32/api/winuser/nf-winuser-getdc). In entrambi i modi, il layout iniziale per il controller di dominio viene impostato da [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint) o **GetDC** in base al flag WS \_ EX \_ LAYOUTRTL della finestra.

I valori restituiti da [**GetWindowOrgEx,**](/windows/win32/api/wingdi/nf-wingdi-getwindoworgex) [**GetWindowExtEx,**](/windows/win32/api/wingdi/nf-wingdi-getwindowextex) [**GetViewportOrgEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportorgex) e [**GetViewportExtEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportextex) non sono interessati dalla chiamata [**a SetLayout.**](/windows/win32/api/wingdi/nf-wingdi-setlayout)

Quando il layout è RTL, [**GetMapMode**](/windows/win32/api/wingdi/nf-wingdi-getmapmode) restituirà MM \_ ANISOTROP anziché MM \_ TEXT. La [**chiamata di SetMapMode**](/windows/win32/api/wingdi/nf-wingdi-setmapmode) con MM TEXT funzionerà correttamente. Viene interessato \_ solo il valore restituito da **GetMapMode.** Analogamente, la chiamata [**a SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(hdc, LAYOUT RTL) quando la modalità di mapping è MM TEXT fa sì che la modalità di mapping segnalata cambi \_ in MM \_ \_ ANISO STANDBY.

## <a name="window-destruction"></a>Distruzione delle finestre

In generale, un'applicazione deve eliminare tutte le finestre create. A tale scopo, usa la [**funzione DestroyWindow.**](/windows/win32/api/winuser/nf-winuser-destroywindow) Quando una finestra viene distrutta, il sistema nasconde la finestra, se è visibile, e quindi rimuove tutti i dati interni associati alla finestra. In questo modo viene invalidato l'handle di finestra, che non può più essere usato dall'applicazione.

Un'applicazione elimina molte delle finestre create subito dopo averle create. Ad esempio, un'applicazione in genere elimina una finestra di dialogo non appena l'applicazione dispone di un input sufficiente da parte dell'utente per continuare l'attività. Un'applicazione elimina infine la finestra principale dell'applicazione (prima di terminare).

Prima di eliminare una finestra, un'applicazione deve salvare o rimuovere tutti i dati associati alla finestra e rilasciare tutte le risorse di sistema allocate per la finestra. Se l'applicazione non rilascia le risorse, il sistema libera tutte le risorse non liberate dall'applicazione.

L'eliminazione di una finestra non influisce sulla classe della finestra da cui viene creata la finestra. È comunque possibile creare nuove finestre usando tale classe e tutte le finestre esistenti della classe continuano a funzionare. L'eliminazione di una finestra elimina anche le finestre discendenti della finestra. La [**funzione DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) invia prima [**un messaggio DESTROY WM \_**](wm-destroy.md) alla finestra, quindi alle finestre figlio e alle finestre discendenti. In questo modo, vengono distrutte anche tutte le finestre discendenti della finestra da eliminare.

Una finestra con un menu di finestra riceve un messaggio [**WM \_ CLOSE**](wm-close.md) quando l'utente fa clic su **Chiudi.** Elaborando questo messaggio, un'applicazione può richiedere conferma all'utente prima di eliminare la finestra. Se l'utente conferma che la finestra deve essere distrutta, l'applicazione può chiamare la [**funzione DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) per eliminare la finestra.

Se la finestra da eliminare è la finestra attiva, gli stati attivo e attivo vengono trasferiti in un'altra finestra. La finestra che diventa la finestra attiva è la finestra successiva, come determinato dalla combinazione di tasti ALT+ESC. La nuova finestra attiva determina quindi quale finestra riceve lo stato attivo della tastiera.

 

 
