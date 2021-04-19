---
description: Questo argomento fornisce indicazioni per gli sviluppatori su come ottimizzare le prestazioni e l'efficienza nello stack di presentazione nelle versioni moderne di Windows.
ms.assetid: B6B92F4F-B1D0-40B9-987D-F0C0F2CC7AD1
title: Per ottenere prestazioni ottimali, usare DXGI flip model
ms.topic: article
ms.date: 05/31/2018
ms.custom: RS5
ms.openlocfilehash: 2a1e671c03f468fd62b0b5bad0f008f84e62ca3c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303914"
---
# <a name="for-best-performance-use-dxgi-flip-model"></a>Per ottenere prestazioni ottimali, usare DXGI flip model

Questo argomento fornisce indicazioni per gli sviluppatori su come ottimizzare le prestazioni e l'efficienza nello stack di presentazione nelle versioni moderne di Windows. Viene rilevata la posizione in cui [DXGI flip model](dxgi-flip-model.md), [DirectX 12: Presentation Modes in Windows 10 (video)](https://www.youtube.com/watch?v=E3wTajGZOsA)e i [miglioramenti della presentazione in Windows 10: un primo aspetto (video)](https://www.youtube.com/watch?v=nUZVV_mssWQ) interrotto.

## <a name="call-to-action"></a>Invito all'azione

Se si sta ancora usando **DXGI \_ swap \_ Effect \_ scarto** o **DXGI \_ swap \_ Effect \_ sequenziale** (noto anche come il modello present "BLT"), è giunto il momento di arrestarsi.

Passare a **DXGI \_ swap \_ Effect \_ Flip \_ sequenziale** o **DXGI \_ swap \_ Effect \_ Flip \_ ignorate** (noto anche come il modello Flip) offrirà prestazioni migliori, una riduzione dell'utilizzo di energia e un set più completo di funzionalità. Per ulteriori informazioni su questi valori, vedere [ \_ enumerazione DXGI swap \_ Effect](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) .

Flip model Presents Go per quanto riguarda la modalità finestra in modo efficace equivalente o migliore rispetto alla modalità classica "esclusiva a schermo intero". In realtà, può essere utile riconsiderare se l'applicazione necessita effettivamente di una modalità esclusiva a schermo intero, perché i vantaggi di una finestra senza bordi del modello sono più veloci Alt-Tab il cambio e una migliore integrazione con le funzionalità di visualizzazione moderne.

Perché ora? Prima dell'aggiornamento del 2018 aprile, il modello BLT presentava un effetto di strappo visibile se usato nelle configurazioni GPU ibride, spesso disponibile nei portatili di fascia alta (vedere [KB 3158621](https://support.microsoft.com/help/3158621/hybrid-graphics-and-vsync-results-in-graphic-tearing-in-some-games-and)). Nell'aggiornamento di aprile 2018, questo strappo è stato risolto, a scapito di alcune operazioni aggiuntive. Se si esegue BLT presenta un framerate elevato tra GPU ibride, soprattutto a risoluzioni elevate, ad esempio 4K, questo lavoro aggiuntivo può influire sulle prestazioni complessive. Per garantire prestazioni ottimali in questi sistemi, passare dal BLT al modello Flip present. Inoltre, è consigliabile ridurre la risoluzione dei presentazione catena, soprattutto se non è il punto principale di interazione dell'utente (come spesso accade con le finestre di anteprima di VR).

## <a name="a-brief-history"></a>Una breve cronologia

Che cos'è il modello Flip? Qual è l'alternativa?

Prima di Windows 7, l'unico modo per presentare il contenuto da D3D era "BLT" o copiarlo in una superficie di proprietà della finestra o dello schermo. A partire dall'effetto di swap FLIPEX di D3D9's e passando a DXGI tramite l' \_ effetto di scambio sequenziale Flip in Windows 8, abbiamo sviluppato un modo più efficiente per inserire il contenuto sullo schermo condividendo il contenuto direttamente con il compositor desktop, con copie minime. Vedere [DXGI flip model](dxgi-flip-model.md) per una panoramica di alto livello della tecnologia.

Questa ottimizzazione è possibile grazie a DWM (Gestione finestre desktop), ovvero il compositor che guida il desktop di Windows.

## <a name="when-should-i-use-the-blt-model"></a>Quando è consigliabile utilizzare il modello BLT?

