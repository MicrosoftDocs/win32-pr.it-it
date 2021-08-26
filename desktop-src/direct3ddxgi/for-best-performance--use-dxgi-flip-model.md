---
description: Questo argomento fornisce indicazioni per gli sviluppatori su come ottimizzare le prestazioni e l'efficienza nello stack di presentazione nelle versioni moderne di Windows.
ms.assetid: B6B92F4F-B1D0-40B9-987D-F0C0F2CC7AD1
title: Per prestazioni ottimali, usare il modello flip DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: RS5
ms.openlocfilehash: ce999bc735042132902158cfd6bd6d41296d29a3afc98ab27d9480dc6bd8b3b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951221"
---
# <a name="for-best-performance-use-dxgi-flip-model"></a>Per prestazioni ottimali, usare il modello flip DXGI

Questo argomento fornisce indicazioni per gli sviluppatori su come ottimizzare le prestazioni e l'efficienza nello stack di presentazione nelle versioni moderne di Windows. Consente di riprendere il punto in cui il modello di inversione [DXGI,](dxgi-flip-model.md) [DirectX 12: Modalità](https://www.youtube.com/watch?v=E3wTajGZOsA)di presentazione in Windows 10 (video) e Miglioramenti alla presentazione in Windows 10: Un aspetto iniziale [(video)](https://www.youtube.com/watch?v=nUZVV_mssWQ) è stato lasciato.

## <a name="call-to-action"></a>Invito all'azione

Se si usa ancora **DXGI \_ SWAP \_ EFFECT \_ DISCARD** o **DXGI \_ SWAP EFFECT \_ \_ SEQUENTIAL** (ovvero il modello attuale "blt"), è il momento di arrestarsi.

Passaggio a **DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL** o **DXGI \_ SWAP EFFECT FLIP \_ \_ \_ DISCARD** il modello flip) offrirà prestazioni migliori, un minore utilizzo di energia e fornirà un set più avanzato di funzionalità. Per altre informazioni su questi valori, vedere Enumerazione [DXGI \_ SWAP \_ EFFECT.](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)

Il modello flip presenta una modalità a finestra equivalente o migliore rispetto alla modalità classica "esclusiva a schermo intero". In effetti, può essere necessario riconsiderare se l'applicazione necessita effettivamente di una modalità esclusiva a schermo intero, poiché i vantaggi di una finestra senza bordi di un modello di inversione includono un cambio di Alt-Tab più veloce e una migliore integrazione con le moderne funzionalità di visualizzazione.

