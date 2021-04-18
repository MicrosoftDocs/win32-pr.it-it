---
description: In questa panoramica vengono illustrate le funzionalità di Windows, ad esempio tipi di finestra, Stati, dimensioni e posizione.
ms.assetid: 8318c22f-85a2-490e-8233-ee1e234890d9
title: Funzionalità delle finestre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228c6b4ab59102cae38a248935fbbad32198f2e0
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/25/2021
ms.locfileid: "106333991"
---
# <a name="window-features"></a>Funzionalità delle finestre

In questa panoramica vengono illustrate le funzionalità di Windows, ad esempio tipi di finestra, Stati, dimensioni e posizione.

-   [Tipi di finestre](#window-types)
    -   [Finestre sovrapposte](#overlapped-windows)
    -   [Finestre popup](#pop-up-windows)
    -   [Finestre figlio](#child-windows)
        -   [Posizionamento](#positioning)
        -   [Ritaglio](#clipping)
        -   [Relazione con la finestra padre](#relationship-to-parent-window)
        -   [Messaggi](#size-and-position-messages)
    -   [Finestre sovrapposte](#layered-windows)
    -   [Finestre solo messaggio](#message-only-windows)
-   [Relazioni tra finestre](#window-relationships)
    -   [Finestre in primo piano e in background](#foreground-and-background-windows)
    -   [Finestre di proprietà](#owned-windows)
    -   [Ordine Z](#z-order)
-   [Mostra stato finestra](#window-show-state)
    -   [Finestra attiva](#active-window)
    -   [Finestre disabilitate](#disabled-windows)
    -   [Visibilità della finestra](#window-visibility)
    -   [Finestre ridotte a icona, ingrandite e ripristinate](#minimized-maximized-and-restored-windows)
-   [Dimensioni e posizione della finestra](#window-size-and-position)
    -   [Dimensioni e posizione predefinite](#default-size-and-position)
    -   [Dimensioni del rilevamento](#tracking-size)
    -   [Comandi di sistema](#system-commands)
    -   [Funzioni di dimensioni e posizioni](#size-and-position-functions)
    -   [Messaggi di dimensioni e posizione](#size-and-position-messages)
-   [Animazione finestra](#window-animation)
-   [Layout della finestra e mirroring](#window-layout-and-mirroring)
    -   [Finestre di dialogo di mirroring e finestre di messaggio](#mirroring-dialog-boxes-and-message-boxes)
    -   [Il mirroring dei contesti di dispositivo non è associato a una finestra](#mirroring-device-contexts-not-associated-with-a-window)
-   [Distruzione finestra](#window-destruction)

## <a name="window-types"></a>Tipi di finestre

Questa sezione contiene i seguenti argomenti che descrivono i tipi di finestra.

-   [Finestre sovrapposte](#overlapped-windows)
-   [Finestre popup](#pop-up-windows)
-   [Finestre figlio](#child-windows)
-   [Finestre sovrapposte](#layered-windows)
-   [Finestre solo messaggio](#message-only-windows)

### <a name="overlapped-windows"></a>Finestre sovrapposte

Una *finestra sovrapposta* è una finestra di primo livello (finestra non figlio) con una barra del titolo, un bordo e un'area client; è destinato a fungere da finestra principale di un'applicazione. Può anche avere un menu finestra, ridurre a icona e ingrandire i pulsanti e le barre di scorrimento. Una finestra sovrapposta utilizzata come finestra principale include in genere tutti questi componenti.

Specificando lo stile [**WS \_ OVERLAPPED**](window-styles.md) o **WS \_ OVERLAPPEDWINDOW** nella funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , un'applicazione crea una finestra sovrapposta. Se si utilizza lo stile **WS \_ sovrapposto** , la finestra dispone di una barra del titolo e di un bordo. Se si usa lo stile **WS \_ OVERLAPPEDWINDOW** , la finestra ha una barra del titolo, il bordo di ridimensionamento, il menu finestra e i pulsanti Riduci a icona e Ingrandisci.

### <a name="pop-up-windows"></a>Finestre popup

Una *finestra popup* è un tipo speciale di finestra sovrapposta usata per finestre di dialogo, finestre di messaggio e altre finestre temporanee visualizzate all'esterno della finestra principale di un'applicazione. Le barre del titolo sono facoltative per le finestre popup; in caso contrario, le finestre popup sono le stesse delle finestre sovrapposte dello stile [**WS \_ OVERLAPPED**](window-styles.md) .

Si crea una finestra popup specificando lo stile [**WS \_ popup**](window-styles.md) in [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Per includere una barra del titolo, specificare lo stile della **\_ didascalia WS** . Usare lo stile **WS \_ POPUPWINDOW** per creare una finestra popup con un bordo e un menu finestra. Lo stile della **\_ didascalia WS** deve essere combinato con lo stile **WS \_ POPUPWINDOW** per rendere visibile il menu finestra.

### <a name="child-windows"></a>Finestre figlio

Una *finestra figlio* ha lo stile [**WS \_ child**](window-styles.md) ed è confinata all'area client della relativa finestra padre. Un'applicazione usa in genere le finestre figlio per dividere l'area client di una finestra padre in aree funzionali. Per creare una finestra figlio, è necessario specificare lo stile **WS \_ figlio** nella funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

Una finestra figlio deve avere una finestra padre. La finestra padre può essere una finestra sovrapposta, una finestra popup o anche un'altra finestra figlio. È possibile specificare la finestra padre quando si chiama [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Se si specifica lo [**stile \_ figlio WS**](window-styles.md) in **CreateWindowEx** ma non si specifica una finestra padre, il sistema non creerà la finestra.

Una finestra figlio ha un'area client ma non altre funzionalità, a meno che non vengano richieste in modo esplicito. Un'applicazione può richiedere una barra del titolo, un menu finestra, i pulsanti Riduci a icona e Ingrandisci, un bordo e le barre di scorrimento per una finestra figlio, ma una finestra figlio non può disporre di un menu. Se l'applicazione specifica un handle di menu, quando registra la classe della finestra figlio o crea la finestra figlio, l'handle di menu viene ignorato. Se non viene specificato alcuno stile del bordo, il sistema crea una finestra senza bordi. Un'applicazione può usare finestre figlio senza bordi per dividere l'area client di una finestra padre mantenendo le divisioni invisibili per l'utente.

In questa sezione vengono illustrati gli aspetti seguenti delle finestre figlio:

-   [Posizionamento](#positioning)
-   [Ritaglio](#clipping)
-   [Relazione con la finestra padre](#relationship-to-parent-window)
-   [Messaggi](#size-and-position-messages)

#### <a name="positioning"></a>Posizionamento

Il sistema posiziona sempre una finestra figlio rispetto all'angolo superiore sinistro dell'area client della finestra padre. Nessuna parte di una finestra figlio viene mai visualizzata all'esterno dei bordi della finestra padre. Se un'applicazione crea una finestra figlio che è più grande della finestra padre o posiziona una finestra figlio in modo che parte o tutte le finestre figlio si estendano oltre i bordi dell'elemento padre, il sistema Ritaglia la finestra figlio; ovvero la parte al di fuori dell'area client della finestra padre non viene visualizzata. Le azioni che interessano la finestra padre possono influire anche sulla finestra figlio, come indicato di seguito.



| Finestra padre | Finestra figlio                                                                                                             |
|---------------|--------------------------------------------------------------------------------------------------------------------------|
| Eliminata     | Distrutto prima che la finestra padre venga distrutta.                                                                         |
| Nascosto        | Nascosto prima che la finestra padre sia nascosta. Una finestra figlio è visibile solo quando la finestra padre è visibile.             |
| Spostato         | Spostato con l'area client della finestra padre. La finestra figlio è responsabile del disegno dell'area client dopo lo spostamento. |
| Illustrato         | Viene visualizzato dopo la visualizzazione della finestra padre.                                                                                  |



 

#### <a name="clipping"></a>Ritaglio

Il sistema non Ritaglia automaticamente una finestra figlio dall'area client della finestra padre. Ciò significa che la finestra padre viene disegnata sulla finestra figlio se esegue un disegno nella stessa posizione della finestra figlio. Tuttavia, il sistema Ritaglia la finestra figlio dall'area client della finestra padre se la finestra padre ha lo stile [**WS \_ CLIPCHILDREN**](window-styles.md) . Se la finestra figlio viene ritagliata, la finestra padre non può essere sottolineata.

Una finestra figlio può sovrapporsi ad altre finestre figlio nella stessa area client. Una finestra figlio che condivide la stessa finestra padre di una o più finestre figlio è detta finestra di *pari livello*. Le finestre di pari livello possono essere disegnate nell'area client dell'altra, a meno che una delle finestre figlio non disponga dello stile [**WS \_ CLIPSIBLINGS**](window-styles.md) . Se una finestra figlio ha questo stile, qualsiasi parte della finestra di pari livello che si trova all'interno della finestra figlio viene ritagliata.

Se una finestra dispone dello stile [**WS \_ CLIPCHILDREN**](window-styles.md) o **WS \_ CLIPSIBLINGS** , si verificherà una lieve perdita di prestazioni. Poiché ogni finestra occupa risorse di sistema, un'applicazione non deve utilizzare le finestre figlio in modo indiscriminato. Per ottenere prestazioni ottimali, un'applicazione che deve suddividere logicamente la finestra principale deve eseguire questa operazione nella procedura della finestra principale anziché usando le finestre figlio.

#### <a name="relationship-to-parent-window"></a>Relazione con la finestra padre

Un'applicazione può modificare la finestra padre di una finestra figlio esistente chiamando la funzione [**padre**](/windows/win32/api/winuser/nf-winuser-setparent) . In questo caso, il sistema rimuove la finestra figlio dall'area client della finestra padre precedente e la sposta nell'area client della nuova finestra padre. Se l' **elemento padre** specifica un handle **null** , la finestra del desktop diventa la nuova finestra padre. In questo caso, la finestra figlio viene disegnata sul desktop, all'esterno dei bordi di qualsiasi altra finestra. La funzione [**GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) recupera un handle per la finestra padre di una finestra figlio.

La finestra padre rilascia una parte dell'area client a una finestra figlio e la finestra figlio riceve tutti gli input da quest'area. Non è necessario che la classe della finestra sia la stessa per ciascuna delle finestre figlio della finestra padre. Ciò significa che un'applicazione può riempire una finestra padre con finestre figlio che hanno un aspetto diverso ed eseguono attività diverse. Una finestra di dialogo, ad esempio, può contenere molti tipi di controlli, ognuno dei quali è una finestra figlio che accetta tipi diversi di dati dell'utente.

Una finestra figlio ha una sola finestra padre, ma un padre può avere un numero qualsiasi di finestre figlio. Ogni finestra figlio può, a sua volta, avere finestre figlio. In questa catena di finestre ogni finestra figlio viene chiamata finestra discendente della finestra padre originale. Per individuare se una determinata finestra è una finestra figlio o una finestra discendente di una determinata finestra padre, un'applicazione utilizza la funzione [**figlio**](/windows/win32/api/winuser/nf-winuser-ischild) .

La funzione [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) enumera le finestre figlio di una finestra padre. Quindi, **EnumChildWindows** passa l'handle a ogni finestra figlio a una funzione di callback definita dall'applicazione. Vengono inoltre enumerate le finestre discendenti della finestra padre specificata.

#### <a name="messages"></a>Messaggi

Il sistema passa i messaggi di input della finestra figlio direttamente alla finestra figlio; i messaggi non vengono passati tramite la finestra padre. L'unica eccezione è rappresentata dal caso in cui la finestra figlio è stata disabilitata dalla funzione [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) . In questo caso, il sistema passa tutti i messaggi di input che verrebbero invece passati alla finestra padre. Ciò consente alla finestra padre di esaminare i messaggi di input e di abilitare la finestra figlio, se necessario.

Una finestra figlio può avere un identificatore di tipo Integer univoco. Gli identificatori della finestra figlio sono importanti quando si utilizzano le finestre di controllo. Un'applicazione indirizza l'attività di un controllo tramite l'invio di messaggi. L'applicazione usa l'identificatore della finestra figlio del controllo per indirizzare i messaggi al controllo. Inoltre, un controllo Invia messaggi di notifica alla relativa finestra padre. Un messaggio di notifica include l'identificatore della finestra figlio del controllo, utilizzato dall'elemento padre per identificare il controllo che ha inviato il messaggio. Un'applicazione specifica l'identificatore della finestra figlio per altri tipi di finestre figlio impostando il parametro *HMENU* della funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) su un valore anziché un handle di menu.

### <a name="layered-windows"></a>Finestre sovrapposte

L'uso di una finestra sovrapposta può migliorare significativamente le prestazioni e gli effetti visivi per una finestra con una forma complessa, anima la forma o desidera usare effetti di fusione alfa. Il sistema compone e ridisegna automaticamente le finestre a livelli e le finestre delle applicazioni sottostanti. Di conseguenza, il rendering delle finestre sovrapposte viene eseguito in modo uniforme, senza lo sfarfallio tipico delle aree di finestra complesse. Inoltre, le finestre a livelli possono essere parzialmente trasparenti, ovvero con alpha blending.

Per creare una finestra sovrapposta, specificare lo stile della finestra estesa di **WS- \_ \_ Layered** quando si chiama la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) oppure chiamare la funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) per impostare WS-only su più **\_ \_ livelli** dopo la creazione della finestra. Dopo la chiamata a **CreateWindowEx** , la finestra sovrapposta non diventerà visibile fino a quando non viene chiamata la funzione [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) o [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow) per questa finestra.

> [!Note]  
> A partire da Windows 8, **WS \_ ex \_ Layered** può essere usato con le finestre figlio e le finestre di primo livello. Le versioni precedenti di Windows supportano il **\_ \_ livello WS ex** solo per le finestre di primo livello.

 

Per impostare il livello di opacità o la chiave di colore della trasparenza per una determinata finestra sovrapposta, chiamare [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes). Dopo la chiamata, il sistema potrebbe ancora chiedere alla finestra di disegnare quando la finestra viene visualizzata o ridimensionata. Tuttavia, poiché il sistema archivia l'immagine di una finestra a più livelli, il sistema non chiederà alla finestra di disegnare se le parti vengono rivelate in seguito a spostamenti relativi della finestra sul desktop. Le applicazioni legacy non devono ristrutturare il codice di disegno se desiderano aggiungere effetti di traslucidità o trasparenza per una finestra, perché il sistema reindirizza il disegno di Windows che ha chiamato **SetLayeredWindowAttributes** nella memoria fuori schermo e lo ricompone per ottenere l'effetto desiderato.

Per animazioni più veloci ed efficienti o se è necessario un Alpha per pixel, chiamare [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow). **UpdateLayeredWindow** deve essere usato principalmente quando l'applicazione deve fornire direttamente la forma e il contenuto di una finestra sovrapposta, senza usare il meccanismo di reindirizzamento fornito dal sistema tramite [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes). Inoltre, l'uso di **UpdateLayeredWindow** USA direttamente la memoria in modo più efficiente, perché il sistema non necessita della memoria aggiuntiva necessaria per archiviare l'immagine della finestra reindirizzata. Per garantire la massima efficienza nell'animazione di Windows, chiamare **UpdateLayeredWindow** per modificare la posizione e le dimensioni di una finestra sovrapposta. Si noti che dopo la chiamata di **SetLayeredWindowAttributes** , le successive chiamate di **UpdateLayeredWindow** avranno esito negativo fino a quando il bit di stile di sovrapposizione non viene cancellato e impostato nuovamente.

L'hit testing di una finestra sovrapposta è basata sulla forma e sulla trasparenza della finestra. Ciò significa che le aree della finestra che sono con chiave di colore o il cui valore alfa è zero conferiranno ai messaggi del mouse. Tuttavia, se la finestra sovrapposta dispone dello stile della finestra estesa di **WS- \_ \_ Transparent** , la forma della finestra sovrapposta verrà ignorata e gli eventi del mouse verranno passati ad altre finestre sotto la finestra sovrapposta.

### <a name="message-only-windows"></a>Message-Only Windows

Una *finestra di solo messaggio* consente di inviare e ricevere messaggi. Non è visibile, non ha alcun ordine z, non può essere enumerato e non riceve messaggi broadcast. La finestra Invia semplicemente i messaggi.

Per creare una finestra di solo messaggio, specificare la costante del [ \_ messaggio HWND](#message-only-windows) o un handle per una finestra di solo messaggio esistente nel parametro *hwndParent* della funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . È inoltre possibile modificare una finestra esistente in una finestra di solo messaggio specificando \_ il messaggio HWND nel parametro *hWndNewParent* della funzione [**padre**](/windows/win32/api/winuser/nf-winuser-setparent) .

Per trovare le finestre solo messaggio, specificare [il \_ messaggio HWND](#message-only-windows) nel parametro *hwndParent* della funzione [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) . Inoltre, **FindWindowEx** Cerca le finestre solo messaggio e le finestre di primo livello se entrambi i parametri *hwndParent* e *hwndChildAfter* sono **null**.

## <a name="window-relationships"></a>Relazioni tra finestre

Esistono diversi modi in cui una finestra può essere correlata all'utente o a un'altra finestra. Una finestra può essere una finestra di proprietà, una finestra in primo piano o una finestra di sfondo. Una finestra dispone anche di un ordine z rispetto ad altre finestre. Per altre informazioni, vedere i seguenti argomenti:

-   [Finestre in primo piano e in background](#foreground-and-background-windows)
-   [Finestre di proprietà](#owned-windows)
-   [Ordine Z](#z-order)

### <a name="foreground-and-background-windows"></a>Finestre in primo piano e in background

Ogni processo può disporre di più thread di esecuzione e ogni thread può creare finestre. Il thread che ha creato la finestra con cui l'utente sta lavorando è chiamato thread in primo piano e la finestra viene chiamata *finestra in primo piano*. Tutti gli altri thread sono thread in background e le finestre create dai thread in background sono denominate *finestre* in background.

Ogni thread ha un livello di priorità che determina la quantità di tempo della CPU ricevuta dal thread. Sebbene un'applicazione possa impostare il livello di priorità dei thread, in genere il thread in primo piano ha un livello di priorità leggermente più alto rispetto ai thread in background. Poiché ha una priorità più elevata, il thread in primo piano riceve più tempo CPU rispetto ai thread in background. Il thread in primo piano ha una priorità di base normale 9; un thread in background ha una priorità di base normale di 7.

L'utente imposta la finestra in primo piano facendo clic su una finestra o utilizzando la combinazione di tasti ALT + TAB o ALT + ESC. Per recuperare un handle per la finestra in primo piano, usare la funzione [**GetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-getforegroundwindow) . Per verificare se la finestra dell'applicazione è la finestra in primo piano, confrontare l'handle restituito da **GetForegroundWindow** con quello della finestra dell'applicazione.

Un'applicazione imposta la finestra in primo piano tramite la funzione [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) .

Il sistema limita i processi che possono impostare la finestra in primo piano. Un processo può impostare la finestra in primo piano solo se:

- Sono soddisfatte tutte le condizioni seguenti:
  - Il processo che chiama **SetForegroundWindow** appartiene a un'applicazione desktop, non a un'app UWP o a un'app di Windows Store progettata per Windows 8 o 8,1.
  - Il processo in primo piano non ha disabilitato le chiamate a **SetForegroundWindow** da una chiamata precedente alla funzione [**LockSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow) .
  - Il timeout del blocco in primo piano è scaduto (vedere [ **SPI_GETFOREGROUNDLOCKTIMEOUT** in **SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa#SPI_GETFOREGROUNDLOCKTIMEOUT)).
  - Nessun menu attivo.
- Inoltre, viene soddisfatta almeno una delle condizioni seguenti:
  - Il processo chiamante è il processo in primo piano.
  - Il processo chiamante è stato avviato dal processo in primo piano.
  - Attualmente non esiste alcuna finestra in primo piano e pertanto nessun processo in primo piano.
  - Il processo chiamante ha ricevuto l'ultimo evento di input.
  - È in corso il debug del processo in primo piano o del processo chiamante.

È possibile che a un processo venga negato il diritto di impostare la finestra in primo piano anche se soddisfa queste condizioni.

Un processo che può impostare la finestra in primo piano può consentire a un altro processo di impostare la finestra in primo piano chiamando la funzione [**AllowSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow) oppure chiamando la funzione [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) con il flag **BSF \_ ALLOWSFW** . Il processo in primo piano può disabilitare le chiamate a [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) chiamando la funzione [**LockSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow) .

### <a name="owned-windows"></a>Finestre di proprietà

Una finestra sovrapposta o popup può essere di proprietà di un'altra finestra popup o sovrapposta. Il proprietario pone diversi vincoli in una finestra.

-   Una finestra di proprietà è sempre sopra il proprietario nell'ordine z.
-   Quando il proprietario viene eliminato definitivamente, il sistema elimina automaticamente una finestra di proprietà.
-   Una finestra di proprietà viene nascosta quando il proprietario è ridotto a icona.

Solo una finestra a comparsa o sovrapposta può essere una finestra proprietaria; una finestra figlio non può essere una finestra proprietaria. Un'applicazione crea una finestra di proprietà specificando l'handle della finestra del proprietario come parametro *hwndParent* di [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) quando crea una finestra con lo stile di **\_ popup** [**WS \_ OVERLAPPED**](window-styles.md) o WS. Il parametro *hwndParent* deve identificare una finestra sovrapposta o popup. Se *hwndParent* identifica una finestra figlio, il sistema assegna la proprietà alla finestra padre di livello superiore della finestra figlio. Dopo la creazione di una finestra di proprietà, un'applicazione non può trasferire la proprietà della finestra a un'altra finestra.

Per impostazione predefinita, le finestre di dialogo e le finestre di messaggio sono Windows di proprietà. Un'applicazione specifica la finestra proprietaria quando si chiama una funzione che crea una finestra di dialogo o una finestra di messaggio.

Un'applicazione può usare la funzione [**GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) con il flag del **\_ proprietario GW** per recuperare un handle per il proprietario di una finestra.

### <a name="z-order"></a>Ordine Z

L' *ordine z* di una finestra indica la posizione della finestra in uno stack di finestre sovrapposte. Questo stack della finestra è orientato lungo un asse immaginario, ovvero l'asse z, che si estende verso l'esterno dallo schermo. La finestra nella parte superiore dello z-order si sovrappone a tutte le altre finestre. La finestra nella parte inferiore dell'ordine z è sovrapposta a tutte le altre finestre.

Il sistema mantiene l'ordine z in un singolo elenco. Aggiunge Windows all'ordine z a seconda che si tratti di finestre di primo livello, finestre di primo livello o finestre figlio. Una *finestra* di livello superiore si sovrappone a tutte le altre finestre non in primo piano, indipendentemente dal fatto che sia la finestra attiva o in primo piano. In una finestra in primo piano è presente **lo stile di \_ \_** primo livello. Tutte le finestre in primo piano vengono visualizzate nell'ordine z prima di tutte le finestre non in primo piano. Una finestra figlio viene raggruppata con il relativo elemento padre nell'ordine z.

Quando un'applicazione crea una finestra, il sistema la inserisce nella parte superiore dell'ordine z per le finestre dello stesso tipo. È possibile usare la funzione [**BringWindowToTop**](/windows/win32/api/winuser/nf-winuser-bringwindowtotop) per portare una finestra nella parte superiore dello z-order per Windows dello stesso tipo. È possibile ridisporre l'ordine z usando le funzioni [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) e [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos) .

L'utente modifica l'ordine z attivando un'altra finestra. Il sistema posiziona la finestra attiva nella parte superiore dello z order per le finestre dello stesso tipo. Quando una finestra viene visualizzata nella parte superiore dell'ordine z, le finestre figlio. È possibile utilizzare la funzione [**GetTopWindow**](/windows/win32/api/winuser/nf-winuser-gettopwindow) per eseguire una ricerca in tutte le finestre figlio di una finestra padre e restituire un handle alla finestra figlio più alta nell'ordine z. La funzione [**GetNextWindow**](/windows/win32/api/winuser/nf-winuser-getnextwindow) recupera un handle per la finestra successiva o precedente nell'ordine z.

## <a name="window-show-state"></a>Mostra stato finestra

In un determinato momento, una finestra potrebbe essere attiva o inattiva; nascosto o visibile; e ridotto a icona, ingrandito o ripristinato. Queste qualità vengono definite collettivamente come la *finestra Mostra stato*. Negli argomenti seguenti viene illustrato lo stato di visualizzazione della finestra:

-   [Finestra attiva](#active-window)
-   [Finestre disabilitate](#disabled-windows)
-   [Visibilità della finestra](#window-visibility)
-   [Finestre ridotte a icona, ingrandite e ripristinate](#minimized-maximized-and-restored-windows)

### <a name="active-window"></a>Finestra attiva

Una *finestra attiva* è la finestra di primo livello dell'applicazione con cui l'utente è attualmente in funzione. Per consentire all'utente di identificare facilmente la finestra attiva, il sistema la posiziona nella parte superiore dell'ordine z e modifica il colore della barra del titolo e del bordo nei colori della finestra attiva definita dal sistema. Solo una finestra di primo livello può essere una finestra attiva. Quando l'utente lavora con una finestra figlio, il sistema attiva la finestra padre di primo livello associata alla finestra figlio.

Solo una finestra di primo livello del sistema è attiva alla volta. L'utente attiva una finestra di primo livello facendo clic su di essa (o una delle finestre figlio) oppure usando la combinazione di tasti ALT + ESC o ALT + TAB. Un'applicazione attiva una finestra di primo livello chiamando la funzione [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) . Altre funzioni possono causare l'attivazione di un'altra finestra di primo livello del sistema, tra cui [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos), [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos), [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement)e [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow). Anche se un'applicazione può attivare un'altra finestra di primo livello in qualsiasi momento, per evitare di confondere l'utente, questa operazione deve essere eseguita solo in risposta a un'azione dell'utente. Un'applicazione usa la funzione [**GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) per recuperare un handle per la finestra attiva.

Quando l'attivazione passa da una finestra di primo livello di un'applicazione alla finestra di primo livello, il sistema invia un messaggio [**WM \_ ACTIVATEAPP**](wm-activateapp.md) a entrambe le applicazioni, notificando la modifica. Quando l'attivazione viene modificata in un'altra finestra di primo livello nella stessa applicazione, il sistema invia un messaggio di [**\_ attivazione WM**](../inputdev/wm-activate.md) di Windows.

### <a name="disabled-windows"></a>Finestre disabilitate

Una finestra può essere disabilitata. Una *finestra disabilitata* non riceve alcun input da tastiera o mouse da parte dell'utente, ma può ricevere messaggi da altre finestre, da altre applicazioni e dal sistema. In un'applicazione viene in genere disabilitata una finestra che impedisce all'utente di utilizzare la finestra. Ad esempio, un'applicazione può disabilitare un pulsante di push in una finestra di dialogo per impedire all'utente di sceglierlo. Un'applicazione può abilitare una finestra disabilitata in qualsiasi momento; Quando si abilita una finestra, viene ripristinato l'input normale.

Per impostazione predefinita, una finestra viene abilitata al momento della creazione. Un'applicazione può tuttavia specificare lo stile [**WS \_ disabled**](window-styles.md) per disabilitare una nuova finestra. Un'applicazione Abilita o Disabilita una finestra esistente tramite la funzione [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) . Il sistema invia un messaggio di [**\_ Abilitazione WM**](wm-enable.md) a una finestra quando lo stato abilitato sta per essere modificato. Un'applicazione può determinare se una finestra è abilitata tramite la funzione [**IsWindowEnabled**](/windows/win32/api/winuser/nf-winuser-iswindowenabled) .

Quando una finestra figlio è disabilitata, il sistema passa i messaggi di input del mouse figlio alla finestra padre. L'elemento padre utilizza i messaggi per determinare se abilitare la finestra figlio. Per ulteriori informazioni, vedere [input del mouse](../inputdev/mouse-input.md).

Una sola finestra alla volta può ricevere input da tastiera; Questa finestra ha lo stato attivo della tastiera. Se un'applicazione usa la funzione [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) per disabilitare una finestra con lo stato attivo della tastiera, la finestra perde lo stato attivo, oltre a essere disabilitata. **EnableWindow** imposta lo stato attivo sulla tastiera su **null**, ovvero nessuna finestra ha lo stato attivo. Se una finestra figlio o un'altra finestra discendente dispone dello stato attivo della tastiera, la finestra discendente perde lo stato attivo quando la finestra padre è disabilitata. Per altre informazioni, vedere [input da tastiera](../inputdev/keyboard-input.md).

### <a name="window-visibility"></a>Visibilità della finestra

Una finestra può essere visibile o nascosta. Il sistema Visualizza una *finestra visibile* sullo schermo. Nasconde una *finestra nascosta* senza disegnarla. Se una finestra è visibile, l'utente può fornire input alla finestra e visualizzarne l'output. Una finestra nascosta è disabilitata. Può elaborare messaggi dal sistema o da altre finestre ma non può elaborare input di utenti o visualizzare output. Quando si crea la finestra, un'applicazione imposta lo stato di visibilità di una finestra. Successivamente, l'applicazione può modificare lo stato di visibilità.

Una finestra è visibile quando lo stile di visualizzazione [**WS \_**](window-styles.md) è impostato per la finestra. Per impostazione predefinita, la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) crea una finestra nascosta, a meno che l'applicazione non specifichi lo stile **\_ visibile WS** . In genere, un'applicazione imposta lo stile **\_ visibile di WS** dopo che ha creato una finestra per la conservazione dei dettagli del processo di creazione nascosto dall'utente. Ad esempio, un'applicazione può lasciare nascosta una nuova finestra mentre Personalizza l'aspetto della finestra. Se lo stile di visualizzazione **WS \_** viene specificato in **CreateWindowEx**, il sistema invia il messaggio [**WM \_ ShowWindow**](wm-showwindow.md) alla finestra dopo aver creato la finestra, ma prima di visualizzarla.

Un'applicazione può determinare se una finestra è visibile tramite la funzione [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) . Un'applicazione può visualizzare (rendere visibile) o nascondere una finestra usando la funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow), [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos), [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos)o [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) o [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) . Queste funzioni mostrano o nascondono una finestra impostando o rimuovendo lo stile [**\_ visibile WS**](window-styles.md) per la finestra. Inviano inoltre il messaggio [**WM \_ ShowWindow**](wm-showwindow.md) alla finestra prima di visualizzarlo o nasconderlo.

Quando una finestra proprietaria è ridotta a icona, il sistema nasconde automaticamente le finestre di proprietà associate. Analogamente, quando viene ripristinata una finestra proprietaria, il sistema visualizza automaticamente le finestre di proprietà associate. In entrambi i casi, il sistema invia il messaggio [**WM \_ ShowWindow**](wm-showwindow.md) alle finestre di proprietà prima di nasconderli o visualizzarli. Occasionalmente, un'applicazione potrebbe dover nascondere le finestre di proprietà senza dover ridurre o nascondere il proprietario. In questo caso, l'applicazione usa la funzione [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) . Questa funzione imposta o rimuove lo [**stile \_ visibile WS**](window-styles.md) per tutte le finestre di proprietà e invia il messaggio **WM \_ ShowWindow** alle finestre di proprietà prima di nasconderle o visualizzarle. Nascondere una finestra proprietaria non ha alcun effetto sullo stato di visibilità delle finestre di proprietà.

Quando una finestra padre è visibile, sono visibili anche le finestre figlio associate. Analogamente, quando la finestra padre è nascosta, vengono nascoste anche le finestre figlio. La riduzione della finestra padre non ha alcun effetto sullo stato di visibilità delle finestre figlio. ovvero la finestra figlio viene ridotta a icona insieme all'elemento padre, ma lo stile di visualizzazione [**WS \_**](window-styles.md) non viene modificato.

Anche se una finestra ha lo stile di visualizzazione [**WS \_**](window-styles.md) , l'utente potrebbe non essere in grado di visualizzare la finestra sullo schermo, altre finestre potrebbero sovrapporsi completamente oppure essere state spostate oltre il bordo dello schermo. Inoltre, una finestra figlio visibile è soggetta alle regole di ritaglio stabilite dalla relazione padre-figlio. Se la finestra padre della finestra non è visibile, non sarà visibile. Se la finestra padre si sposta oltre il bordo dello schermo, la finestra figlio viene spostata anche in quanto viene disegnata una finestra figlio relativa all'angolo superiore sinistro dell'elemento padre. Ad esempio, un utente può spostare la finestra padre che contiene la finestra figlio abbastanza lontano dal bordo dello schermo che l'utente potrebbe non essere in grado di visualizzare la finestra figlio, anche se la finestra figlio e la relativa finestra padre hanno lo stile di visualizzazione **WS \_** .

### <a name="minimized-maximized-and-restored-windows"></a>Finestre ridotte a icona, ingrandite e ripristinate

Una *finestra ingrandita* è una finestra con lo stile [**WS \_ Ingrandisci**](window-styles.md) . Per impostazione predefinita, il sistema visualizza una finestra ingrandita in modo da riempire lo schermo oppure, in caso di una finestra figlia, l'area client della finestra padre. Sebbene sia possibile impostare le dimensioni di una finestra sulle stesse dimensioni di una finestra ingrandita, una finestra ingrandita è leggermente diversa. Il sistema sposta automaticamente la barra del titolo della finestra nella parte superiore della schermata o nella parte superiore dell'area client della finestra padre. Inoltre, il sistema Disabilita il bordo di ridimensionamento della finestra e la funzionalità di posizionamento della finestra della barra del titolo (in modo che l'utente non possa spostare la finestra trascinando la barra del titolo).

Una *finestra ridotta a icona* è una finestra con lo stile di [**riduzione a \_ icona WS**](window-styles.md) . Per impostazione predefinita, il sistema riduce una finestra alle dimensioni del pulsante della barra delle attività e la sposta sulla barra delle attività. Una *finestra ripristinata* è una finestra che è stata restituita alle dimensioni e alla posizione precedenti, ovvero le dimensioni che era prima che venisse ridotta a icona o ingrandita.

Se in un'applicazione viene specificato lo stile [**WS \_ Ingrandisci**](window-styles.md) o **WS \_ minimizza** nella funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , la finestra viene inizialmente ingrandita o ridotta a icona. Dopo la creazione di una finestra, un'applicazione può utilizzare la funzione [**CloseWindow**](/windows/win32/api/winuser/nf-winuser-closewindow) per ridurre al minimo la finestra. La funzione [**ArrangeIconicWindows**](/windows/win32/api/winuser/nf-winuser-arrangeiconicwindows) dispone le icone sul desktop oppure dispone le finestre figlio ridotte a icona della finestra padre nella finestra padre. La funzione [**OpenIcon**](/windows/win32/api/winuser/nf-winuser-openicon) ripristina una finestra ridotta a icona con le dimensioni e la posizione precedenti.

La funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) può ridurre, ingrandire o ripristinare una finestra. Può inoltre impostare gli Stati di visibilità e attivazione della finestra. La funzione [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) include le stesse funzionalità di **ShowWindow**, ma è possibile eseguire l'override delle posizioni predefinite ridotte a icona, ingrandite e ripristinate della finestra.

Le funzioni di [**ingrandimento**](/windows/win32/api/winuser/nf-winuser-iszoomed) e di [**icona**](/windows/win32/api/winuser/nf-winuser-isiconic) determinano se una determinata finestra è ingrandita o ridotta a icona rispettivamente. La funzione [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) recupera le posizioni ridotta a icona, ingrandita e ripristinate per la finestra e determina anche lo stato di visualizzazione della finestra.

Quando il sistema riceve un comando per ingrandire o ripristinare una finestra ridotta a icona, invia alla finestra un messaggio [**WM \_ QUERYOPEN**](wm-queryopen.md) . Se la routine della finestra restituisce **false**, il sistema ignora il comando Ingrandisci o Ripristina.

Il sistema imposta automaticamente le dimensioni e la posizione di una finestra ingrandita sulle impostazioni predefinite definite dal sistema per una finestra ingrandita. Per eseguire l'override di queste impostazioni predefinite, un'applicazione può chiamare la funzione [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) o elaborare il messaggio [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) ricevuto da una finestra quando il sistema sta per ingrandire la finestra. **WM \_ GETMINMAXINFO** include un puntatore a una struttura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) che contiene i valori usati dal sistema per impostare le dimensioni e la posizione ingrandite. La sostituzione di questi valori sostituisce le impostazioni predefinite.

## <a name="window-size-and-position"></a>Dimensioni e posizione della finestra

Le dimensioni e la posizione di una finestra sono espresse come un rettangolo di delimitazione, dato in coordinate relative alla schermata o alla finestra padre. Le coordinate di una finestra di primo livello sono relative all'angolo superiore sinistro dello schermo; le coordinate di una finestra figlio sono relative all'angolo superiore sinistro della finestra padre. Un'applicazione specifica le dimensioni e la posizione iniziali della finestra quando crea la finestra, ma può modificare le dimensioni e la posizione della finestra in qualsiasi momento. Per altre informazioni, vedere [forme compilate](../gdi/filled-shapes.md).

Questa sezione contiene i seguenti argomenti:

-   [Dimensioni e posizione predefinite](#default-size-and-position)
-   [Dimensioni del rilevamento](#tracking-size)
-   [Comandi di sistema](#system-commands)
-   [Funzioni di dimensioni e posizioni](#size-and-position-functions)
-   [Messaggi di dimensioni e posizione](#size-and-position-messages)

### <a name="default-size-and-position"></a>Dimensioni e posizione predefinite

Un'applicazione può consentire al sistema di calcolare la dimensione o la posizione iniziale di una finestra di primo livello specificando CW \_ usedefault (in [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Se l'applicazione imposta le coordinate della finestra su CW \_ usedefault (e non ha creato altre finestre di primo livello, il sistema imposta la posizione della nuova finestra rispetto all'angolo superiore sinistro dello schermo; in caso contrario, imposta la posizione rispetto alla posizione della finestra di primo livello che l'applicazione ha creato più di recente. Se i parametri width e Height sono impostati su CW \_ usedefault (, le dimensioni della nuova finestra vengono calcolate dal sistema. Se l'applicazione ha creato altre finestre di primo livello, il sistema basa le dimensioni della nuova finestra sulle dimensioni della finestra di primo livello più recente creata dall'applicazione. Se si specifica \_ usedefault (CW quando si crea una finestra popup o figlio, il sistema imposta le dimensioni della finestra sulle dimensioni minime predefinite della finestra.

### <a name="tracking-size"></a>Dimensioni del rilevamento

Il sistema mantiene le dimensioni minime e massime di rilevamento per una finestra dello stile [**WS \_ THICKFRAME**](window-styles.md) . una finestra con questo stile ha un bordo di ridimensionamento. La *dimensione minima del rilevamento* è la dimensione della finestra più piccola che è possibile produrre trascinando il bordo di ridimensionamento della finestra. Analogamente, la *dimensione massima del rilevamento* è la dimensione della finestra più grande che è possibile produrre trascinando il bordo di ridimensionamento.

Le dimensioni minime e massime di rilevamento di una finestra sono impostate sui valori predefiniti definiti dal sistema quando il sistema crea la finestra. Un'applicazione può individuare le impostazioni predefinite ed eseguirne l'override elaborando il messaggio [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) . Per ulteriori informazioni, vedere la pagina relativa alle [dimensioni e alla posizione dei messaggi](#size-and-position-messages).

### <a name="system-commands"></a>Comandi di sistema

Un'applicazione che dispone di un menu finestra può modificare le dimensioni e la posizione di tale finestra inviando i comandi di sistema. I comandi di sistema vengono generati quando l'utente sceglie i comandi dal menu finestra. Un'applicazione può emulare l'azione dell'utente inviando un messaggio [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) alla finestra. I comandi di sistema seguenti influiscono sulle dimensioni e sulla posizione di una finestra.



| Comando      | Descrizione                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_chiusura SC    | Chiude la finestra. Questo comando Invia un messaggio di [**\_ chiusura WM**](wm-close.md) alla finestra. La finestra esegue tutti i passaggi necessari per la pulizia e la distruzione. |
| \_Ingrandisci SC | Ingrandisce la finestra.                                                                                                                                                |
| SC \_ Riduci a icona | Riduce a icona la finestra.                                                                                                                                                |
| \_spostamento SC     | Sposta la finestra.                                                                                                                                                    |
| \_ripristino SC  | Ripristina le dimensioni e la posizione precedenti di una finestra ridotta a icona o ingrandita.                                                                                          |
| \_Dimensioni SC     | Avvia un comando size. Per modificare le dimensioni della finestra, utilizzare il mouse o la tastiera.                                                                                  |



 

### <a name="size-and-position-functions"></a>Funzioni di dimensioni e posizioni

Dopo la creazione di una finestra, un'applicazione può impostare la dimensione o la posizione della finestra chiamando una delle diverse funzioni, tra cui [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement), [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow), [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)e [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos). **SetWindowPlacement** imposta la posizione ridotta a icona di una finestra, la posizione ingrandita, le dimensioni e la posizione ripristinate e lo stato di visualizzazione. Le funzioni **MoveWindow** e **SetWindowPos** sono simili; impostare la dimensione o la posizione di una singola finestra dell'applicazione. La funzione **SetWindowPos** include un set di flag che influiscono sullo stato di visualizzazione della finestra. **MoveWindow** non include questi flag. Usare le funzioni [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos), **DeferWindowPos** e [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos) per impostare contemporaneamente la posizione di un numero di finestre, incluse le dimensioni, la posizione, la posizione nell'ordine z e lo stato di visualizzazione.

Un'applicazione può recuperare le coordinate del rettangolo di delimitazione di una finestra usando la funzione [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) . **GetWindowRect** riempie una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) con le coordinate degli angoli superiore sinistro e inferiore destro della finestra. Le coordinate sono relative all'angolo superiore sinistro dello schermo, anche per una finestra figlio. La funzione [**ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) o [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) mappa le coordinate dello schermo del rettangolo di delimitazione di una finestra figlio alle coordinate relative all'area client della finestra padre.

La funzione [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) recupera le coordinate dell'area client di una finestra. **GetClientRect** riempie una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) con le coordinate degli angoli superiore sinistro e inferiore destro dell'area client, ma le coordinate sono relative all'area client stessa. Ciò significa che le coordinate dell'angolo superiore sinistro dell'area client sono sempre (0, 0) e le coordinate dell'angolo inferiore destro sono la larghezza e l'altezza dell'area client.

La funzione [**CascadeWindows**](/windows/win32/api/winuser/nf-winuser-cascadewindows) sovrappone le finestre sul desktop o sovrappone le finestre figlio della finestra padre specificata. La funzione [**TileWindows**](/windows/win32/api/winuser/nf-winuser-tilewindows) riquadri le finestre sul desktop o riquadri le finestre figlio della finestra padre specificata.

### <a name="size-and-position-messages"></a>Messaggi di dimensioni e posizione

Il sistema invia il messaggio [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) a una finestra la cui dimensione o posizione sta per essere modificata. Ad esempio, il messaggio viene inviato quando l'utente fa clic su **Sposta** o **Ridimensiona** dal menu finestra o fa clic sul bordo di ridimensionamento o sulla barra del titolo; il messaggio viene inviato anche quando un'applicazione chiama [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) per spostare o ridimensionare la finestra. **WM \_ GETMINMAXINFO** include un puntatore a una struttura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) che contiene le dimensioni ingrandite predefinite e la posizione per la finestra, nonché le dimensioni minime e massime predefinite del rilevamento. Un'applicazione può eseguire l'override delle impostazioni predefinite elaborando **WM \_ GETMINMAXINFO** e impostando i membri appropriati di **MINMAXINFO**. Per ricevere **WM \_ GETMINMAXINFO**, una finestra deve avere lo stile di **\_ didascalia** [**WS \_ THICKFRAME**](window-styles.md) o WS. Una finestra con lo stile **WS \_ THICKFRAME** riceve questo messaggio durante il processo di creazione della finestra, nonché quando viene spostato o ridimensionato.

Il sistema invia il messaggio [**WM \_ WINDOWPOSCHANGING**](wm-windowposchanging.md) a una finestra la cui dimensione, posizione, posizione nell'ordine z o lo stato di visualizzazione sta per essere modificata. Questo messaggio include un puntatore a una struttura [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) che specifica la nuova dimensione della finestra, la posizione, la posizione nell'ordine z e lo stato di visualizzazione. Impostando i membri di **WINDOWPOS**, un'applicazione può influire sulle nuove dimensioni, sulla posizione e sull'aspetto della finestra.

Dopo aver modificato le dimensioni, la posizione e la posizione di una finestra nell'ordine z oppure visualizzato lo stato, il sistema invia il messaggio [**\_ WINDOWPOSCHANGED WM**](wm-windowposchanged.md) alla finestra. Questo messaggio include un puntatore a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) che informa la finestra della nuova dimensione, posizione, posizione nell'ordine z e Mostra lo stato. L'impostazione dei membri della struttura **WINDOWPOS** passata con **WM \_ WINDOWPOSCHANGED** non ha alcun effetto sulla finestra. Una finestra che deve elaborare i messaggi WM [**\_ size**](wm-size.md) e [**WM \_ Move**](wm-move.md) deve **passare WM \_ WINDOWPOSCHANGED** alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ; in caso contrario, il sistema non invia i messaggi **WM \_ size** e **WM \_ Move** alla finestra.

Il sistema invia il messaggio [**WM \_ NCCALCSIZE**](wm-nccalcsize.md) a una finestra quando la finestra viene creata o ridimensionata. Il sistema utilizza il messaggio per calcolare le dimensioni dell'area client di una finestra e la posizione dell'area client rispetto all'angolo superiore sinistro della finestra. Una finestra di solito passa questo messaggio alla routine della finestra predefinita. Tuttavia, questo messaggio può essere utile nelle applicazioni che consentono di personalizzare un'area non client di una finestra o di mantenere parti dell'area client quando la finestra viene ridimensionata. Per altre informazioni, vedere [disegno e disegno](../gdi/painting-and-drawing.md).

## <a name="window-animation"></a>Animazione finestra

È possibile produrre effetti speciali quando si visualizzano o nascondono finestre usando la funzione [**AnimateWindow**](/windows/win32/api/winuser/nf-winuser-animatewindow) . Quando la finestra viene animata in questo modo, il sistema esegue il Rolling, la diapositiva o la dissolvenza della finestra, a seconda dei flag specificati in una chiamata a **AnimateWindow**.

Per impostazione predefinita, il sistema utilizza l' *animazione Roll*. Con questo effetto, la finestra viene visualizzata per il roll-up aperto (che mostra la finestra) o il rullo chiuso (nascondendo la finestra). È possibile usare il parametro *dwFlags* per specificare se la finestra viene spostata orizzontalmente, verticalmente o in diagonale.

Quando si specifica il flag **AW \_ Slide** , il sistema utilizza l' *animazione Slide*. Con questo effetto, la finestra viene visualizzata per visualizzare (mostrando la finestra) o scorrere fuori dalla visualizzazione (nascondendo la finestra). È possibile usare il parametro *dwFlags* per specificare se la finestra scorre orizzontalmente, verticalmente o in diagonale.

Quando si specifica il flag **AW \_ Blend** , il sistema usa una *dissolvenza alfa-Blend*.

È anche possibile usare il flag **AW \_ Center** per comprimere una finestra in modo da comprimere in senso interno o espandersi verso l'esterno.

## <a name="window-layout-and-mirroring"></a>Layout della finestra e mirroring

Il layout della finestra definisce la disposizione degli oggetti di testo e Windows Graphics Device Interface (GDI) in una finestra o in un contesto di dispositivo (DC). Alcune lingue, ad esempio inglese, francese e tedesco, richiedono un layout da sinistra a destra (LTR). Altre lingue, ad esempio l'arabo e l'ebraico, richiedono un layout da destra a sinistra (RTL). Il layout della finestra viene applicato al testo, ma influiscono anche sugli altri elementi GDI della finestra, incluse le bitmap, le icone, la posizione dell'origine, i pulsanti, i controlli dell'albero a cascata e il fatto che la coordinata orizzontale aumenti man mano che si procede verso sinistra o destra. Ad esempio, dopo che un'applicazione ha impostato il layout RTL, l'origine viene posizionata sul bordo destro della finestra o del dispositivo e il numero che rappresenta la coordinata orizzontale aumenta man mano che si sposta verso sinistra. Tuttavia, non tutti gli oggetti sono interessati dal layout di una finestra. Ad esempio, il layout per le finestre di dialogo, le finestre di messaggio e i contesti di dispositivo che non sono associati a una finestra, ad esempio i controller di dominio dei metafile e delle stampanti, devono essere gestiti separatamente. Le specifiche per queste informazioni sono indicate più avanti in questo argomento.

Le funzioni finestra consentono di specificare o modificare il layout della finestra nelle versioni arabe ed ebraiche di Windows. Si noti che la modifica a un layout RTL (noto anche come mirroring) non è supportata per le finestre con lo stile [cs \_ OWNDC](about-window-classes.md) o per un controller di dominio con la \_ modalità grafica avanzata GM.

Per impostazione predefinita, il layout della finestra è da sinistra a destra (LTR). Per impostare il layout della finestra RTL, chiamare [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) con lo stile **WS \_ ex \_ LAYOUTRTL**. Inoltre, per impostazione predefinita, una finestra figlio, ovvero una creata con lo [**stile \_ figlio WS**](window-styles.md) e con un parametro *HWND* padre valido nella chiamata a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o **CreateWindowEx**, ha lo stesso layout del relativo elemento padre. Per disabilitare l'ereditarietà del mirroring in tutte le finestre figlio, specificare **WS \_ ex \_ NOINHERITLAYOUT** nella chiamata a **CreateWindowEx**. Si noti che il mirroring non viene ereditato dalle finestre di proprietà (quelle create senza lo stile **WS \_ figlio** ) o quelle create con il parametro *HWND* padre in **CreateWindowEx** impostato su **null**. Per disabilitare l'ereditarietà del mirroring per una singola finestra, elaborare il messaggio [**WM \_ NCCREATE**](wm-nccreate.md) con [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) per disattivare il flag **WS \_ ex \_ LAYOUTRTL** . Questa elaborazione è aggiunta a qualsiasi altra elaborazione necessaria. Il frammento di codice seguente illustra come eseguire questa operazione.


```
SetWindowLong (hWnd, 
               GWL_EXSTYLE, 
               GetWindowLong(hWnd,GWL_EXSTYLE) & ~WS_EX_LAYOUTRTL))
```



È possibile impostare il layout predefinito su RTL chiamando [**SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout)(layout \_ RTL). Tutte le finestre create dopo la chiamata verranno sottoposte a mirroring, ma le finestre esistenti non saranno interessate. Per disattivare il mirroring predefinito, chiamare **SetProcessDefaultLayout**(0).

Si noti che [**SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout) riflette i controller di dominio solo delle finestre con mirroring. Per eseguire il mirroring di qualsiasi controller di dominio, chiamare [**selayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(HDC, layout \_ RTL). Per ulteriori informazioni, vedere la discussione relativa ai contesti di dispositivo di mirroring non associati a Windows, disponibile più avanti in questo argomento.

Anche le bitmap e le icone in una finestra con mirroring vengono rispecchiate per impostazione predefinita. Tuttavia, non tutti questi devono essere sottoutilizzati per il mirroring. Ad esempio, quelli con testo, un logo aziendale o un orologio analogico non devono essere sottoporre a mirroring. Per disabilitare il mirroring delle bitmap, chiamare [**selayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) con il \_ bit BITMAPORIENTATIONPRESERVED del layout impostato in *dwLayout*. Per disabilitare il mirroring in un controller di dominio, chiamare **selayout**(HDC, 0).

Per eseguire una query sul layout predefinito corrente, chiamare [**GetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-getprocessdefaultlayout). In caso di esito positivo, *pdwDefaultLayout* contiene il layout \_ RTL o 0. Per eseguire una query sulle impostazioni di layout del contesto di dispositivo, chiamare [**GetLayout**](/windows/win32/api/wingdi/nf-wingdi-getlayout). In caso di esito positivo, **GetLayout** restituisce un **valore DWORD** che indica le impostazioni di layout in base alle impostazioni del LAYOUT \_ RTL e del layout \_ BITMAPORIENTATIONPRESERVED bit.

Dopo la creazione di una finestra, modificare il layout utilizzando la funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) . Questo è necessario, ad esempio, quando l'utente modifica la lingua dell'interfaccia utente di una finestra esistente da araba o ebraica a tedesca. Tuttavia, quando si modifica il layout di una finestra esistente, è necessario invalidare e aggiornare la finestra per assicurarsi che il contenuto della finestra venga interamente disegnato nello stesso layout. Nell'esempio di codice riportato di seguito viene utilizzato il codice di esempio per modificare il layout della finestra in base alle esigenze:


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



Nel mirroring è necessario pensare in termini di "near" e "lontano" invece di "left" e "Right". In caso contrario, è possibile che si verifichino problemi. Una procedura di codifica comune che causa problemi in una finestra con mirroring si verifica quando si esegue il mapping tra coordinate dello schermo e coordinate del client. Ad esempio, le applicazioni spesso utilizzano codice simile al seguente per posizionare un controllo in una finestra:


```
// DO NOT USE THIS IF APPLICATION MIRRORS THE WINDOW

// get coordinates of the window in screen coordinates
GetWindowRect(hControl, (LPRECT) &rControlRect);  

// map screen coordinates to client coordinates in dialog
ScreenToClient(hDialog, (LPPOINT) &rControlRect.left); 
ScreenToClient(hDialog, (LPPOINT) &rControlRect.right);
```



Ciò causa problemi nel mirroring poiché il bordo sinistro del rettangolo diventa il bordo destro in una finestra con mirroring e viceversa. Per evitare questo problema, sostituire le chiamate [**ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) con una chiamata a [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) come indicato di seguito:


```
// USE THIS FOR MIRRORING

GetWindowRect(hControl, (LPRECT) &rControlRect);
MapWindowPoints(NULL, hDialog, (LPPOINT) &rControlRect, 2)
```



Questo codice funziona perché, sulle piattaforme che supportano il mirroring, [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) viene modificato per scambiare le coordinate dei punti di sinistra e destra quando viene eseguito il mirroring della finestra del client. Per ulteriori informazioni, vedere la sezione Osservazioni di **MapWindowPoints**.

Un'altra pratica comune che può causare problemi nelle finestre con mirroring consiste nel posizionare gli oggetti in una finestra client usando gli offset nelle coordinate dello schermo anziché le coordinate client. Nel codice seguente, ad esempio, viene utilizzata la differenza tra le coordinate dello schermo e la posizione x nelle coordinate client per posizionare un controllo in una finestra di dialogo.


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



Questo codice è corretto quando la finestra di dialogo ha un layout da sinistra a destra (LTR) e la modalità di mapping del client è il \_ testo mm, perché la nuova posizione x nelle coordinate client corrisponde alla differenza tra i bordi sinistro del controllo e la finestra di dialogo nelle coordinate dello schermo. Tuttavia, in una finestra di dialogo con mirroring, Left e right vengono invertiti, quindi è consigliabile usare [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) come segue:


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



### <a name="mirroring-dialog-boxes-and-message-boxes"></a>Finestre di dialogo di mirroring e finestre di messaggio

Le finestre di dialogo e le finestre di messaggio non ereditano il layout, quindi è necessario impostare il layout in modo esplicito. Per eseguire il mirroring di una finestra di messaggio, chiamare [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) o [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) con l'opzione **MB \_ RTLREADING** Per eseguire il layout di una finestra di dialogo da destra a sinistra, usare lo stile esteso WS \_ ex \_ LAYOUTRTL nella struttura del modello di finestra di dialogo [**DLGTEMPLATEEX**](../dlgbox/dlgtemplateex.md). Le finestre delle proprietà sono un caso speciale di finestre di dialogo. Ogni scheda viene considerata come una finestra di dialogo separata, pertanto è necessario includere lo \_ stile WS ex \_ LAYOUTRTL in ogni scheda di cui si desidera eseguire il mirroring.

### <a name="mirroring-device-contexts-not-associated-with-a-window"></a>Il mirroring dei contesti di dispositivo non è associato a una finestra

I controller di dominio non associati a una finestra, ad esempio i controller di dominio del metafile o della stampante, non ereditano il layout, quindi è necessario impostare il layout in modo esplicito. Per modificare il layout del contesto di dispositivo, utilizzare la funzione [**selayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) .

La funzione [**selayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) viene utilizzata raramente con Windows. In genere, Windows riceve un controller di dominio associato solo nell'elaborazione di un messaggio di [**\_ disegno WM**](../gdi/wm-paint.md) . Occasionalmente, un programma crea un controller di dominio per una finestra chiamando [**GetDC**](/windows/win32/api/winuser/nf-winuser-getdc). In entrambi i casi, il layout iniziale per il controller di dominio viene impostato da [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint) o **GetDC** in base al \_ flag WS ex LAYOUTRTL della finestra \_ .

I valori restituiti da [**GetWindowOrgEx**](/windows/win32/api/wingdi/nf-wingdi-getwindoworgex), [**GetWindowExtEx**](/windows/win32/api/wingdi/nf-wingdi-getwindowextex), [**GetViewportOrgEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportorgex) e [**GetViewportExtEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportextex) non sono interessati dalla chiamata a [**selayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout).

Quando il layout è RTL, [**GetMapMode**](/windows/win32/api/wingdi/nf-wingdi-getmapmode) restituirà il \_ testo mm anisotropico anziché il \_ testo mm. La chiamata di [**SetMapMode**](/windows/win32/api/wingdi/nf-wingdi-setmapmode) con \_ il testo mm funzionerà correttamente. il valore restituito da **GetMapMode** sarà interessato. Analogamente, [**la chiamata a**](/windows/win32/api/wingdi/nf-wingdi-setlayout)SetText (HDC, layout \_ RTL) quando la modalità di mapping è il \_ testo mm causa la modifica della modalità di mapping indicata in mm \_ anisotropico.

## <a name="window-destruction"></a>Distruzione finestra

In generale, un'applicazione deve eliminare tutte le finestre create. Questa operazione viene eseguita tramite la funzione [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) . Quando una finestra viene distrutta, il sistema nasconde la finestra, se è visibile, quindi rimuove tutti i dati interni associati alla finestra. In questo modo viene invalidato l'handle della finestra, che non può più essere utilizzato dall'applicazione.

Un'applicazione elimina molte delle finestre create subito dopo la creazione. Ad esempio, in un'applicazione viene in genere eliminata una finestra di dialogo non appena l'applicazione dispone di un input sufficiente da parte dell'utente per continuare l'attività. Un'applicazione elimina definitivamente la finestra principale dell'applicazione (prima di terminare).

Prima di eliminare una finestra, un'applicazione deve salvare o rimuovere tutti i dati associati alla finestra e deve rilasciare tutte le risorse di sistema allocate per la finestra. Se l'applicazione non rilascia le risorse, il sistema libererà le risorse che non vengono liberate dall'applicazione.

L'eliminazione definitiva di una finestra non influisce sulla classe della finestra da cui viene creata la finestra. È ancora possibile creare nuove finestre usando tale classe e tutte le finestre esistenti di tale classe continuano a funzionare. L'eliminazione definitiva di una finestra Elimina inoltre le finestre discendenti della finestra. La funzione [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) invia prima di tutto un messaggio [**WM \_ Destroy**](wm-destroy.md) alla finestra, quindi alle finestre figlio e alle finestre discendenti. In questo modo, vengono eliminate anche tutte le finestre discendenti della finestra distrutta.

Una finestra con un menu finestra riceve un messaggio di [**\_ chiusura WM**](wm-close.md) quando l'utente fa clic su **Chiudi**. Elaborando questo messaggio, un'applicazione può richiedere conferma all'utente prima di eliminare definitivamente la finestra. Se l'utente conferma che la finestra deve essere distrutta, l'applicazione può chiamare la funzione [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) per eliminare definitivamente la finestra.

Se la finestra distrutta è la finestra attiva, lo stato attivo e lo stato attivo vengono trasferiti in un'altra finestra. La finestra che diventa la finestra attiva è la finestra successiva, come determinato dalla combinazione di tasti ALT + ESC. La nuova finestra attiva determina quindi la finestra che riceve lo stato attivo della tastiera.

 

 
