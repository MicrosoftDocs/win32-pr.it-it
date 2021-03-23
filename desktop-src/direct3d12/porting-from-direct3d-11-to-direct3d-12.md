---
title: Conversione da Direct3D 11 a Direct3D 12
description: In questa sezione vengono fornite alcune indicazioni sul porting da un motore di grafica Direct3D 11 personalizzato a Direct3D 12.
ms.assetid: 9EB4AC6B-AFDD-4673-8EB3-54272C151784
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b5bc6784d6f96c3c1599a601a57bf68b0d612d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548870"
---
# <a name="porting-from-direct3d-11-to-direct3d-12"></a>Conversione da Direct3D 11 a Direct3D 12

In questa sezione vengono fornite alcune indicazioni sul porting da un motore di grafica Direct3D 11 personalizzato a Direct3D 12.

-   [Creazione del dispositivo](#device-creation)
-   [Risorse sottoposte a commit](#committed-resources)
-   [Risorse riservate](#reserved-resources)
-   [Caricamento dei dati](#uploading-data)
-   [Shader e oggetti shader](#shaders-and-shader-objects)
-   [Invio di lavoro alla GPU](#submitting-work-to-the-gpu)
-   [Sincronizzazione CPU/GPU](#cpugpu-synchronization)
-   [Associazione di risorse](#resource-binding)
-   [Stato risorsa](#resource-state)
-   [Le catene](#swapchains)
-   [Correzione del rendering della funzione](#fixed-function-rendering)
-   [Probabilità e fine](#odds-and-ends)
-   [Argomenti correlati](#related-topics)

## <a name="device-creation"></a>Creazione del dispositivo

Direct3D 11 e Direct3D 12 condividono un modello di creazione del dispositivo simile. I driver Direct3D 12 esistenti sono tutti **D3D_FEATURE_LEVEL_11_0** o meglio, quindi è possibile ignorare i livelli di funzionalità precedenti e i lmitations associati.

Tenere inoltre presente che con Direct3D 12 è necessario enumerare in modo esplicito le informazioni sul dispositivo usando le interfacce DXGI. In Direct3D 11, è possibile *concatenare* il dispositivo DXGI dal dispositivo Direct3D e questa operazione non è supportata per Direct3D 12.

La creazione di un dispositivo software WARP in Direct3D 12 viene eseguita fornendo una scheda esplicita ottenuta da **IDXGIFcatory4:: EnumWarpAdapter**. Il dispositivo WARP per Direct3D 12 è disponibile solo nei sistemi con la funzionalità facoltativa **strumenti di grafica** abilitata.

> [!NOTE]
> Non esiste alcun equivalente a **D3D11CreateDeviceAndSwapChain**. Anche con Direct3D 11, si sconsiglia l'uso di questa funzione perché è spesso preferibile creare il dispositivo e presentazione catena in passaggi distinti.

## <a name="committed-resources"></a>Risorse sottoposte a commit

Gli oggetti creati con le interfacce seguenti in Direct3D 11, si traducono in quelli denominati "risorse vincolate" in Direct3D 12. Una risorsa di cui è stato eseguito il commit è una risorsa a cui sono associati sia lo spazio degli indirizzi virtuale che le pagine fisiche. Si tratta di un concetto di modello di memoria di Microsoft Windows Device Driver 2 (WDD2) su cui si basa Direct3D 12.

Risorse Direct3D 11:

-   [**ID3D11Resource**](/windows/win32/api/d3d11/nn-d3d11-id3d11resource)
-   [**ID3D11Buffer**](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) e [ **ID3D11Device:: CreateBuffer**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createbuffer)
-   [**ID3D11Texture1D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture1d) e [ **ID3D11Device: CreateTexture1D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture1d)
-   [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) e [ **ID3D11Device:: CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d)
-   [**ID3D11Texture3D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture3d) e [ **ID3D11Device:: CreateTexture3D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture3d)

In Direct3D 12 queste sono tutte rappresentate da [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) e [**ID3D12Device:: CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

## <a name="reserved-resources"></a>Risorse riservate

Le risorse riservate sono risorse in cui è stato allocato solo lo spazio degli indirizzi virtuali. la memoria fisica non viene allocata fino a quando non viene chiamata a [**ID3D12Device:: createheap ha provocato**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap). Si tratta essenzialmente dello stesso concetto di risorse affiancate in Direct3D 11.

Flag ([**d3d11 \_ Resource \_ varie \_ flag**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)) usati in Direct3D 11 per configurare le risorse affiancate, quindi eseguirne il mapping alla memoria fisica.

-   \_Varie risorse \_ d3d11 \_ affiancate
-   \_Pool di \_ \_ sezioni varie della risorsa \_ d3d11

## <a name="uploading-data"></a>Caricamento dei dati

In Direct3D 11 esiste l'aspetto di una singola sequenza temporale (chiama dopo una sequenza, ad esempio i dati inizializzati con [**\_ \_ i dati della sottorisorsa d3d11**](/windows/win32/api/d3d11/ns-d3d11-d3d11_subresource_data), quindi viene effettuata una chiamata a [**sul ID3D11DeviceContext:: UpdateSubresource**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource)e quindi una chiamata a [**sul ID3D11DeviceContext:: Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)). Il numero di copie create dai dati non è ovvio per uno sviluppatore Direct3D 11.

In Direct3D 12 sono presenti due sequenze temporali, la sequenza temporale della GPU (configurata dalle chiamate a [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)e [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) da mappabili Memory) e la sequenza temporale della CPU (determinata dalle chiamate a [**Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)). Vengono fornite funzioni di supporto (nel file d3dx12. h) denominate [**updatesubresources con**](updatesubresources1.md) che usano una sequenza temporale condivisa. Esistono diverse varianti di questa funzione helper, una che usa [**ID3D12Device:: GetCopyableFootprints**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints), un'altra che usa un meccanismo di allocazione dell'heap e un'altra che usa un meccanismo di allocazione dello stack. Queste funzioni helper copiano le risorse sia sulla GPU che sulla CPU, tramite un'area di gestione temporanea intermedia di memoria.

In genere, la GPU e la CPU hanno ciascuna una propria copia di una risorsa legata alla propria sequenza temporale. L'approccio della sequenza temporale condivisa gestisce in modo analogo due copie.

## <a name="shaders-and-shader-objects"></a>Shader e oggetti shader

In Direct3D 11 sono disponibili numerose attività di creazione di shader e di oggetti di stato e l'impostazione dello stato di tali oggetti, usando i metodi di creazione [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) e i metodi set [**sul ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) . Viene in genere eseguito un numero elevato di chiamate a questi metodi, che vengono quindi combinati in fase di estrazione dal driver per impostare lo stato corretto della pipeline.

In Direct3D 12 questa impostazione dello stato della pipeline è stata combinata in un singolo oggetto ([**CreateComputePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) per un motore di calcolo e [**CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) per un motore di grafica), che viene quindi collegato a un elenco di comandi prima della chiamata di progetto con una chiamata a [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

Queste chiamate sostituiscono tutte le singole chiamate per impostare shader, layout di input, stato di Blend, stato di rasterizzazione, stato di depth stencil e così via, in Direct3D 11

- Metodi Device 11: ``CreateInputLayout`` , ``CreateXShader`` , ``CreateDepthStencilState`` , andd ``CreateRasterizerState`` .
- Metodi del contesto di dispositivo 11:  ``IASetInputLayout`` , ``xxSetShader`` , ``OMSetBlendState`` , ``OMSetDepthStencilState`` e ``RSSetState`` .

Sebbene Direct3D 12 possa supportare i BLOB dello shader compilati meno recenti, gli shader devono essere compilati usando il modello di shader 5,1 con le API FXC/D3DCompile o usando il modello di shader 6 usando il compilatore DXC di DXIL. È necessario convalidare il supporto del modello di shader 6 con [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) e **D3D12_FEATURE_SHADER_MODEL**.

## <a name="submitting-work-to-the-gpu"></a>Invio di lavoro alla GPU

in Direct3D 11 il controllo sul modo in cui viene inviato il lavoro viene gestito in gran parte dal driver, anche se alcuni controlli sono abilitati tramite le chiamate a [**sul ID3D11DeviceContext:: Flush**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-flush) e [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) .

In Direct3D 12 l'invio del lavoro è molto esplicito e controllato dall'app. Il costrutto principale per l'invio del lavoro è [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist), che viene usato per registrare tutti i comandi delle app (ed è molto simile a quello del contesto posticipato di ID3D11). L'archivio di backup per un elenco di comandi viene fornito da [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator), che consente all'app di gestire l'utilizzo della memoria dell'elenco di comandi esponendo effettivamente la memoria che il driver Direct3D 12 utilizzerà per archiviare l'elenco dei comandi.

Infine, [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) è una coda First-in First-out, che archivia l'ordine corretto degli elenchi di comandi per l'invio alla GPU. Solo quando un elenco di comandi ha completato l'esecuzione sulla GPU, l'elenco dei comandi successivi dalla coda verrà inviato dal driver.

In Direct3D 11 non esiste alcun concetto esplicito di coda dei comandi. Nel programma di installazione comune per Direct3D 12, l'elenco di comandi attualmente aperti **D3D12_COMMAND_LIST_TYPE_DIRECT** per il frame corrente può essere considerato analogo al contesto immediato di Direct3D 11. In questo modo vengono fornite molte delle stesse funzioni.


| Su D3D11DeviceContext                  | Elenco ID3D12GraphicsCommand     |
|-------------------------------------|--------------------------------|
| ClearDepthStencilView               | ClearDepthStencilView          |
| ClearRenderTargetView               | ClearRenderTargetView          |
| ClearUnorderedAccess*               | ClearUnorderedAccess*          |
| DrawInstanced                 | DrawInstanced                  |
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
> Un elenco di comandi creato con **D3D12_COMMAND_LIST_TYPE_BUNDLE** viene simile a un contesto posticipato. Direct3D 12 supporta inoltre abiilty per accedere ad alcune funzionalità di un *contesto immediato* simultaneamente al rendering tramite **D3D12_COMMAND_LIST_TYPE_COPY** e **D3D12_COMMAND_LIST_TYPE_COMPUTE** tipi di elenco dei comandi.

## <a name="cpugpu-synchronization"></a>Sincronizzazione CPU/GPU

In Direct3D 11 la sincronizzazione della CPU/GPU era in gran parte automatica e non era necessario che l'app mantenga lo stato della memoria fisica.

in Direct3D 12 l'app deve gestire in modo esplicito le due sequenze temporali (CPU e GPU). Questa operazione richiede che le informazioni debbano essere mantenute, dall'app, sulle risorse richieste dalla GPU e per quanto tempo. Questo significa anche che l'app è responsabile di garantire che il contenuto delle risorse (ad esempio, risorse sottoposte a commit, heap, allocatori di comandi) non cambi fino a quando la GPU non ne ha terminato l'uso.

L'oggetto principale per la sincronizzazione delle sequenze temporali è l'oggetto [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) . L'operazione di recinzione è semplice, ma consente alla GPU di segnalare il completamento di un'attività. La GPU e la CPU possono entrambi segnalare ed è possibile attendere le recinzioni.

In genere, l'approccio consiste nel fatto che quando si invia un elenco di comandi per l'esecuzione, un segnale di recinzione viene trasmesso dalla GPU al completamento (al termine della lettura dei dati), consentendo alla CPU di riutilizzare o eliminare definitivamente le risorse.

In Direct3D 11 il flag [**sul ID3D11DeviceContext:: Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map) d3d11 \_ mapping \_ Write \_ Ignora essenzialmente ogni risorsa come una quantità infinita di memoria in cui l'app può scrivere (un processo noto come "ridenominazione"). In Direct3D 12 di nuovo il processo è esplicito: è necessario allocare memoria aggiuntiva e usare i limiti per sincronizzare le operazioni. I buffer circolare (costituiti da buffer di grandi dimensioni) potrebbero essere una tecnica efficace, fare riferimento allo scenario di buffer circolare nella [gestione delle risorse basata su recinzioni](fence-based-resource-management.md).

![uso di un buffer circolare](images/ring-buffer-1.png)

## <a name="resource-binding"></a>Associazione di risorse

Le visualizzazioni in Direct3D 11 (viste delle risorse dello shader, visualizzazioni della destinazione di rendering e così via) sono state in gran parte sostituite in Direct3D 12 con il concetto di descrittore. I metodi di creazione sono ancora presenti in Direct3D 12, ad esempio [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview) e [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview), che vengono chiamati dopo la creazione dell'heap del descrittore per la scrittura dei dati nell'heap. Il binding in Direct3D 12 è ora gestito dagli handle di descrittore descritti in una firma radice e inviato usando i metodi [**SetGraphicsRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) o [**SetComputeRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) .

Firme radice Dettagli mapping tra il numero di slot della firma radice e le tabelle descrittore, in cui la tabella descrittore può contenere riferimenti a risorse disponibili per i vertex shader, pixel shader e gli altri shader, ad esempio buffer costanti, visualizzazioni di risorse shader e Samplers. Questa flessibilità disconnette lo spazio del registro HLSL dallo spazio di associazione API in Direct3D 12, a differenza di Direct3D 11 in cui è presente un mapping uno-a-uno tra questi.

Una delle implicazioni di questo sistema è che l'app è responsabile della ridenominazione delle tabelle dei descrittori, che consente agli sviluppatori di comprendere il costo delle prestazioni della modifica anche di un singolo descrittore per ogni chiamata di progetto.

Una nuova funzionalità di Direct3D 12 è che un'app può controllare quali descrittori sono condivisi tra le fasi dello shader. Nelle risorse Direct3D 11, ad esempio UAV, vengono condivise tra tutte le fasi dello shader. Consentendo la disabilitazione dei descrittori per determinate fasi dello shader, i registri utilizzati dai descrittori che sono stati disabilitati sono disponibili per essere utilizzati dai descrittori che sono abilitati per una fase particolare dello shader.

Nella tabella seguente viene illustrata una firma radice di esempio.



| Slot parametri radice | Voce della tabella descrittore         |
|---------------------|--------------------------------|
| 0                   | Intervallo descrittore VS B0-B13     |
| 1                   | Intervallo descrittore VS T0-T127    |
| 2                   | Intervallo descrittore VS S0-S16     |
| 3                   | Intervallo descrittore PS B0-B13     |
| ...                 |                                |
| 14                  | Intervallo descrittori DS S0-16      |
| 15                  | Intervallo descrittore condiviso U0-U63 |



 

## <a name="resource-state"></a>Stato della risorsa

Lo stato della risorsa Direct3D 11 non viene gestito dall'app, ma dal driver.

In Direct3D 12 la manutenzione dello stato delle risorse diventa la responsabilità dell'app, per abilitare il parallelismo completo nella registrazione degli elenchi di comandi: l'app deve gestire le sequenze temporali di registrazione per gli elenchi di comandi (che possono essere eseguiti in parallelo) e le sequenze temporali di esecuzione che devono essere sequenziali.

Una transizione di stato della risorsa viene gestita dal metodo [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) . Principalmente l'app deve informare il driver quando l'utilizzo delle risorse è in corso di modifica. Se, ad esempio, una risorsa viene usata come destinazione di rendering e quindi deve essere usata come input per un vertex shader alla successiva chiamata di disegnare, potrebbe essere necessario un breve blocco nell'operazione GPU per completare l'operazione di rendering della destinazione prima di gestire il vertex shader.

Questo sistema consente la sincronizzazione con granularità fine (stalli GPU) della pipeline grafica, nonché gli scaricamenti della cache e possibilmente alcune modifiche al layout della memoria, ad esempio la visualizzazione della destinazione di rendering per depth stencil la decompressione della visualizzazione.

Questa operazione è nota come barriera di transizione. In Direct3D 11 sono disponibili altri tipi di barriere [**: ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) ha abilitato la stessa memoria fisica per l'uso da parte di due risorse affiancate diverse. In Direct3D 12 questa operazione viene definita "barriera di aliasing". È possibile usare le barriere alias per le risorse affiancate e posizionate in Direct3D 12. Inoltre, è presente la barriera UAV. In Direct3D 11 tutte le operazioni di invio e di richiamo di UAV devono essere serializzate, anche se è possibile eseguire la pipeline o lavorare in parallelo. Per Direct3D 12 questa restrizione viene rimossa dall'aggiunta di una barriera UAV. Una barriera UAV garantisce che le operazioni UAV siano sequenziali, quindi, se una seconda operazione richiede che il primo completamento, il secondo verrà forzato ad attendere l'aggiunta della barriera. L'operazione predefinita per UAV è semplicemente che le operazioni procedono il più rapidamente possibile.

Se un carico di lavoro può essere parallelo, è evidente un miglioramento delle prestazioni.

## <a name="swapchains"></a>Le catene

La catena di scambio DXGI è la base per le catene di scambio in Direct3D 11 e 12. Vi sono alcune piccole differenze, in Direct3D 11 i tre tipi di catena di scambio sono SEQUENZIAli, SCARTAti e FLIP \_ sequenziali. Per Direct3D 12 sono disponibili solo due tipi: CAPOVOLGi \_ sequenziali e Capovolgi \_ Ignora. Come indicato in precedenza, è necessario creare in modo esplicito il presentazione catena tramite **IDXGIFactory4** o versione successiva e usando la stessa interfaccia per qualsiasi enumerazione di adapter.

In Direct3D 11 è presente la rotazione automatica del buffer: è necessaria una sola visualizzazione della destinazione di rendering per il buffer nascosto 0. In Direct3D 12 la rotazione del buffer è esplicita, deve essere presente una visualizzazione della destinazione di rendering per ogni buffer nascosto. Usare il metodo [**IDXGISwapChain3:: GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) per selezionare quello in cui eseguire il rendering. Questa ulteriore flessibilità consente inoltre una maggiore parallelizzazione.

> [!NOTE]
> Sebbene esistano molti modi per configurare l'applicazione, in genere le applicazioni hanno un **ID3D12CommandAllocator** per ogni buffer a catena di scambio. Ciò consente all'applicazione di procedere alla creazione di un set di comandi per il frame successivo mentre la GPU esegue il rendering dell'oggetto precedente.

## <a name="fixed-function-rendering"></a>Correzione del rendering della funzione

In Direct3D 11 sono disponibili alcuni metodi che semplificano varie operazioni di livello superiore, ad esempio [**GenerateMips**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips) (creazione di catene MIP complete) e [**DrawAuto**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto) (usando l'output del flusso come input dello shader senza ulteriore input dall'app). Questi metodi non sono disponibili in Direct3D 12, l'app deve gestire queste operazioni creando shader per eseguirle.

## <a name="odds-and-ends"></a>Probabilità e fine

La tabella seguente illustra una serie di funzionalità simili tra Direct3D 11 e 12, ma non sono identiche.



| Direct3D 11                                                                            | Direct3D 12                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Query**](/windows/win32/api/d3d11/nn-d3d11-id3d11query)                                              | [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) consente di raggruppare le query, riducendo i costi.                                                                                                                                                                                                                                                                                                                                     |
| [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate)                                      | Predicazione è ora abilitato con dati in un buffer completamente trasparente. L'oggetto [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate) Direct3D 11 viene sostituito da [**ID3D12Resource:: Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map), che deve seguire una chiamata a [**ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) e un'operazione di sincronizzazione GPU usando un limite per attendere che i dati siano pronti. Vedere [predicazione](predication.md). |
| Contatore UAV/così nascosto                                                                  | L'app è responsabile dell'allocazione e della gestione dei contatori di così/UAV. Vedere [contatori di output di flusso](stream-output-counters.md) e [contatori UAV](uav-counters.md).                                                                                                                                                                                                                                                             |
| MinLOD dinamico risorse (livello minimo di dettaglio)                                       | Questa operazione è stata spostata nel MinLOD statico del descrittore SRV.                                                                                                                                                                                                                                                                                                                                                                                 |
| Disegnato \* indirect/[**DispatchIndirect**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-dispatchindirect) | Il disegno di metodi indiretti viene unito in un unico metodo [**ExecuteIndirect**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) .                                                                                                                                                                                                                                                                                                        |
| I formati DepthStencil sono con interfoliazione                                                   | I formati DepthStencil sono planari. Ad esempio, un formato di 24 bit di profondità, 8 bit di stencil verranno archiviati nel formato 24/8/24/8... e così via in Direct3D 11, ma come 24/24/24... seguito da 8/8/8... in Direct3D 12. Si noti che ogni piano è la propria sottorisorsa in D3D12 (vedere [le sottorisorse](subresources.md)).                                                                                                                    |
| [**ResizeTilePool**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)                   | È possibile eseguire il mapping delle risorse riservate a più heap. Quando un pool di sezioni è stato ampliato in D3D11, è possibile allocare un heap aggiuntivo in D3D12.                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esercitazioni video su DirectX Advanced Learning: Guida al porting di DirectX 11 a DirectX 12](https://www.youtube.com/watch?v=BV64mdOCgZo)
</dt> <dt>

[Informazioni su Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Uso di Direct3D 11, Direct3D 10 e Direct2D](direct3d-12-interop.md)
</dt> </dl>