Perché ora? Prima dell'aggiornamento di aprile 2018, la visualizzazione del modello blt potrebbe causare un'operazione di rimozione visibile se usata nelle configurazioni gpu ibride, spesso presente nei portatili di fascia alta (vedere [KB 3158621](https://support.microsoft.com/help/3158621/hybrid-graphics-and-vsync-results-in-graphic-tearing-in-some-games-and)). Nell'aggiornamento di aprile 2018 questo tearing è stato risolto, a costo di un lavoro aggiuntivo. Se si sta eseguendo blt presenta a framerate elevati tra GPU ibride, in particolare a risoluzioni elevate, ad esempio 4K, questo lavoro aggiuntivo può influire sulle prestazioni complessive. Per garantire prestazioni ottimali in questi sistemi, passare dal modello blt al modello flip present. È anche consigliabile ridurre la risoluzione del swapchain, soprattutto se non è il punto principale di interazione dell'utente(come spesso accade con le finestre di anteprima VR).

## <a name="a-brief-history"></a>Breve cronologia

Che cos'è il modello flip? Qual è l'alternativa?

Prima di Windows 7, l'unico modo per presentare il contenuto da D3D era "blt" o copiarlo in una superficie di proprietà della finestra o dello schermo. A partire dall'effetto flipex swap di D3D9 e passando a DXGI tramite l'effetto di scambio FLIP SEQUENTIAL in Windows 8, è stato sviluppato un modo più efficiente per inserire il contenuto sullo schermo condividendo il contenuto direttamente con il \_ compositore desktop, con copie minime. Per una panoramica generale della tecnologia, vedere Modello flip [DXGI.](dxgi-flip-model.md)

Questa ottimizzazione è possibile grazie al DWM (Gestione finestre desktop), che è il compositore che guida il Windows desktop.

## <a name="when-should-i-use-the-blt-model"></a>Quando usare il modello blt?

C'è una funzionalità che il modello flip non offre: la possibilità di avere più API diverse che producono contenuto, che tutti stratno insieme nello stesso **HWND,** in base a una base attuale. Un esempio di questo potrebbe essere l'uso di D3D per disegnare uno sfondo della finestra e quindi Windows [GDI per](/windows/desktop/gdi/windows-gdi) disegnare qualcosa sopra o usando due API grafiche diverse, o due swapchain della stessa API, per produrre fotogrammi alternati. Se non è necessaria l'interoperabilità a livello **di HWND** tra i componenti grafici, non è necessario un modello blt.

Esiste un secondo componente di funzionalità che non è stato fornito nella progettazione originale del modello flip, ma è ora disponibile, ovvero la possibilità di presentare a una velocità di fotogramma non impostata. Per un'applicazione che usa l'intervallo di sincronizzazione 0, non è consigliabile passare al modello di inversione a meno che non sia disponibile l'API [IDXGIFactory5::CheckFeatureSupport](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) e non venga restituito il supporto per LA FUNZIONALITÀ **DXGI \_ PRESENT ALLOW \_ \_ \_ TEARING**. Questa funzionalità è quasi onnipresente nelle versioni recenti di Windows 10 e nell'hardware moderno.

## <a name="directflip"></a>DirectFlip

Se si è visto [DirectX 12: Modalità](https://www.youtube.com/watch?v=E3wTajGZOsA)di presentazione in Windows 10 , verrà visualizzato "Direct Flip" e "Independent Flip". Si tratta di ottimizzazioni abilitate per le applicazioni che usano swapchain di modelli flip. A seconda della configurazione della finestra e del buffer, è possibile ignorare completamente la composizione del desktop e inviare direttamente i fotogrammi dell'applicazione allo schermo, come fa l'esclusivo schermo intero.

Queste ottimizzazioni possono essere in questi giorni in uno dei tre scenari seguenti, in ordine di funzionalità crescente:

1.  **DirectFlip:** i buffer swapchain corrispondono alle dimensioni dello schermo e l'area client della finestra copre lo schermo. Invece di usare lo swapchain DWM da visualizzare sullo schermo, viene usato lo swapchain dell'applicazione.
2.  **DirectFlip con** pannelli infitter: l'area client della finestra copre lo schermo e i buffer swapchain si trova all'interno di un fattore di ridimensionamento dipendente dall'hardware (ad esempio, da 0,25 x a 4x) dello schermo. L'hardware di analisi GPU viene usato per ridimensionare il buffer durante l'invio allo schermo.
3.  **DirectFlip con sovrapposizione multi-piano (MPO):** i buffer swapchain si trova all'interno di un fattore di scala dipendente dall'hardware delle dimensioni della finestra. DWM è in grado di riservare un piano di analisi hardware dedicato per l'applicazione, che viene quindi analizzato e potenzialmente allungato in una sottoarea dello schermo con alpha blended.

Con il modello di capovolgimento finestra, l'applicazione può eseguire query sul supporto hardware per diversi scenari DirectFlip e implementare diversi tipi di ridimensionamento dinamico tramite l'uso di [IDXGIOutput6::CheckHardwareCompositionSupport](/windows/desktop/api/DXGI1_6/nf-dxgi1_6-idxgioutput6-checkhardwarecompositionsupport). Un'avvertenza da tenere presente è che se vengono utilizzati pannelli infitter, è possibile che il cursore subisca effetti collaterali di stretching, indicato tramite **DXGI \_ HARDWARE COMPOSITION SUPPORT FLAG CURSOR \_ \_ \_ \_ \_ STRETCHED**.

Dopo che lo swapchain è stato "DirectFlipped", il DWM può passare alla sospensione e riattivarsi solo quando qualcosa cambia all'esterno dell'applicazione. I frame dell'applicazione vengono inviati direttamente allo schermo, in modo indipendente, con la stessa efficienza dell'esclusiva a schermo intero. Si tratta di "Independent Flip" e può essere utilizzato in tutti gli scenari precedenti. Se si verificano altri contenuti desktop, il DWM può tornare facilmente alla modalità composta, "invertire" in modo efficiente il contenuto sopra l'applicazione prima di capovolgerlo o sfruttare MPO per mantenere la modalità di capovolgimento indipendente.

Vedere lo strumento [PresentMon](https://github.com/GameTechDev/PresentMon) per ottenere informazioni dettagliate su quale degli elementi precedenti è stato usato.

## <a name="what-else-is-new-in-the-flip-model"></a>Quali altre novità del modello flip?

Oltre ai miglioramenti precedenti, che si applicano agli swapchain standard senza alcuna particolarità, sono disponibili diverse funzionalità per l'uso da parte delle applicazioni modello flip:

-   Riduzione della latenza tramite **DXGI \_ SWAP CHAIN FLAG FRAME \_ \_ \_ \_ LATENCY \_ WAITABLE \_ OBJECT**. In modalità Flip indipendente è possibile ottenere fino a 1 fotogramma di latenza nelle versioni recenti di Windows, con fallback normale al minimo possibile quando composto.
    -   Avvertenza: si è verificato un problema che ha fornito almeno due fotogrammi di latenza nell'aggiornamento Windows 10'anniversario e versioni precedenti. Per [altre informazioni, vedere](https://www.gamedev.net/forums/topic/686507-windows-10-dx12-low-latency-tearing-free-rendering/) questo argomento del forum. Questo problema è stato risolto in Fall Creator's Update.
-   **DXGI \_ SWAP \_ EFFECT FLIP DISCARD \_ \_ abilita** una modalità di "composizione inversa" di capovolgimento diretto, che comporta un lavoro meno complessivo per visualizzare il desktop. DWM può eseguire lo scribble nei buffer dell'applicazione e inviarli alla schermata, anziché eseguire una copia completa nei propri swapchain.
-   **DXGI \_ SWAP \_ CHAIN FLAG ALLOW \_ \_ \_ TEARING** può abilitare una latenza ancora più bassa rispetto all'oggetto waitable, anche in una finestra nei sistemi con supporto della sovrapposizione su più piani.
-   Le applicazioni hanno il controllo sul ridimensionamento del contenuto che si verifica durante il ridimensionamento della finestra, usando la proprietà [DXGI \_ SCALING](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling) impostata durante la creazione dello swapchain.
-   Il contenuto nei formati HDR (R10G10B10A2 UNORM o \_ R16G16B16A16 FLOAT) non viene ancorato a meno che non sia composto da un \_ desktop SDR.
-   Le statistiche presenti sono disponibili in modalità finestra.
-   È disponibile una maggiore compatibilità con il modello di applicazione UWP (Universal Windows Platform) e DX12 perché sono compatibili solo con il modello flip.

## <a name="what-do-i-have-to-do-to-use-the-flip-model"></a>Cosa è necessario fare per usare il modello flip?

Gli swapchain del modello flip hanno alcuni requisiti aggiuntivi per gli swapchain blt:

1.  Il numero di buffer deve essere almeno 2.
2.  Dopo [le chiamate](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) present, il buffer nascosto deve essere associato in modo esplicito al contesto immediato D3D11 prima di poterlo usare di nuovo.
3.  Dopo aver chiamato [SetFullscreenState,](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)l'applicazione deve chiamare [ResizeBuffers](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) prima di **Present**.
4.  Gli swapchain MSAA (multisample anti-aliasing) non sono supportati direttamente nel modello flip, quindi l'applicazione dovrà eseguire una risoluzione MSAA prima di rilasciare **present**.

## <a name="how-to-choose-the-right-rendering-and-presentation-resolutions"></a>Come scegliere le risoluzioni di rendering e presentazione giuste

Il modello tradizionale per le applicazioni in passato è stato quello di fornire all'utente un elenco di risoluzioni tra cui scegliere quando l'utente seleziona la modalità schermo intero esclusiva. Con la possibilità degli schermi moderni di iniziare facilmente il ridimensionamento del contenuto, è consigliabile offrire agli utenti la possibilità di scegliere una risoluzione di rendering per il ridimensionamento delle prestazioni, indipendente da una risoluzione di output e anche in modalità a finestre. Inoltre, le applicazioni devono sfruttare **IDXGIOutput6::CheckHardwareCompositionSupport** per determinare se è necessario ridimensionare il contenuto prima di presentarlo o se devono consentire all'hardware di eseguire il ridimensionamento.

Potrebbe essere necessario eseguire la migrazione del contenuto da una GPU a un'altra come parte dell'operazione di composizione o presente. Questo vale spesso nei computer portatili multi-GPU o nei sistemi con GPU esterne collegate. Con l'aumentare delle dimensioni di queste configurazioni e con l'aumentare del numero di schermi ad alta risoluzione, aumenta il costo della presentazione di uno swapchain con risoluzione completa. Se la destinazione del swapchain non è il punto principale di interazione dell'utente, come spesso accade con i titoli VR che presentano un'anteprima 2D della scena VR in una finestra secondaria, è consigliabile usare uno swapchain a risoluzione inferiore per ridurre al minimo la quantità di larghezza di banda che deve essere trasferita tra GPU diverse.

## <a name="other-considerations"></a>Altre considerazioni

La prima volta che si chiede alla GPU di scrivere nel buffer nascosto dello swapchain è il momento in cui la GPU si blocca in attesa che il buffer diventi disponibile. Quando possibile, ritardare questo punto il più lontano possibile nel frame.

 

 
