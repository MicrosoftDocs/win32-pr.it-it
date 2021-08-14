---
title: procedure consigliate per DirectX Graphic Infrastructure (DXGI)
description: Questo articolo illustra i principali problemi di porting.
ms.assetid: 2df92ffe-1bfc-d682-2770-20cf0c831c9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be992fe2346868eb3481482325297a2c9ec27ee61bdd2c65f83b0f916fc22308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290238"
---
# <a name="directx-graphics-infrastructure-dxgi-best-practices"></a>DirectX Graphic Infrastructure (DXGI): Procedure consigliate

Microsoft DirectX Graphic Infrastructure (DXGI) è un nuovo sottosistema introdotto con Windows Vista che incapsula alcune delle attività di basso livello necessarie per Direct3D 10, 10.1, 11 e 11.1. Dal punto di vista di un programmatore Direct3D 9, DXGI include la maggior parte del codice per l'enumerazione, la creazione della catena di scambio e la presentazione precedentemente racchiusa nelle API Direct3D 9. Quando si esegue il port di un'app in DXGI e Direct3D 10.x e Direct3D 11.x, è necessario tenere conto di alcune considerazioni per assicurarsi che il processo venga eseguito senza problemi.

Questo articolo illustra i principali problemi di porting.

-   [Problemi a schermo intero](#full-screen-issues)
-   [Più monitoraggi](#multiple-monitors)
-   [Stili di finestra e DXGI](#window-styles-and-dxgi)
-   [Multithreading e DXGI](#multithreading-and-dxgi)
-   [Gamma e DXGI](#gamma-and-dxgi)
-   [DXGI 1.1](#dxgi-11)
-   [DXGI 1.2](#dxgi-12)

## <a name="full-screen-issues"></a>Full-Screen problemi

Durante la portabilità da Direct3D 9 a DXGI e a Direct3D 10.x o Direct3D 11.x, i problemi associati al passaggio dalla modalità finestra alla modalità schermo intero spesso possono causare problemi per gli sviluppatori. I problemi principali si verificano perché le applicazioni Direct3D 9, a differenza delle applicazioni DXGI, richiedono un approccio più diretto al rilevamento degli stili e degli stati delle finestre. Quando il codice di modifica della modalità viene portato per l'esecuzione in DXGI, spesso causa un comportamento imprevisto.

Spesso, le applicazioni Direct3D 9 gestiscono la transizione alla modalità schermo intero impostando la risoluzione del front buffer, forzando il dispositivo in modalità esclusiva a schermo intero e quindi impostando le risoluzioni del buffer nascosto in modo che corrispondano. È stato usato un percorso separato per le modifiche alle dimensioni della finestra perché dovevano essere gestite dal processo della finestra ogni volta che l'applicazione riceveva un messaggio WM \_ SIZE.

DXGI tenta di semplificare questo approccio combinando i due casi. Ad esempio, quando il bordo della finestra viene trascinato in modalità finestra, l'applicazione riceve un messaggio WM \_ SIZE. DXGI intercetta questo messaggio e ridimensiona automaticamente il front buffer. L'applicazione deve solo chiamare [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) per ridimensionare il buffer nascosto alle dimensioni passate come parametri in WM \_ SIZE. Analogamente, quando l'applicazione deve passare dalla modalità schermo intero alla modalità finestra, l'applicazione può chiamare [**semplicemente IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate). DXGI ridimensiona il front buffer in modo che corrisponda alla modalità schermo intero appena selezionata e invia un messaggio WM \_ SIZE all'applicazione. L'applicazione chiama **nuovamente ResizeBuffers**, come se il bordo della finestra fosse stato trascinato.

La metodologia della spiegazione precedente segue un percorso molto particolare. Per impostazione predefinita, DXGI imposta la risoluzione a schermo intero sulla risoluzione desktop. Molte applicazioni, tuttavia, passano a una risoluzione a schermo intero preferita. In tal caso, DXGI fornisce [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget). Questa operazione deve essere chiamata prima [**di chiamare SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate). Anche se questi metodi possono essere chiamati nell'ordine opposto (**SetFullscreenState** prima, seguito da **ResizeTarget**), in questo modo viene inviato un messaggio WM SIZE aggiuntivo \_ all'applicazione. Questa operazione può causare anche uno sfarfallio, poiché DXGI potrebbe essere forzato a eseguire due modifiche della modalità. Dopo aver **chiamato SetFullscreenState,** è consigliabile chiamare **nuovamente ResizeTarget** con il membro **RefreshRate** di [**DXGI \_ MODE \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) azzerato. Si tratta di un'istruzione di nessuna operazione in DXGI, ma può evitare problemi con la frequenza di aggiornamento, come illustrato di seguito.

In modalità schermo intero, il Gestione finestre desktop (DWM) è disabilitato. DXGI può eseguire un capovolgimento per presentare il contenuto del buffer nascosto anziché eseguire un blit, operazione che verrebbe eseguita in modalità finestra. Questo miglioramento delle prestazioni può essere annullato, tuttavia, se non vengono soddisfatti determinati requisiti. Per garantire che DXGI eserciti un capovolgimento anziché un blit, il front buffer e il buffer nascosto devono essere ridimensionati in modo identico. Se l'applicazione gestisce correttamente i messaggi WM \_ SIZE, questo non dovrebbe essere un problema. Inoltre, i formati devono essere identici.

Il problema per la maggior parte delle applicazioni è la frequenza di aggiornamento. La frequenza di aggiornamento specificata nella chiamata a [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) deve essere una frequenza di aggiornamento enumerata dall'oggetto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) utilizzato dalla catena di scambio. DXGI può calcolare automaticamente questo valore se l'applicazione azzera il membro **RefreshRate** di [**DXGI \_ MODE \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) passato in **ResizeTarget.** È importante non presupporre che siano sempre supportate determinate frequenze di aggiornamento e che sia sufficiente impostare come hard code un valore. Spesso gli sviluppatori scelgono 60 Hz come frequenza di aggiornamento, senza sapere che la frequenza di aggiornamento enumerata dal monitoraggio è di circa 60.000/1.001 Hz dal monitoraggio. Se la frequenza di aggiornamento non corrisponde alla frequenza di aggiornamento prevista di 60, DXGI viene forzato a eseguire un blit in modalità schermo intero anziché capovolgimento.

L'ultimo problema che gli sviluppatori devono spesso affrontare è come modificare le risoluzioni a schermo intero rimanendo in modalità schermo intero. La [**chiamata di ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) e [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) a volte ha esito positivo, ma la risoluzione a schermo intero rimane la risoluzione del desktop. Inoltre, gli sviluppatori possono creare una catena di scambio a schermo intero e fornire una risoluzione specifica, solo per scoprire che DXGI viene utilizzato per impostazione predefinita per la risoluzione del desktop indipendentemente dai numeri passati. Se non diversamente indicato, DXGI ha come impostazione predefinita la risoluzione del desktop per le catene di scambio a schermo intero. Quando si crea una catena di scambio a schermo intero, il membro **Flags** della struttura [**DXGI \_ SWAP CHAIN \_ \_ DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) deve essere impostato su [**DXGI \_ SWAP CHAIN FLAG ALLOW MODE \_ \_ \_ \_ \_ SWITCH**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) per eseguire l'override del comportamento predefinito di DXGI. Questo flag può anche essere passato a **ResizeTarget** per abilitare o disabilitare questa funzionalità in modo dinamico.

## <a name="multiple-monitors"></a>Più monitoraggi

Quando si usa DXGI con più monitoraggi, è necessario seguire due regole.

La prima regola si applica alla creazione di due o più catene di scambio a schermo intero su più monitor. Quando si creano catene di scambio di questo tipo, è meglio creare tutte le catene di scambio come finestre e quindi impostarle a schermo intero. Se le catene di scambio vengono create in modalità schermo intero, la creazione di una seconda catena di scambio determina l'invio di una modifica della modalità alla prima catena di scambio, che potrebbe causare la terminazione della modalità schermo intero.

La seconda regola si applica agli output. Controllare gli output usati durante la creazione di catene di scambio. Con DXGI, [**l'oggetto IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) controlla che monitora l'uso della catena di scambio quando diventa schermo intero. A differenza di DXGI, Direct3D 9 non aveva alcun concetto di output.

## <a name="window-styles-and-dxgi"></a>Stili di finestra e DXGI

Le applicazioni Direct3D 9 hanno molto da fare quando si passa dalla modalità schermo intero alla modalità finestra. Gran parte di questo lavoro ha comportato la modifica degli stili delle finestre per aggiungere e rimuovere bordi, aggiungere barre di scorrimento e così via. Quando le applicazioni vengono convertire in DXGI e Direct3D 10.x o Direct3D 11.x, questo codice viene spesso lasciato sul posto. A seconda delle modifiche apportate, il passaggio da una modalità all'altra può causare un comportamento imprevisto. Ad esempio, quando si passa alla modalità finestra, l'applicazione potrebbe non avere più un bordo di finestra o cornice nonostante il codice che imposta in modo specifico questi stili. Ciò si verifica perché DXGI ora gestisce gran parte di questo stile cambiando da solo. L'impostazione manuale degli stili di finestra può interferire con DXGI e ciò può causare un comportamento imprevisto.

Il comportamento consigliato è quello di eseguire il meno possibile il lavoro e di consentire a DXGI di gestire la maggior parte dell'interazione con le finestre. Tuttavia, se l'applicazione deve gestire il proprio comportamento di finestra, è possibile usare [**IDXGIFactory::MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation) per indicare a DXGI di disabilitare parte della gestione automatica della finestra.

## <a name="multithreading-and-dxgi"></a>Multithreading e DXGI

È necessario fare particolare attenzione quando si usa DXGI in un'applicazione multithreading per assicurarsi che non si verifichino deadlock. A causa dell'interazione stretta di DXGI con la finestra, invia occasionalmente messaggi di finestra alla finestra dell'applicazione associata. Per poter continuare, DXGI richiede che le modifiche alla finestra si verifichino, quindi userà [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), che è una chiamata sincrona. L'applicazione deve elaborare il messaggio della finestra prima **che venga restituito SendMessage.**

In un'applicazione in cui le chiamate DXGI e il message pump si trova nello stesso thread (o in un'applicazione a thread singolo), è necessario eseguire poco. Quando la chiamata DXGI si trova nello stesso thread del message pump, [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) chiama [*WindowProc della finestra.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) In questo modo il message pump viene ignorato e l'esecuzione può continuare dopo la chiamata a **SendMessage**. Tenere presente che anche le chiamate [**IDXGISwapChain,**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) ad esempio [**IDXGISwapChain::P resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present), vengono considerate chiamate DXGI. DXGI può rinviare il lavoro da [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) o [**ResizeTarget fino**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) a **quando non viene chiamato** Present.

Se la chiamata DXGI e il message pump si verificano in thread diversi, è necessario fare attenzione per evitare deadlock. Quando message pump e SendMessage sono in thread diversi, [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) aggiunge un messaggio alla coda di messaggi della finestra e attende che la finestra elavi il messaggio. Se la routine della finestra è occupata o non viene chiamata dal message pump, il messaggio potrebbe non essere mai elaborato e DXGI attenderà a tempo indeterminato.

Ad esempio, se un'applicazione con message pump in un thread e il relativo rendering in un altro, potrebbe voler cambiare modalità. Il thread message pump indica al thread di rendering di modificare le modalità e attende il completamento della modifica della modalità. Tuttavia, il thread di rendering chiama le funzioni DXGI, che a loro volta chiamano [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), che si blocca fino a quando il message pump non elabora il messaggio. Un deadlock si verifica perché entrambi i thread sono ora bloccati e sono in attesa l'uno sull'altro. Per evitare questo problema, non bloccare mai il message pump. Se un blocco è inevitabile, tutte le interazioni DXGI devono verificarsi nello stesso thread del message pump.

## <a name="gamma-and-dxgi"></a>Gamma e DXGI

Anche se la gamma può essere gestita meglio in Direct3D 10.x o Direct3D 11.x usando trame SRGB, la rampa gamma può comunque essere utile per gli sviluppatori che vogliono un valore gamma diverso da 2.2 o che usano un formato di destinazione di rendering che non supporta SRGB. Tenere presenti due problemi durante l'impostazione della rampa gamma tramite DXGI. Il primo problema è che i valori di rampa passati in [**IDXGIOutput::SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) sono valori float, non **valori WORD.** Assicurarsi inoltre che il codice convertito da Direct3D 9 non tuffi la conversione in **valori WORD** prima di passarli a **SetGammaControl**.

Il secondo problema è che, dopo il passaggio alla modalità schermo intero, [**SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) potrebbe non funzionare, a seconda [**dell'oggetto IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) usato. Quando si cambia modalità schermo intero, DXGI crea un nuovo oggetto di output e usa l'oggetto per tutte le operazioni successive sull'output. Se si **chiama SetGammaControl** su un output enumerato prima di un'opzione di modalità schermo intero, la chiamata non viene indirizzata all'output attualmente in uso da DXGI. Per evitare questo problema, chiamare [**IDXGISwapChain::GetContainingOutput**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput) per ottenere l'output corrente e quindi chiamare **SetGammaControl** dall'output per ottenere il comportamento corretto.

Per informazioni sull'uso della correzione gamma, vedere [Uso della correzione gamma.](/windows/desktop/direct3ddxgi/using-gamma-correction)

## <a name="dxgi-11"></a>DXGI 1.1

Il runtime Direct3D 11 incluso in Windows 7 e installato in Windows Vista (vedere [KB971644](https://support.microsoft.com/kb/971644)) include la versione 1.1 di DXGI. Questo aggiornamento aggiunge definizioni per diversi nuovi formati (in particolare BGRA, distorsione X2 a 10 bit e compressione delle trame BC6H e BC7 di Direct3D 11), nonché una nuova versione delle interfacce factory e adapter DXGI ([**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1), [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1), [**IDXGIAdapter1**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1)) per l'enumerazione delle connessioni Desktop remoto.

Quando si usa Direct3D 11, il runtime userà DXGI 1.1 per impostazione predefinita quando si chiama [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) con un puntatore [**NULL IDXGIAdapter.**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) La combinazione dell'uso di DXGI 1.0 e DXGI 1.1 nello stesso processo non è supportata. La combinazione di istanze di oggetti DXGI da factory diverse nello stesso processo non è supportata. Pertanto, quando si usa DirectX 11, qualsiasi uso esplicito delle interfacce DXGI usa [**un IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) creato dal punto di ingresso [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) in "DXGI.DLL" per garantire che l'applicazione usi sempre DXGI 1.1.

## <a name="dxgi-12"></a>DXGI 1.2

Il runtime Direct3D 11.1 incluso in Windows 8 include anche la versione 1.2 di DXGI.

DXGI 1.2 abilita queste funzionalità:

-   rendering stereo
-   Formati a 16 bit per pixel

    -   DXGI \_ FORMAT \_ B5G6R5 \_ UNORM e DXGI \_ FORMAT \_ B5G5R5A1 \_ UNORM sono ora completamente supportati
    -   è stato aggiunto un nuovo formato DXGI \_ \_ B5G5R5A1 \_ UNORM

-   formati video
-   nuove interfacce DXGI

Per altre informazioni sulle funzionalità di DXGI 1.2, vedere Miglioramenti di [DXGI 1.2.](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

 

 