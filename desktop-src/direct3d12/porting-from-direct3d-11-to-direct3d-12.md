---
title: Conversione da Direct3D 11 a Direct3D 12
description: Questa sezione fornisce alcune indicazioni sulla portabilità da un motore di grafica Direct3D 11 personalizzato a Direct3D 12.
ms.assetid: 9EB4AC6B-AFDD-4673-8EB3-54272C151784
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ccf4a0bd10032d94ecaf4a88cc442f3a7ad516
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812554"
---
# <a name="porting-from-direct3d-11-to-direct3d-12"></a>Conversione da Direct3D 11 a Direct3D 12

Questa sezione fornisce alcune indicazioni sulla portabilità da un motore di grafica Direct3D 11 personalizzato a Direct3D 12.

-   [Creazione del dispositivo](#device-creation)
-   [Risorse di cui è stato eseguito il commit](#committed-resources)
-   [Risorse riservate](#reserved-resources)
-   [Caricamento dei dati](#uploading-data)
-   [Shader e oggetti shader](#shaders-and-shader-objects)
-   [Invio di lavoro alla GPU](#submitting-work-to-the-gpu)
-   [Sincronizzazione CPU/GPU](#cpugpu-synchronization)
-   [Associazione di risorse](#resource-binding)
-   [Stato della risorsa](#resource-state)
-   [Swapchain](#swapchains)
-   [Rendering di funzioni fisse](#fixed-function-rendering)
-   [Probabilità e fine](#odds-and-ends)
-   [Argomenti correlati](#related-topics)

## <a name="device-creation"></a>Creazione del dispositivo

Sia Direct3D 11 che Direct3D 12 condividono un modello di creazione di dispositivi simile. I driver Direct3D 12 esistenti D3D_FEATURE_LEVEL_11_0 o superiore, pertanto è possibile ignorare i livelli di funzionalità precedenti e le limitazioni associate. 

Tenere inoltre presente che con Direct3D 12 è consigliabile enumerare in modo esplicito le informazioni sul dispositivo usando le interfacce DXGI. In Direct3D 11 è possibile eseguire il *concatenamento* al dispositivo DXGI dal dispositivo Direct3D e questo non è supportato per Direct3D 12.

La creazione di un dispositivo software WARP in Direct3D 12 viene eseguita fornendo un adattatore esplicito ottenuto da **IDXGIFactory4::EnumWarpAdapter**. Il dispositivo WARP per Direct3D 12 è disponibile solo nei sistemi con la **funzionalità** facoltativa Strumenti di grafica abilitata.

> [!NOTE]
> Non esiste alcun equivalente a **D3D11CreateDeviceAndSwapChain**. Anche con Direct3D 11, è sconsigliato l'uso di questa funzione perché spesso è meglio creare il dispositivo e lo swapchain in passaggi distinti.

## <a name="committed-resources"></a>Risorse di cui è stato eseguito il commit

Gli oggetti creati con le interfacce seguenti in Direct3D 11 vengono tradotti in "risorse di cui è stato eseguito il commit" in Direct3D 12. Una risorsa di cui è stato eseguito il commit è una risorsa a cui sono associate sia pagine fisiche che spazi di indirizzi virtuali. Si tratta di un concetto del modello di memoria di Microsoft Windows Device Driver 2 (WDD2), su cui si basa Direct3D 12.

Risorse Direct3D 11:

-   [**ID3D11Resource**](/windows/win32/api/d3d11/nn-d3d11-id3d11resource)
-   [**ID3D11Buffer**](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) e [ **ID3D11Device::CreateBuffer**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createbuffer)
-   [**ID3D11Texture1D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture1d) e [ **ID3D11Device:CreateTexture1D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture1d)
-   [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) e [ **ID3D11Device::CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d)
-   [**ID3D11Texture3D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture3d) e [ **ID3D11Device::CreateTexture3D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture3d)

In Direct3D 12 questi sono tutti rappresentati da [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) e [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

## <a name="reserved-resources"></a>Risorse riservate

Le risorse riservate sono risorse in cui è stato allocato solo lo spazio degli indirizzi virtuali, la memoria fisica non viene allocata fino a quando non viene chiamata a [**ID3D12Device::CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap). Si tratta essenzialmente dello stesso concetto delle risorse affiancate in Direct3D 11.

Flag ([**D3D11 \_ RESOURCE \_ MISC \_ FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)) usati in Direct3D 11 per configurare le risorse affiancate, quindi eseguire il mapping alla memoria fisica.

-   RISORSA D3D11 \_ \_ \_ AFFIANCATA
-   POOL DI RIQUADRI \_ \_ MISC DELLA RISORSA \_ D3D11 \_

## <a name="uploading-data"></a>Caricamento dei dati

In Direct3D 11 si ha l'aspetto di una singola sequenza temporale (chiama dopo una sequenza, ad esempio i dati inizializzati con [**D3D11 \_ SUBRESOURCE \_ DATA,**](/windows/win32/api/d3d11/ns-d3d11-d3d11_subresource_data)quindi viene effettuata una chiamata a [**ID3D11DeviceContext::UpdateSubresource**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource)e quindi una chiamata a [**ID3D11DeviceContext::Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)). Il numero di copie create dei dati non è ovvio per uno sviluppatore Direct3D 11.

In Direct3D 12 sono disponibili due sequenze temporali, la sequenza temporale della GPU (impostata dalle chiamate a [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)e [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) dalla memoria mappabile) e la sequenza temporale della CPU (determinata dalle chiamate a [**Map).**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map) Nel file d3dx12.h sono disponibili funzioni helper denominate [**Updatesubresources**](updatesubresources1.md) che usano una sequenza temporale condivisa. Esistono diverse varianti di questa funzione helper, una che usa [**ID3D12Device::GetCopyablePrints,**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)un'altra che usa un meccanismo di allocazione heap e un'altra che usa un meccanismo di allocazione dello stack. Queste funzioni helper copiano le risorse sia nella GPU che nella CPU, tramite un'area di gestione temporanea intermedia della memoria.

In genere la GPU e la CPU hanno ognuna una propria copia di una risorsa associata alla propria sequenza temporale. L'approccio della sequenza temporale condivisa mantiene in modo analogo due copie.

## <a name="shaders-and-shader-objects"></a>Shader e oggetti shader

In Direct3D 11 è presente una grande quantità di creazione di oggetti shader e di stato e l'impostazione dello stato di tali oggetti, usando i metodi di creazione [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) e i metodi set [**ID3D11DeviceContext.**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) In genere viene effettuato un numero elevato di chiamate a questi metodi, che vengono quindi combinati in fase di disegno dal driver per impostare lo stato corretto della pipeline.

In Direct3D 12 questa impostazione dello stato della pipeline è stata combinata in un singolo oggetto ([**CreateComputePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) per un motore di calcolo e [**CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) per un motore di grafica), che viene quindi associato a un elenco di comandi prima della chiamata di disegno con una chiamata a [**SetPipelineState.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)

Queste chiamate sostituiscono tutte le singole chiamate per impostare shader, layout di input, stato di fusione, stato di rasterizzazione, depth stencil stato e così via, in Direct3D 11

- Metodi del dispositivo 11: ``CreateInputLayout`` ``CreateXShader`` , , ``CreateDepthStencilState`` eD ``CreateRasterizerState`` .
- Metodi del contesto di dispositivo 11:  ``IASetInputLayout`` , , , e ``xxSetShader`` ``OMSetBlendState`` ``OMSetDepthStencilState`` ``RSSetState`` .

Anche se Direct3D 12 può supportare i BLOB di shader compilati meno recenti, gli shader devono essere compilati usando il modello shader 5.1 con le API FXC/D3DCompile o usando il modello shader 6 usando il compilatore DXIL DXC. È necessario convalidare il supporto del modello shader 6 [**con CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) **e D3D12_FEATURE_SHADER_MODEL**.

## <a name="submitting-work-to-the-gpu"></a>Invio di lavoro alla GPU

In Direct3D 11 il controllo sul modo in cui viene effettivamente inviato il lavoro è in gran parte gestito dal driver, anche se alcuni controlli sono abilitati tramite le chiamate [**ID3D11DeviceContext::Flush**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-flush) e [**IDXGISwapChain1::P resent1.**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)

In Direct3D 12 l'invio di lavoro è molto esplicito e controllato dall'app. Il costrutto principale per l'invio del lavoro è [**ID3D12GraphicsCommandList,**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)che viene usato per registrare tutti i comandi delle app (ed è piuttosto simile nel concetto al contesto posticipato ID3D11). L'archivio di backup per un elenco di comandi viene fornito da [**ID3D12CommandAllocator,**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)che consente all'app di gestire l'utilizzo della memoria dell'elenco di comandi esponendo effettivamente la memoria che il driver Direct3D 12 userà per archiviare l'elenco dei comandi.

Infine [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) è una coda first-in first-out che archivia l'ordine corretto degli elenchi di comandi per l'invio alla GPU. Solo quando un elenco di comandi ha completato l'esecuzione nella GPU, l'elenco di comandi successivo dalla coda verrà inviato dal driver.

In Direct3D 11 non esiste alcun concetto esplicito di coda di comandi. Nella configurazione comune per Direct3D 12, l'elenco di comandi **D3D12_COMMAND_LIST_TYPE_DIRECT** attualmente aperto per il frame corrente può essere considerato analogo al contesto immediato Direct3D 11. In questo modo vengono fornite molte delle stesse funzioni.


| D3D11DeviceContext                  | ID3D12GraphicsCommand List     |
|-------------------------------------|--------------------------------|
| ClearDepthStencilView               | ClearDepthStencilView          |
| ClearRenderTargetView               | ClearRenderTargetView          |
| ClearUnorderedAccess*               | ClearUnorderedAccess*          |
| Draw, DrawInstanced                 | DrawInstanced                  |
| DrawIndexed, DrawIndexedInstanced   | DrawIndexedInstanced           |
| Dispatch                            | Dispatch                       |
| IASetInputLayout, xxSetShader e così via. | SetPipelineState               |
| OMSetBlendState                     | OMSetBlendFactor               |
| OMSetDepthStencilState              | OMSetStencilRef                |
| OMSetRenderTargets                  | OMSetRenderTargets             |
| RSSetViewports                      | RSSetViewports                 |
| RSSetScissorRects                   | RSSetScissorRects              |
| IASetPrimitiveTopology              | IASetPrimitiveTopology         |
| IASetVertexBuffers                  | IASetVertexBuffers             |
| IASetIndexBuffer                    | IASetIndexBuffer               |
| ResolveSubresource                  | ResolveSubresource             |
| CopySubresourceRegion               | CopyBufferRegion               |
| UpdateSubresource                   | CopyTextureRegion              |
| CopyResource                        | CopyResource                   |

> [!NOTE]
> Un elenco di comandi creato **con D3D12_COMMAND_LIST_TYPE_BUNDLE** è simliar a un contesto posticipato. Direct3D 12 supporta anche l'abiilità di accedere ad alcune  funzionalità di  un contesto immediato simultanee al rendering tramite D3D12_COMMAND_LIST_TYPE_COPY e D3D12_COMMAND_LIST_TYPE_COMPUTE di elenco di comandi. 

## <a name="cpugpu-synchronization"></a>Sincronizzazione CPU/GPU

Nella sincronizzazione CPU/GPU Direct3D 11 era in gran parte automatica e non era necessario che l'app manteneva lo stato della memoria fisica.

in Direct3D 12 l'app deve gestire le due sequenze temporali (CPU e GPU) in modo esplicito. A questo scopo, l'app deve mantenere le informazioni sulle risorse richieste dalla GPU e per quanto tempo. Ciò significa anche che l'app è responsabile di garantire che il contenuto delle risorse (risorse di cui è stato eseguito il commit, heap, allocatori di comandi, ad esempio) non cambi fino a quando la GPU non ha terminato di usarle.

L'oggetto principale per la sincronizzazione delle sequenze temporali è [**l'oggetto ID3D12Fence.**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) Il funzionamento dei recinti è piuttosto semplice e consente alla GPU di segnalare quando è stata completata un'attività. La GPU e la CPU possono entrambi segnalare ed entrambi possono attendere i recinti.

In genere l'approccio consiste nel fatto che quando si invia un elenco di comandi per l'esecuzione, un segnale di recinto viene trasmesso dalla GPU al completamento (al termine della lettura dei dati), consentendo alla CPU di riutilizzare o eliminare le risorse.

In Direct3D 11 il flag [**ID3D11DeviceContext::Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map) D3D11 MAP WRITE DISCARD ha essenzialmente trattato ogni risorsa come un'infinita quantità di memoria in cui l'app può scrivere (un processo noto come \_ \_ \_ "ridenominazione"). In Direct3D 12 il processo è esplicito: è necessario allocare memoria aggiuntiva e usare recinti per sincronizzare le operazioni. I buffer circolare (costituiti da buffer di grandi dimensioni) potrebbero essere una tecnica efficace per questo scopo, fare riferimento allo scenario di buffer circolare in [Fence-Based Resource Management](fence-based-resource-management.md).

![uso di un buffer circolare](images/ring-buffer-1.png)

## <a name="resource-binding"></a>Associazione di risorse

Le viste in Direct3D 11 (visualizzazioni delle risorse shader, visualizzazioni di destinazione di rendering e così via) sono state in gran parte sostituite in Direct3D 12 con il concetto di descrittore. I metodi di creazione esistono ancora in Direct3D 12 (ad esempio [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview) e [**CreateRenderTargetView),**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)che vengono chiamati dopo la creazione dell'heap del descrittore, per scrivere i dati nell'heap. L'associazione in Direct3D 12 viene ora gestita dagli handle del descrittore descritti in una firma radice e inviata tramite i metodi [**SetGraphicsRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) o [**SetComputeRootDescriptorTable.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)

Le firme radice dettaglino i mapping tra il numero di slot della firma radice e le tabelle descrittori, in cui la tabella del descrittore può contenere riferimenti alle risorse disponibili per vertex shader, pixel shader e altri shader, ad esempio buffer costanti, visualizzazioni delle risorse shader e campionatori. Questa flessibilità disconnette lo spazio di registrazione HLSL dallo spazio di associazione dell'API in Direct3D 12, a differenza di Direct3D 11 in cui è presente un mapping uno a uno tra questi.

Una delle implicazioni di questo sistema è che l'app è responsabile della ridenominazione delle tabelle dei descrittori, che consente agli sviluppatori di comprendere il costo delle prestazioni di modifica anche di un singolo descrittore per ogni chiamata di disegno.

Una nuova funzionalità di Direct3D 12 è che un'app può controllare quali descrittori vengono condivisi tra le fasi dello shader. In Direct3D 11 le risorse, ad esempio UAV, sono condivise tra tutte le fasi dello shader. Abilitando la disabilitazione dei descrittori per determinate fasi dello shader, i registri usati dai descrittori disabilitati possono essere usati dai descrittori abilitati per una determinata fase dello shader.

Nella tabella seguente viene illustrata una firma radice di esempio.



| Slot dei parametri radice | Voce tabella descrittore         |
|---------------------|--------------------------------|
| 0                   | Intervallo descrittore VS b0-b13     |
| 1                   | Intervallo descrittore vs t0-t127    |
| 2                   | Vs Descriptor Range s0-s16     |
| 3                   | Intervallo descrittore PS b0-b13     |
| ...                 |                                |
| 14                  | Intervallo descrittore DS s0-16      |
| 15                  | Intervallo descrittore condiviso u0-u63 |



 

## <a name="resource-state"></a>Stato della risorsa

Lo stato della risorsa Direct3D 11 non viene gestito dall'app, ma dal driver.

In Direct3D 12 la gestione dello stato delle risorse diventa responsabilità dell'app, per abilitare il parallelismo completo nella registrazione degli elenchi di comandi: l'app deve gestire le sequenze temporali di registrazione per gli elenchi di comandi (che possono essere eseguite in parallelo) e le sequenze temporali di esecuzione che devono essere sequenziali.

Una transizione dello stato della risorsa viene gestita dal [**metodo ResourceBarrier.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) Principalmente l'app deve informare il driver in caso di modifica dell'utilizzo delle risorse. Ad esempio, se una risorsa viene usata come destinazione di rendering e deve essere usata come input per un vertex shader alla successiva chiamata di disegno, potrebbe essere necessario un breve blocco nell'operazione GPU per completare l'operazione di destinazione di rendering prima di gestire il vertex shader.

Questo sistema consente la sincronizzazione con granularità fine (blocchi GPU) della pipeline grafica, nonché scaricamenti della cache ed eventualmente alcune modifiche al layout della memoria ,ad esempio la visualizzazione della destinazione di rendering depth stencil decompressione della visualizzazione.

Questa operazione è nota come barriera di transizione. Esistono altri tipi di barriere, in Direct3D 11 [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) ha abilitato la stessa memoria fisica per l'uso da parte di due diverse risorse affiancate. In Direct3D 12 questo viene definito "barriera di aliasing". Le barriere di aliasing possono essere usate sia per le risorse affiancate che per le risorse posizionate in Direct3D 12. È inoltre presente la barriera UAV. In Direct3D 11 tutte le operazioni di invio e disegno UAV devono essere serializzate, anche se queste operazioni possono essere eseguite tramite pipeline o funzionare in parallelo. Per Direct3D 12 questa restrizione viene rimossa dall'aggiunta di una barriera UAV. Una barriera UAV garantisce che le operazioni UAV siano sequenziali, quindi se una seconda operazione richiede il primo completamento, la seconda verrà forzata ad attendere dall'aggiunta della barriera. L'operazione predefinita per gli UAV è semplicemente che le operazioni procedono il più rapidamente possibile.

È evidente che si verificano miglioramenti delle prestazioni se un carico di lavoro può essere parallelizzato.

## <a name="swapchains"></a>Swapchain

La catena di scambio DXGI è la base per le catene di scambio in Direct3D 11 e 12. Esistono alcune differenze minori, in Direct3D 11 i tre tipi di catena di scambio sono SEQUENTIAL, DISCARD e FLIP \_ SEQUENTIAL. Per Direct3D 12 sono disponibili solo due tipi: FLIP \_ SEQUENTIAL e FLIP \_ DISCARD. Come indicato in precedenza, è necessario creare in modo esplicito lo swapchain tramite **IDXGIFactory4** o versioni successive e usare la stessa interfaccia per qualsiasi enumerazione dell'adapter.

In Direct3D 11 è presente la rotazione automatica del backbuffer: è necessaria una sola visualizzazione di destinazione di rendering per il buffer nascosto 0. In Direct3D 12 la rotazione del buffer è esplicita e deve essere presente una visualizzazione di destinazione di rendering per ogni buffer nascosto. Usare il [**metodo IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) per selezionare la destinazione di rendering. Anche in questo caso questa flessibilità aggiuntiva consente una maggiore parallelizzazione.

> [!NOTE]
> Anche se esistono diversi modi per configurare l'applicazione, in genere le applicazioni hanno un **ID3D12CommandAllocator** per ogni buffer della catena di scambio. In questo modo l'applicazione può procedere alla creazione di un set di comandi per il frame successivo mentre la GPU esegue il rendering del precedente.

## <a name="fixed-function-rendering"></a>Rendering di funzioni fisse

In Direct3D 11 sono stati semplificati alcuni metodi che semplificano varie operazioni di livello superiore, ad esempio [**GenerateMips**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips) (creazione di catene mip complete) e [**DrawAuto**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto) (usando l'output di flusso come input shader senza ulteriore input dall'app). Questi metodi non sono disponibili in Direct3D 12. L'app deve gestire queste operazioni creando shader per eseguirle.

## <a name="odds-and-ends"></a>Quote e estremità

La tabella seguente illustra una serie di funzionalità simili tra Direct3D 11 e 12, ma non identiche.



| Direct3D 11                                                                            | Direct3D 12                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Query**](/windows/win32/api/d3d11/nn-d3d11-id3d11query)                                              | [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) consente di raggruppare le query, riducendo il costo.                                                                                                                                                                                                                                                                                                                                     |
| [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate)                                      | La predicazione è ora abilitata con i dati in un buffer completamente trasparente. L'oggetto Direct3D 11 [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate) viene sostituito da [**ID3D12Resource::Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map), che deve seguire una chiamata a [**ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) e un'operazione di sincronizzazione GPU usando un limite per attendere che i dati siano pronti. Fare riferimento a [Predication](predication.md). |
| Contatore nascosto UAV/SO                                                                  | L'app è responsabile dell'allocazione e della gestione dei contatori SO/UAV. Fare riferimento a [Contatori di output di flusso](stream-output-counters.md) e [Contatori UAV](uav-counters.md).                                                                                                                                                                                                                                                             |
| MinLOD dinamico della risorsa (livello minimo di dettaglio)                                       | Questa operazione è stata spostata nel descrittore SRV statico MinLOD.                                                                                                                                                                                                                                                                                                                                                                                 |
| Disegno \* [indiretto/DispatchIndirect](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-dispatchindirect) | I metodi indiretti di disegno vengono tutti uniti in un [**unico metodo ExecuteIndirect.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)                                                                                                                                                                                                                                                                                                        |
| I formati DepthStencil sono interleaved                                                   | I formati DepthStencil sono planari. Ad esempio, un formato a 24 bit di profondità, 8 bit di stencil verrebbero archiviati nel formato 24/8/24/8... e così via in Direct3D 11, ma come 24/24/24... seguito da 8/8/8... in Direct3D 12. Si noti che ogni piano è la propria sottorisorsa in D3D12 (vedere [Subresources).](subresources.md)                                                                                                                    |
| [**ResizeTilePool**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)                   | Le risorse riservate possono essere mappate a più heap. Quando un pool di riquadri viene aumentato in D3D11, è invece possibile allocare un heap aggiuntivo in D3D12.                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esercitazioni video di apprendimento avanzato di DirectX: Guida alla portabilità da DirectX 11 a DirectX 12](https://www.youtube.com/watch?v=BV64mdOCgZo)
</dt> <dt>

[Informazioni su Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Uso di Direct3D 11, Direct3D 10 e Direct2D](direct3d-12-interop.md)
</dt> </dl>
