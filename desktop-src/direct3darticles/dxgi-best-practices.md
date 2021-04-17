---
title: Procedure consigliate per l'infrastruttura grafica DirectX (DXGI)
description: Questo articolo illustra i problemi di portabilità delle chiavi.
ms.assetid: 2df92ffe-1bfc-d682-2770-20cf0c831c9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f576368674d05af74e3161d4251301ebc066a489
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399481"
---
# <a name="directx-graphics-infrastructure-dxgi-best-practices"></a>Infrastruttura grafica DirectX (DXGI): procedure consigliate

Microsoft DirectX Graphics Infrastructure (DXGI) è un nuovo sottosistema introdotto con Windows Vista che incapsula alcune delle attività di basso livello richieste da Direct3D 10, 10,1, 11 e 11,1. Dal punto di vista di un programmatore Direct3D 9, DXGI include la maggior parte del codice per l'enumerazione, la creazione della catena di scambio e la presentazione che in precedenza era stato compresso nelle API Direct3D 9. Quando si porta un'app in DXGI e Direct3D 10. x e Direct3D 11. x, è necessario prendere in considerazione alcune considerazioni per assicurarsi che il processo venga eseguito senza problemi.

Questo articolo illustra i problemi di portabilità delle chiavi.

-   [Problemi a schermo intero](#full-screen-issues)
-   [Più monitoraggi](#multiple-monitors)
-   [Stili della finestra e DXGI](#window-styles-and-dxgi)
-   [Multithreading e DXGI](#multithreading-and-dxgi)
-   [Gamma e DXGI](#gamma-and-dxgi)
-   [DXGI 1,1](#dxgi-11)
-   [DXGI 1,2](#dxgi-12)

## <a name="full-screen-issues"></a>Problemi di Full-Screen

Nel porting da Direct3D 9 a DXGI e a Direct3D 10. x o Direct3D 11. x, spesso i problemi associati al passaggio dalla finestra alla modalità a schermo intero possono causare problemi per gli sviluppatori. I principali problemi si verificano perché le applicazioni Direct3D 9, a differenza delle applicazioni DXGI, richiedono un approccio pratico per tenere traccia degli stili e degli Stati delle finestre. Quando il codice per la modifica della modalità viene trasferito per l'esecuzione su DXGI, causa spesso un comportamento imprevisto.

Spesso, le applicazioni Direct3D 9 gestivano la transizione in modalità a schermo intero impostando la risoluzione del buffer anteriore, forzando il dispositivo in modalità esclusiva a schermo intero e quindi impostando le risoluzioni del buffer indietro per la corrispondenza. Un percorso separato è stato usato per le modifiche alle dimensioni della finestra perché doveva essere gestito dal processo della finestra ogni volta che l'applicazione riceve un \_ messaggio di dimensioni WM.

DXGI tenta di semplificare questo approccio combinando i due casi. Ad esempio, quando il bordo della finestra viene trascinato in modalità finestra, l'applicazione riceve un \_ messaggio di dimensioni WM. DXGI intercetta questo messaggio e ridimensiona automaticamente il buffer anteriore. A tale scopo, è necessario chiamare [**IDXGISwapChain:: ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) per ridimensionare il buffer nascosto in base alle dimensioni passate come parametri in \_ dimensioni WM. Analogamente, quando l'applicazione deve passare dalla modalità a schermo intero a quella a finestra, l'applicazione può semplicemente chiamare [**IDXGISwapChain:: SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate). DXGI ridimensiona il buffer anteriore in modo che corrisponda alla modalità a schermo intero appena selezionato e invia un \_ messaggio di dimensioni WM all'applicazione. L'applicazione chiama di nuovo **ResizeBuffers**, proprio come se il bordo della finestra fosse stato trascinato.

La metodologia della spiegazione precedente segue un percorso molto particolare. Per impostazione predefinita, DXGI imposta la risoluzione a schermo intero sulla risoluzione del desktop. Molte applicazioni, tuttavia, passano a una risoluzione a schermo intero preferita. In tal caso, DXGI fornisce [**IDXGISwapChain:: ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget). Questa operazione deve essere chiamata prima di chiamare [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate). Sebbene questi metodi possano essere chiamati nell'ordine opposto (**SetFullscreenState** prima, seguito da **ResizeTarget**), in questo modo \_ viene inviato un messaggio di dimensioni WM aggiuntive all'applicazione. Questa operazione può anche causare lo sfarfallio, perché DXGI potrebbe essere forzato a eseguire due modifiche in modalità. Dopo aver chiamato **SetFullscreenState**, è consigliabile chiamare di nuovo **ResizeTarget** con il membro **RefreshRate** della [**modalità DXGI \_ \_ desc**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) azzerato. Questa operazione equivale a un'istruzione di nessuna operazione in DXGI, ma può evitare problemi con la frequenza di aggiornamento, che verranno discussi successivamente.

In modalità schermo intero, il Gestione finestre desktop (DWM) è disabilitato. DXGI può eseguire un flip per presentare il contenuto del buffer nascosto anziché eseguire un blit, operazione eseguita in modalità finestra. Questo miglioramento delle prestazioni può essere annullato, tuttavia, se non vengono soddisfatti determinati requisiti. Per assicurarsi che DXGI faccia un capovolgimento anziché un blit, il buffer anteriore e il buffer nascosto devono essere dimensionati in modo identico. Se l'applicazione gestisce correttamente i \_ messaggi di dimensioni WM, questo non dovrebbe essere un problema. Inoltre, i formati devono essere identici.

Il problema per la maggior parte delle applicazioni è la frequenza di aggiornamento. La frequenza di aggiornamento specificata nella chiamata a [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) deve essere una frequenza di aggiornamento enumerata dall'oggetto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) usato dalla catena di scambio. DXGI è in grado di calcolare automaticamente questo valore se l'applicazione Azzera il membro **RefreshRate** di [**DXGI \_ mode \_ desc**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) passato a **ResizeTarget**. È importante non presupporre che alcune frequenze di aggiornamento siano sempre supportate e semplicemente impostare come hardcoded un valore. Spesso, gli sviluppatori scelgono 60 Hz come frequenza di aggiornamento, non sapendo che la frequenza di aggiornamento enumerata dal monitor è circa 60.000/1.001 Hz dal monitor. Se la frequenza di aggiornamento non corrisponde alla frequenza di aggiornamento prevista di 60, DXGI è forzato a eseguire un blit in modalità schermo intero anziché un capovolgimento.

L'ultimo problema che gli sviluppatori spesso affrontano è come modificare le risoluzioni a schermo intero rimanendo in modalità schermo intero. La chiamata a [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) e [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) a volte riesce, ma la risoluzione a schermo intero rimane la risoluzione del desktop. Inoltre, gli sviluppatori possono creare una catena di scambio a schermo intero e fornire una risoluzione specifica, solo per trovare che DXGI utilizza per impostazione predefinita la risoluzione desktop indipendentemente dai numeri passati. Se non diversamente indicato, il valore predefinito di DXGI è la risoluzione del desktop per le catene di scambio a schermo intero. Quando si crea una catena di scambio a schermo intero, il membro **Flags** della struttura [**\_ desc della \_ catena \_ di scambio DXGI**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) deve essere impostato sull' [**\_ \_ \_ \_ \_ \_ opzione di modalità Consenti flag catena di scambio DXGI**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) per eseguire l'override del comportamento predefinito di dxgi. Questo flag può anche essere passato a **ResizeTarget** per abilitare o disabilitare questa funzionalità in modo dinamico.

## <a name="multiple-monitors"></a>Più monitoraggi

Quando si usa DXGI con più monitoraggi, è necessario seguire due regole.

La prima regola si applica alla creazione di due o più catene di scambio a schermo intero su più monitor. Quando si creano tali catene di scambio, è preferibile creare tutte le catene di scambio come finestra, quindi impostarle a schermo intero. Se le catene di scambio vengono create in modalità schermo intero, la creazione di una seconda catena di scambio causa l'invio di una modifica della modalità alla prima catena di scambio, che può causare la terminazione della modalità schermo intero.

La seconda regola si applica agli output. Osservare gli output utilizzati durante la creazione di catene di scambio. Con DXGI, l'oggetto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) controlla il monitoraggio usato dalla catena di scambio quando si diventa a schermo intero. A differenza di DXGI, Direct3D 9 non aveva alcun concetto di output.

## <a name="window-styles-and-dxgi"></a>Stili della finestra e DXGI

Le applicazioni Direct3D 9 erano molto lavoro da eseguire quando si passa da una modalità a schermo intero a un'altra. Gran parte di questo lavoro ha comportato la modifica degli stili della finestra per aggiungere e rimuovere bordi, per aggiungere barre di scorrimento e così via. Quando le applicazioni vengono trasferite in DXGI e Direct3D 10. x o Direct3D 11. x, questo codice viene spesso lasciato sul posto. A seconda delle modifiche apportate, il cambio tra le modalità può causare un comportamento imprevisto. Ad esempio, quando si passa alla modalità finestra, l'applicazione potrebbe non avere più una cornice della finestra o un bordo della finestra, anche se dispone di codice che imposta in modo specifico questi stili. Questo problema si verifica perché DXGI gestisce ora la maggior parte di questo stile cambiando autonomamente. L'impostazione manuale degli stili della finestra può interferire con DXGI e questo può causare un comportamento imprevisto.

Il comportamento consigliato è quello di eseguire il minor lavoro possibile e di consentire a DXGI di gestire la maggior parte dell'interazione con le finestre. Tuttavia, se l'applicazione deve gestire il proprio comportamento di windowing, [**IDXGIFactory:: MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation) può essere usato per indicare a DXGI di disabilitare alcune della gestione automatica della finestra.

## <a name="multithreading-and-dxgi"></a>Multithreading e DXGI

Quando si usa DXGI in un'applicazione multithread per garantire che non si verifichino deadlock, è necessario prestare particolare attenzione. A causa dell'interazione di chiusura di DXGI con windowing, occasionalmente invia messaggi della finestra alla finestra dell'applicazione associata. DXGI richiede che le modifiche apportate alla finestra vengano eseguite prima di continuare, quindi utilizzerà [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), che è una chiamata sincrona. L'applicazione deve elaborare il messaggio della finestra prima della restituzione di **SendMessage** .

In un'applicazione in cui DXGI chiama e il message pump si trovano nello stesso thread (o in un'applicazione a thread singolo), è necessario eseguire alcune operazioni. Quando la chiamata DXGI si trova sullo stesso thread del message pump, [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) chiama il [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))della finestra. Questo ignora il message pump e consente di continuare l'esecuzione dopo la chiamata a **SendMessage**. Tenere presente che le chiamate a [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) , ad esempio [**IDXGISwapChain::P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)reinviate, vengono considerate chiamate DXGI; DXGI può rinviare il lavoro da [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) o [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) fino a quando non viene chiamato il metodo **present** .

Se la chiamata DXGI e message pump si trovano su thread diversi, è necessario prestare attenzione per evitare deadlock. Quando il message pump e SendMessage si trovano su thread diversi, [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) aggiunge un messaggio alla coda di messaggi della finestra e attende che la finestra elabori il messaggio. Se la routine della finestra è occupata o non viene chiamata dal message pump, il messaggio potrebbe non essere mai elaborato e DXGI resterà in attesa per un periodo illimitato.

Se, ad esempio, un'applicazione che dispone di un message pump su un thread e il relativo rendering su un altro, potrebbe voler modificare le modalità. Il thread message pump indica al thread di rendering di modificare le modalità e attende il completamento della modifica della modalità. Tuttavia, il thread di rendering chiama le funzioni DXGI, che a loro volta chiamano [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), che si blocca fino a quando il message pump elabora il messaggio. Si verifica un deadlock perché entrambi i thread sono ora bloccati e sono in attesa l'uno sull'altro. Per evitare questo problema, non bloccare mai il message pump. Se un blocco è inevitabile, tutte le interazioni DXGI devono essere eseguite nello stesso thread del message pump.

## <a name="gamma-and-dxgi"></a>Gamma e DXGI

Sebbene la gamma possa essere gestita in modo ottimale in Direct3D 10. x o Direct3D 11. x usando trame SRGB, la rampa gamma può comunque essere utile per gli sviluppatori che desiderano un valore gamma diverso rispetto a 2,2 o che usano un formato di destinazione di rendering che non supporta SRGB. Quando si imposta la rampa gamma tramite DXGI, tenere presenti due problemi. Il primo problema è che i valori della rampa passati in [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) sono valori float, non valori di **parole** . Assicurarsi inoltre che il codice trasferito da Direct3D 9 non tenti di eseguire la conversione in valori di **Word** prima di passarli a **SetGammaControl**.

Il secondo problema è che, dopo aver modificato la modalità schermo intero, [**SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) potrebbe non sembrare funzionante, a seconda dell'oggetto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) in uso. Quando si passa alla modalità a schermo intero, DXGI crea un nuovo oggetto di output e usa l'oggetto per tutte le operazioni successive nell'output. Se si chiama **SetGammaControl** in un output enumerato prima di un'opzione di modalità a schermo intero, la chiamata non viene indirizzata verso l'output attualmente utilizzato da dxgi. Per evitare questo problema, chiamare [**IDXGISwapChain:: GetContainingOutput**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput) per ottenere l'output corrente, quindi chiamare **SetGammaControl** da questo output per ottenere il comportamento corretto.

Per informazioni sull'uso della correzione gamma, vedere [uso della correzione gamma](/windows/desktop/direct3ddxgi/using-gamma-correction).

## <a name="dxgi-11"></a>DXGI 1,1

Il runtime Direct3D 11 incluso in Windows 7 e installato in Windows Vista (vedere [KB971644](https://support.microsoft.com/kb/971644)) include la versione 1,1 di dxgi. Questo aggiornamento aggiunge le definizioni per diversi nuovi formati (in particolare BGRA, la distorsione X2 a 10 bit e la compressione della trama BC6H e BC7 di Direct3D 11), nonché una nuova versione di DXGI Factory e interfacce di adapter ([**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1), [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1), [**IDXGIAdapter1**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1)) per l'enumerazione delle connessioni Desktop remoto.

Quando si utilizza Direct3D 11, per impostazione predefinita il runtime utilizzerà DXGI 1,1 quando viene chiamato [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) con un puntatore [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) null. La combinazione di uso di DXGI 1,0 e DXGI 1,1 nello stesso processo non è supportata. Anche la combinazione di istanze di oggetti DXGI da diverse Factory nello stesso processo non è supportata. Pertanto, quando si usa DirectX 11, qualsiasi uso esplicito delle interfacce DXGI usa un [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) creato dal punto di ingresso di [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) in "DXGI.DLL" per garantire che l'applicazione usi sempre DXGI 1,1.

## <a name="dxgi-12"></a>DXGI 1,2

Il runtime Direct3D 11,1 incluso in Windows 8 include anche la versione 1,2 di DXGI.

DXGI 1,2 Abilita queste funzionalità:

-   rendering stereo
-   formati a 16 bit per pixel

    -   DXGI \_ Format \_ B5G6R5 \_ UNORM e DXGI \_ Format \_ B5G5R5A1 \_ UNORM sono ora completamente supportati
    -   è stato aggiunto un nuovo formato DXGI \_ \_ B5G5R5A1 \_ UNORM Format

-   formati video
-   nuove interfacce DXGI

Per altre informazioni sulle funzionalità di DXGI 1,2, vedere [miglioramenti di DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements).

 

 