Esiste una delle funzionalità che il modello Flip non fornisce: la possibilità di avere più API che producono contenuto, che tutti i livelli nello stesso **HWND**, su base attuale. Un esempio di questo approccio consiste nell'usare D3D per creare uno sfondo della finestra, quindi [Windows GDI](/windows/desktop/gdi/windows-gdi) per creare un elemento in primo piano o per usare due API grafiche diverse o due le catene dalla stessa API, per produrre frame alternativi. Se non è necessaria l'interoperabilità a livello di **HWND** tra i componenti grafici, non è necessario il modello BLT.

Esiste una seconda funzionalità che non è stata fornita nella progettazione del modello Flip originale, ma è ora disponibile, che è la possibilità di presentare un framerate non limitato. Per un'applicazione che usa l'intervallo di sincronizzazione 0, non è consigliabile passare a capovolgere il modello a meno che non sia disponibile l'API [IDXGIFactory5:: CheckFeatureSupport](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) e il supporto dei report per la **\_ funzionalità DXGI \_ \_ consenta lo \_ strappo**. Questa funzionalità è quasi onnipresente nelle versioni recenti di Windows 10 e nell'hardware moderno.

## <a name="directflip"></a>DirectFlip

Se sono state osservate le [modalità di presentazione di DirectX 12 in Windows 10](https://www.youtube.com/watch?v=E3wTajGZOsA), verrà visualizzato il discorso "Direct Flip" e "Independent Flip". Si tratta di ottimizzazioni abilitate per le applicazioni che usano il modello Flip le catene. A seconda della configurazione della finestra e del buffer, è possibile ignorare completamente la composizione del desktop e inviare direttamente i frame dell'applicazione allo schermo, nello stesso modo in cui viene utilizzato lo schermo a schermo intero esclusivo.

Questi giorni, queste ottimizzazioni possono impegnarsi in uno dei tre scenari, per aumentare le funzionalità:

1.  **DirectFlip**: i buffer presentazione catena corrispondono alle dimensioni dello schermo e l'area client della finestra copre la schermata. Anziché utilizzare DWM presentazione catena per visualizzare sullo schermo, viene utilizzata l'applicazione presentazione catena.
2.  **DirectFlip con** gli adattatori del pannello: l'area client della finestra copre lo schermo e i buffer presentazione catena rientrano in un fattore di scala dipendente dall'hardware (ad esempio, 0,25 x a 4x) dello schermo. L'hardware di analisi GPU viene usato per ridimensionare il buffer mentre lo si invia alla visualizzazione.
3.  **DirectFlip con sovrapposizione multipiano (MPO)**: i buffer presentazione catena sono all'interno di un fattore di scala dipendente dall'hardware delle dimensioni della finestra. DWM è in grado di riservare un piano dedicato di analisi dell'hardware per l'applicazione, che viene quindi sottoposta a scansione e potenzialmente allungata a un'area secondaria con Alpha Blend dello schermo.

Con il modello Flip a finestra, l'applicazione può eseguire query sul supporto hardware per diversi scenari DirectFlip e implementare tipi diversi di scalabilità dinamica tramite l'uso di [IDXGIOutput6:: CheckHardwareCompositionSupport](/windows/desktop/api/DXGI1_6/nf-dxgi1_6-idxgioutput6-checkhardwarecompositionsupport). Un avvertimento da tenere presente è che se gli installatori di pannelli vengono utilizzati, è possibile che il cursore soffra degli effetti collaterali, che è indicato tramite il **cursore del \_ flag di supporto della composizione hardware DXGI \_ \_ \_ \_ \_ esteso**.

Una volta che il presentazione catena è stato "DirectFlipped", lo strumento DWM può passare alla modalità di sospensione e riattivarsi solo quando vengono apportate modifiche all'esterno dell'applicazione. I frame dell'applicazione vengono inviati direttamente allo schermo, in modo indipendente, con la stessa efficienza dell'esclusiva a schermo intero. Si tratta di un "Flip indipendente" e può interagire con tutti gli scenari descritti in precedenza. Se sono disponibili altri contenuti desktop, DWM può eseguire facilmente la transizione alla modalità composta, "invertire la composizione" del contenuto sopra l'applicazione prima di ingrandirla o utilizzare MPO per gestire la modalità Flip indipendente.

Vedere lo strumento [PresentMon](https://github.com/GameTechDev/PresentMon) per ottenere informazioni dettagliate su come è stato usato.

## <a name="what-else-is-new-in-the-flip-model"></a>Quali sono le altre novità del modello Flip?

Oltre ai miglioramenti descritti in precedenza, che si applicano a le catene standard senza alcuna operazione speciale, sono disponibili diverse funzionalità per l'uso delle applicazioni flip model:

-   Riduzione della latenza utilizzando l' **\_ \_ \_ \_ \_ \_ \_ oggetto waitable frame flag della catena di scambio DXGI**. In modalità Flip indipendente, è possibile arrivare fino a 1 frame di latenza nelle versioni recenti di Windows, con il fallback normale al minimo possibile quando composto.
    -   Avvertenza: si è verificato un problema che ha fornito almeno due fotogrammi di latenza nell'aggiornamento dell'anniversario di Windows 10 e versioni precedenti. Per ulteriori informazioni, vedere [questo argomento del forum](https://www.gamedev.net/forums/topic/686507-windows-10-dx12-low-latency-tearing-free-rendering/) . Questo problema è stato risolto nell'aggiornamento del creatore della ricadenza.
-   **DXGI \_ SWAP \_ Effect \_ Flip \_ Ignora** consente la modalità "composizione inversa" del flip diretto, il che comporta un minor lavoro complessivo per la visualizzazione del desktop. DWM può scarabocchiare sui buffer dell'applicazione e inviarli allo schermo, anziché eseguire una copia completa nella propria le catene.
-   **DXGI \_ Il \_ flag chain di scambio \_ \_ consente lo \_ strappo** può consentire una latenza ancora inferiore rispetto all'oggetto waitable, anche in una finestra nei sistemi con supporto di sovrimpressione a più livelli.
-   Le applicazioni hanno il controllo sulla scalabilità del contenuto che si verifica durante il ridimensionamento della finestra, usando la proprietà [DXGI \_ scaling](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling) impostata durante la creazione del presentazione catena
-   Il contenuto in formati HDR (R10G10B10A2 \_ UNORM o R16G16B16A16 \_ float) non viene bloccato a meno che non sia composto da un desktop SDR.
-   Le statistiche presenti sono disponibili in modalità finestra.
-   Esiste una maggiore compatibilità con il modello di applicazione UWP (piattaforma UWP (Universal Windows Platform)) e DX12, poiché sono compatibili solo con il modello flip.

## <a name="what-do-i-have-to-do-to-use-the-flip-model"></a>Cosa devo fare per usare il modello Flip?

Capovolgere il modello le catene presenta alcuni requisiti aggiuntivi oltre al le catene BLT:

1.  Il numero di buffer deve essere almeno 2.
2.  Dopo [le](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) chiamate a, il buffer nascosto deve essere riassociato in modo esplicito al contesto immediato d3d11 prima di poterlo usare nuovamente.
3.  Dopo la chiamata a [SetFullscreenState](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate), l'applicazione deve chiamare [ResizeBuffers](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) prima di essere **presente**.
4.  MSAA (anti-aliasing di multicampionamento) le catene non sono supportati direttamente nel modello Flip, quindi l'applicazione deve eseguire una risoluzione MSAA prima di emettere il **presente**.

## <a name="how-to-choose-the-right-rendering-and-presentation-resolutions"></a>Come scegliere le risoluzioni per il rendering e la presentazione corrette

Il modello tradizionale per le applicazioni in passato è stato quello di fornire all'utente un elenco di risoluzioni da scegliere quando l'utente seleziona la modalità a schermo intero esclusivo. Con la possibilità di visualizzare i moderni per iniziare a ridimensionare facilmente il contenuto, è consigliabile fornire agli utenti la possibilità di scegliere una risoluzione per il rendering per il ridimensionamento delle prestazioni, indipendente dalla risoluzione dell'output e persino in modalità finestra. Inoltre, le applicazioni devono utilizzare **IDXGIOutput6:: CheckHardwareCompositionSupport** per determinare se è necessario ridimensionare il contenuto prima di presentarlo o se devono consentire all'hardware di eseguire il ridimensionamento.

Potrebbe essere necessario eseguire la migrazione del contenuto da una GPU a un'altra come parte dell'operazione presente o di composizione. Questo problema si verifica spesso nei computer portatili con più GPU oppure nei sistemi con GPU esterne collegate. Man mano che queste configurazioni diventano più comuni e, poiché i display ad alta risoluzione diventano più comuni, aumenta il costo della presentazione di un presentazione catena di risoluzione completa. Se la destinazione del presentazione catena non è il punto principale di interazione dell'utente, come spesso accade con i titoli VR che presentano un'anteprima 2D della scena VR in una finestra secondaria, provare a usare un presentazione catena di risoluzione inferiore per ridurre al minimo la quantità di larghezza di banda che deve essere trasferita tra GPU diverse.

## <a name="other-considerations"></a>Altre considerazioni

La prima volta che si chiede alla GPU di scrivere nel buffer nascosto presentazione catena è il momento in cui la GPU resterà in attesa che il buffer diventi disponibile. Quando possibile, ritardare questo punto fino al frame possibile.

 

 
