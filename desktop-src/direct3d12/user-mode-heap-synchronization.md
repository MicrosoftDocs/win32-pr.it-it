---
title: Sincronizzazione di più motori
description: In questo argomento viene illustrata la sincronizzazione dell'accesso ai più motori indipendenti disponibili nelle GPU più moderne.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: 2d250133d8cacb26d933d3774f397de4c949c72b7b58114759791c103d374c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987553"
---
# <a name="multi-engine-synchronization"></a>Sincronizzazione di più motori

La maggior parte delle GPU moderne contiene più motori indipendenti che forniscono funzionalità specializzate. Molti hanno uno o più motori di copia dedicati e un motore di calcolo, in genere diverso dal motore 3D. Ognuno di questi motori può eseguire comandi in parallelo tra loro. Direct3D 12 offre accesso con granularità fine ai motori 3D, di calcolo e di copia, usando code ed elenchi di comandi.

## <a name="gpu-engines"></a>Motori GPU

Il diagramma seguente mostra i thread della CPU di un titolo, ognuno dei quali popola una o più code di copia, calcolo e 3D. La coda 3D può guidare tutti e tre i motori GPU; la coda di calcolo può guidare i motori di calcolo e copia; e la coda di copia sono semplicemente il motore di copia.

Poiché i diversi thread popolano le code, non vi può essere alcuna garanzia semplice dell'ordine di esecuzione, quindi la necessità di meccanismi di sincronizzazione quando il titolo &mdash; li richiede.

![quattro thread che inviano comandi a tre code](images/gpu-engines.png)

L'immagine seguente illustra come un titolo potrebbe pianificare il lavoro tra più motori GPU, inclusa la sincronizzazione tra motori, dove necessario: mostra i carichi di lavoro per motore con dipendenze tra motori. In questo esempio, il motore di copia copia prima di tutto la geometria necessaria per il rendering. Il motore 3D attende il completamento di queste copie ed esegue il rendering di un pre-passaggio sulla geometria. Viene quindi utilizzato dal motore di calcolo. I risultati di [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)del motore di calcolo, insieme a diverse operazioni di copia della trama nel motore di copia, vengono utilizzati dal motore 3D per la chiamata [**di disegno**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) finale.

![comunicazione tra i motori di copia, grafica e calcolo](images/gpu-sync.png)

Lo pseudocodice seguente illustra come un titolo potrebbe inviare un carico di lavoro di questo tipo.

``` syntax
// Get per-engine contexts. Note that multiple queues may be exposed
// per engine, however that design is not reflected here.
copyEngine = device->GetCopyEngineContext();
renderEngine = device->GetRenderEngineContext();
computeEngine = device->GetComputeEngineContext();
copyEngine->CopyResource(geometry, ...); // copy geometry
copyEngine->Signal(copyFence, 101);
copyEngine->CopyResource(tex1, ...); // copy textures
copyEngine->CopyResource(tex2, ...); // copy more textures
copyEngine->CopyResource(tex3, ...); // copy more textures
copyEngine->CopyResource(tex4, ...); // copy more textures
copyEngine->Signal(copyFence, 102);
renderEngine->Wait(copyFence, 101); // geometry copied
renderEngine->Draw(); // pre-pass using geometry only into rt1
renderEngine->Signal(renderFence, 201);
computeEngine->Wait(renderFence, 201); // prepass completed
computeEngine->Dispatch(); // lighting calculations on pre-pass (using rt1 as SRV)
computeEngine->Signal(computeFence, 301);
renderEngine->Wait(computeFence, 301); // lighting calculated into buf1
renderEngine->Wait(copyFence, 102); // textures copied
renderEngine->Draw(); // final render using buf1 as SRV, and tex[1-4] SRVs
```

Lo pseudocodice seguente illustra la sincronizzazione tra i motori di copia e 3D per eseguire l'allocazione di memoria simile all'heap tramite un buffer circolare. I titoli offrono la flessibilità necessaria per scegliere il giusto equilibrio tra l'ottimizzazione del parallelismo (tramite un buffer di grandi dimensioni) e la riduzione del consumo di memoria e della latenza (tramite un buffer di piccole dimensioni).

``` syntax
device->CreateBuffer(&ringCB);
for(int i=1;i++){
  if(i > length) copyEngine->Wait(fence1, i - length);
  copyEngine->Map(ringCB, value%length, WRITE, pData); // copy new data
  copyEngine->Signal(fence2, i);
  renderEngine->Wait(fence2, i);
  renderEngine->Draw(); // draw using copied data
  renderEngine->Signal(fence1, i);
}

// example for length = 3:
// copyEngine->Map();
// copyEngine->Signal(fence2, 1); // fence2 = 1  
// copyEngine->Map();
// copyEngine->Signal(fence2, 2); // fence2 = 2
// copyEngine->Map();
// copyEngine->Signal(fence2, 3); // fence2 = 3
// copy engine has exhausted the ring buffer, so must wait for render to consume it
// copyEngine->Wait(fence1, 1); // fence1 == 0, wait
// renderEngine->Wait(fence2, 1); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 1); // fence1 = 1, copy engine now unblocked
// renderEngine->Wait(fence2, 2); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 2); // fence1 = 2
// renderEngine->Wait(fence2, 3); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 3); // fence1 = 3
// now render engine is starved, and so must wait for the copy engine
// renderEngine->Wait(fence2, 4); // fence2 == 3, wait
```

## <a name="multi-engine-scenarios"></a>Scenari con più motori

Direct3D 12 consente di evitare l'inefficienza accidentale causata da ritardi imprevisti della sincronizzazione. Consente inoltre di introdurre la sincronizzazione a un livello superiore in cui la sincronizzazione richiesta può essere determinata con maggiore certezza. Un secondo problema degli indirizzi multimotore è rendere più esplicite le operazioni dispendiose, incluse le transizioni tra 3D e video tradizionalmente costose a causa della sincronizzazione tra più contesti del kernel.

In particolare, gli scenari seguenti possono essere affrontati con Direct3D 12.

-   Funzionamento asincrono e con priorità bassa della GPU. Ciò consente l'esecuzione simultanea di operazioni atomiche e di lavoro gpu con priorità bassa che consentono a un thread GPU di utilizzare i risultati di un altro thread non sincronizzato senza blocco.
-   Lavoro di calcolo ad alta priorità. Con il calcolo in background è possibile interrompere il rendering 3D per eseguire una piccola quantità di lavoro di calcolo ad alta priorità. I risultati di questo lavoro possono essere ottenuti in anticipo per un'ulteriore elaborazione della CPU.
-   Lavoro di calcolo in background. Una coda separata con priorità bassa per i carichi di lavoro di calcolo consente a un'applicazione di usare cicli GPU di riserva per eseguire il calcolo in background senza alcun impatto negativo sulle attività di rendering primarie (o di altro tipo). Le attività in background possono includere la decompressione delle risorse o l'aggiornamento di simulazioni o strutture di accelerazione. Le attività in background devono essere sincronizzate raramente nella CPU (circa una volta per fotogramma) per evitare di bloccare o rallentare il lavoro in primo piano.
-   Streaming e caricamento dei dati. Una coda di copia separata sostituisce i concetti D3D11 relativi ai dati iniziali e all'aggiornamento delle risorse. Anche se l'applicazione è responsabile di altri dettagli nel modello Direct3D 12, questa responsabilità è data dalla potenza. L'applicazione può controllare la quantità di memoria di sistema dedicata al buffering dei dati di caricamento. L'app può scegliere quando e come (CPU e GPU, blocco o non blocco) per la sincronizzazione e può tenere traccia dello stato di avanzamento e controllare la quantità di lavoro in coda.
-   Maggiore parallelismo. Le applicazioni possono usare code più approfondite per i carichi di lavoro in background ,ad esempio la decodifica video, quando hanno code separate per il lavoro in primo piano.

In Direct3D 12 il concetto di coda di comandi è la rappresentazione API di una sequenza di lavoro approssimativamente seriale inviata dall'applicazione. Le barriere e altre tecniche consentono l'esecuzione di questo lavoro in una pipeline o non in ordine, ma l'applicazione vede solo una singola sequenza temporale di completamento. Corrisponde al contesto immediato in D3D11.

## <a name="synchronization-apis"></a>API di sincronizzazione

### <a name="devices-and-queues"></a>Dispositivi e code

Il dispositivo Direct3D 12 include metodi per creare e recuperare code di comandi di tipi e priorità diversi. La maggior parte delle applicazioni deve usare le code di comandi predefinite perché consentono l'utilizzo condiviso da parte di altri componenti. Le applicazioni con requisiti di concorrenza aggiuntivi possono creare code aggiuntive. Le code vengono specificate dal tipo di elenco dei comandi che utilizzano.

Vedere i metodi di creazione seguenti di [**ID3D12Device.**](/windows/win32/api/d3d12/nn-d3d12-id3d12device)

-   [**CreateCommandQueue:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) crea una coda di comandi in base alle informazioni in una [**struttura DIRECT3D 12 \_ COMMAND QUEUE \_ \_ DESC.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)
-   [**CreateCommandList:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) crea un elenco di comandi di tipo [**Direct3D 12 \_ COMMAND LIST \_ \_ TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).
-   [**CreateFence:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) crea un limite, annotando i flag in [**Direct3D 12 \_ FENCE \_ FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). I recinti vengono usati per sincronizzare le code.

Le code di tutti i tipi (3D, calcolo e copia) condividono la stessa interfaccia e sono tutte basate sull'elenco dei comandi.

Fare riferimento ai metodi seguenti di [**ID3D12CommandQueue.**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)

-   [**ExecuteCommandLists:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) invia una matrice di elenchi di comandi per l'esecuzione. Ogni elenco di comandi definito da [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).
-   [**Segnale:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) imposta un valore di limite quando la coda (in esecuzione sulla GPU) raggiunge un determinato punto.
-   [**Wait:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) la coda attende fino a quando il limite specificato non raggiunge il valore specificato.

Si noti che le aggregazioni non vengono utilizzate da alcuna coda e pertanto questo tipo non può essere usato per creare una coda.

### <a name="fences"></a>Barriere

L'API multimotore fornisce API esplicite per la creazione e la sincronizzazione tramite i recinti. Un limite è un costrutto di sincronizzazione controllato da un valore UINT64. I valori limite vengono impostati dall'applicazione. Un'operazione di segnalazione modifica il valore di limite e un'operazione di attesa si blocca fino a quando il limite non raggiunge il valore richiesto o superiore. Un evento può essere generato quando un limite raggiunge un determinato valore.

Fare riferimento ai metodi [**dell'interfaccia ID3D12Fence.**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)

-   [**GetCompletedValue:**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) restituisce il valore corrente del limite.
-   [**SetEventOnCompletion:**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) genera un evento quando il limite raggiunge un valore specificato.
-   [**Signal:**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) imposta il limite sul valore specificato.

I limiti consentono l'accesso della CPU al valore di limite corrente e le attese e i segnali della CPU.

Il [**metodo Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) nell'interfaccia [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) aggiorna un limite dal lato CPU. Questo aggiornamento viene eseguito immediatamente. Il [**metodo Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) su [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) aggiorna un limite dal lato GPU. Questo aggiornamento si verifica dopo il completamento di tutte le altre operazioni nella coda dei comandi.

Tutti i nodi in una configurazione a più motori possono leggere e reagire a qualsiasi limite che raggiunge il valore giusto.

Le applicazioni impostano i propri valori di limite. Un buon punto di partenza potrebbe essere l'aumento di un limite una volta per fotogramma.

È possibile *che venga* *riassato un limite*. Ciò significa che il valore limite non deve essere incrementato esclusivamente. Se un'operazione **Signal** viene accodata in due code di comandi diverse o se due thread della CPU chiamano **entrambi Signal** su un limite, potrebbe esserci una corsa per determinare quale **segnale** viene completato per ultimo e quindi quale valore limite rimarrà. Se viene riassato un limite, tutte le nuove attese (incluse le richieste **SetEventOnCompletion)** verranno confrontate con il nuovo valore di limite inferiore e pertanto potrebbero non essere soddisfatte, anche se il valore di limite era in precedenza sufficientemente elevato da soddisfarle. Se si verifica una race, tra un valore che soddisferà un'attesa in attesa e un valore inferiore che non lo sarà, l'attesa verrà soddisfatta indipendentemente dal valore che rimane in seguito. 

Le API di recinto forniscono potenti funzionalità di sincronizzazione, ma possono creare problemi potenzialmente difficili da eseguire il debug. È consigliabile usare ogni limite solo per indicare lo stato di avanzamento in una sequenza temporale per impedire le races tra i segnalatori.

### <a name="copy-and-compute-command-lists"></a>Copiare e calcolare elenchi di comandi

Tutti e tre i tipi di elenco dei comandi usano l'interfaccia [**ID3D12GraphicsCommandList,**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ma solo un subset dei metodi è supportato per la copia e il calcolo.

Gli elenchi di comandi di copia e calcolo possono usare i metodi seguenti.

-   [**Chiudi**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**CopyResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**CopyTiles**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

Gli elenchi di comandi di calcolo possono anche usare i metodi seguenti.

-   [**ClearState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [**ClearUnorderedAccessViewFloat**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**ClearUnorderedAccessViewUint**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**ExecuteIndirect**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [**SetComputeRoot32BitConstant**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetComputeRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetComputeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [**Impostazione della predicazione**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

Gli elenchi di comandi di calcolo devono impostare un pso di calcolo quando si [**chiama SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

I bundle non possono essere usati con gli elenchi di comandi di calcolo o copia o le code.

## <a name="pipelined-compute-and-graphics-example"></a>Esempio di calcolo e grafica in pipeline

Questo esempio illustra come usare la sincronizzazione dei recinti per creare una pipeline di lavoro di calcolo in una coda (a cui fa riferimento ) utilizzata dal lavoro grafico `pComputeQueue` sulla coda `pGraphicsQueue` . Il lavoro di calcolo e grafica viene pipelinedato con la coda grafica che utilizza il risultato del lavoro di calcolo da diversi fotogrammi indietro e viene usato un evento CPU per la limitazione del totale del lavoro in coda nel suo complesso.

```cpp
void PipelinedComputeGraphics()
{
    const UINT CpuLatency = 3;
    const UINT ComputeGraphicsLatency = 2;

    HANDLE handle = CreateEvent(nullptr, FALSE, FALSE, nullptr);

    UINT64 FrameNumber = 0;

    while (1)
    {
        if (FrameNumber > ComputeGraphicsLatency)
        {
            pComputeQueue->Wait(pGraphicsFence,
                FrameNumber - ComputeGraphicsLatency);
        }

        if (FrameNumber > CpuLatency)
        {
            pComputeFence->SetEventOnFenceCompletion(
                FrameNumber - CpuLatency,
                handle);
            WaitForSingleObject(handle, INFINITE);
        }

        ++FrameNumber;

        pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
        pComputeQueue->Signal(pComputeFence, FrameNumber);
        if (FrameNumber > ComputeGraphicsLatency)
        {
            UINT GraphicsFrameNumber = FrameNumber - ComputeGraphicsLatency;
            pGraphicsQueue->Wait(pComputeFence, GraphicsFrameNumber);
            pGraphicsQueue->ExecuteCommandLists(1, &pGraphicsCommandList);
            pGraphicsQueue->Signal(pGraphicsFence, GraphicsFrameNumber);
        }
    }
}
```

Per supportare questo pipelining, deve essere presente un buffer di copie diverse dei dati che passano dalla coda di calcolo `ComputeGraphicsLatency+1` alla coda grafica. Gli elenchi di comandi devono usare UAV e il riferimento indiretto per leggere e scrivere dalla "versione" appropriata dei dati nel buffer. La coda di calcolo deve attendere che la coda grafica abbia terminato la lettura dai dati per il frame N prima di poter scrivere il frame `N+ComputeGraphicsLatency` .

Si noti che la quantità di coda di calcolo utilizzata rispetto alla CPU non dipende direttamente dalla quantità di buffering necessaria, tuttavia l'accodamento del lavoro della GPU oltre la quantità di spazio disponibile nel buffer è meno utile.

Un meccanismo alternativo per evitare il riferimento indiretto consiste nel creare più elenchi di comandi corrispondenti a ognuna delle versioni "rinominate" dei dati. L'esempio successivo usa questa tecnica durante l'estensione dell'esempio precedente per consentire l'esecuzione asincrona delle code di calcolo e grafica.

## <a name="asynchronous-compute-and-graphics-example"></a>Esempio di calcolo asincrono e grafica

L'esempio seguente consente il rendering asincrono della grafica dalla coda di calcolo. Tra le due fasi è ancora presente una quantità fissa di dati memorizzati nel buffer, ma ora il lavoro grafico procede in modo indipendente e usa il risultato più aggiornato della fase di calcolo, come noto nella CPU quando il lavoro grafico viene accodato. Ciò sarebbe utile se il lavoro grafico fosse stato aggiornato da un'altra origine, ad esempio l'input dell'utente. Devono essere presenti più elenchi di comandi per consentire ai frame di grafica di essere in esecuzione contemporaneamente e la funzione rappresenta l'aggiornamento dell'elenco dei comandi per includere i dati di input più recenti e leggere i dati di calcolo dal `ComputeGraphicsLatency` `UpdateGraphicsCommandList` buffer appropriato.

La coda di calcolo deve comunque attendere il completamento della coda grafica con i buffer della pipe, ma è stato introdotto un terzo limite ( ) in modo che sia possibile tenere traccia dello stato di avanzamento del lavoro di calcolo della lettura della grafica rispetto allo stato di avanzamento della grafica `pGraphicsComputeFence` in generale. Ciò riflette il fatto che i fotogrammi grafici consecutivi possono ora leggere dallo stesso risultato di calcolo o ignorare un risultato di calcolo. Una progettazione più efficiente ma leggermente più complessa userebbe solo il singolo recinto grafico e archivierebbe un mapping ai frame di calcolo usati da ogni frame grafico.

```cpp
void AsyncPipelinedComputeGraphics()
{
    const UINT CpuLatency{ 3 };
    const UINT ComputeGraphicsLatency{ 2 };

    // The compute fence is at index 0; the graphics fence is at index 1.
    ID3D12Fence* rgpFences[]{ pComputeFence, pGraphicsFence };
    HANDLE handles[2];
    handles[0] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    handles[1] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    UINT FrameNumbers[]{ 0, 0 };

    ID3D12GraphicsCommandList* rgpGraphicsCommandLists[CpuLatency];
    CreateGraphicsCommandLists(ARRAYSIZE(rgpGraphicsCommandLists),
        rgpGraphicsCommandLists);

    // Graphics needs to wait for the first compute frame to complete; this is the
    // only wait that the graphics queue will perform.
    pGraphicsQueue->Wait(pComputeFence, 1);

    while (true)
    {
        for (auto i = 0; i < 2; ++i)
        {
            if (FrameNumbers[i] > CpuLatency)
            {
                rgpFences[i]->SetEventOnCompletion(
                    FrameNumbers[i] - CpuLatency,
                    handles[i]);
            }
            else
            {
                ::SetEvent(handles[i]);
            }
        }


        auto WaitResult = ::WaitForMultipleObjects(2, handles, FALSE, INFINITE);
        if (WaitResult > WAIT_OBJECT_0 + 1) continue;
        auto Stage = WaitResult - WAIT_OBJECT_0;
        ++FrameNumbers[Stage];

        switch (Stage)
        {
        case 0:
        {
            if (FrameNumbers[Stage] > ComputeGraphicsLatency)
            {
                pComputeQueue->Wait(pGraphicsComputeFence,
                    FrameNumbers[Stage] - ComputeGraphicsLatency);
            }
            pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
            pComputeQueue->Signal(pComputeFence, FrameNumbers[Stage]);
            break;
        }
        case 1:
        {
            // Recall that the GPU queue started with a wait for pComputeFence, 1
            UINT64 CompletedComputeFrames = min(1,
                pComputeFence->GetCompletedValue());
            UINT64 PipeBufferIndex =
                (CompletedComputeFrames - 1) % ComputeGraphicsLatency;
            UINT64 CommandListIndex = (FrameNumbers[Stage] - 1) % CpuLatency;
            // Update graphics command list based on CPU input and using the appropriate
            // buffer index for data produced by compute.
            UpdateGraphicsCommandList(PipeBufferIndex,
                rgpGraphicsCommandLists[CommandListIndex]);

            // Signal *before* new rendering to indicate what compute work
            // the graphics queue is DONE with
            pGraphicsQueue->Signal(pGraphicsComputeFence, CompletedComputeFrames - 1);
            pGraphicsQueue->ExecuteCommandLists(1,
                rgpGraphicsCommandLists + PipeBufferIndex);
            pGraphicsQueue->Signal(pGraphicsFence, FrameNumbers[Stage]);
            break;
        }
        }
    }
}
```

## <a name="multi-queue-resource-access"></a>Accesso alle risorse multi-coda

Per accedere a una risorsa in più code, un'applicazione deve rispettare le regole seguenti.

-   L'accesso alle risorse [**(vedere Direct3D 12 \_ RESOURCE \_ STATES)**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)è determinato dalla classe del tipo di coda non dall'oggetto coda. Esistono due classi di tipo di coda: compute/3D queue è una classe di tipo, Copy è una seconda classe di tipo. Pertanto, una risorsa con una barriera allo stato DELLA RISORSA NON PIXEL SHADER in una coda 3D può essere usata in tale stato in qualsiasi coda 3D o di calcolo, in base ai requisiti di sincronizzazione che richiedono la serializzazione della maggior parte delle \_ \_ \_ scritture. Gli stati delle risorse condivisi tra le due classi di tipi (COPY SOURCE e COPY DEST) sono considerati stati \_ diversi per ogni classe di \_ tipo. In questo modo, se una risorsa passa a COPY DEST in una coda di copia, non è accessibile come destinazione di copia da code 3D o di calcolo \_ e viceversa.

    Per riepilogare.

    -   Un "oggetto" della coda è una singola coda.
    -   Un "tipo" della coda è uno di questi tre: Calcolo, 3D e Copia.
    -   Una "classe di tipo" della coda è una delle due seguenti: Calcolo/3D e Copia.

-   I flag COPY (COPY DEST e COPY SOURCE) usati come stati iniziali rappresentano gli stati \_ nella classe di tipo \_ 3D/Compute. Per usare inizialmente una risorsa in una coda di copia, è necessario che inizi nello stato COMMON. Lo stato COMMON può essere usato per tutti gli utilizzi in una coda di copia usando le transizioni di stato implicite. 
-   Anche se lo stato della risorsa è condiviso tra tutte le code di calcolo e 3D, non è consentito scrivere contemporaneamente nella risorsa in code diverse. "Simultaneamente" in questo caso significa non sincronizzato, notando che l'esecuzione non sincronizzata non è possibile su alcuni componenti hardware. Si applicano le regole seguenti.

    -   Solo una coda può scrivere in una risorsa alla volta.
    -   Più code possono leggere dalla risorsa purché non leggono i byte modificati dal writer (la lettura dei byte scritti simultaneamente produce risultati non definiti).
    -   È necessario utilizzare un limite per la sincronizzazione dopo la scrittura prima che un'altra coda possa leggere i byte scritti o effettuare qualsiasi accesso in scrittura.

-   I buffer back presentati devono essere nello stato COMUNE STATO RISORSA Direct3D \_ \_ 12. \_ 

## <a name="related-topics"></a>Argomenti correlati

[Guida alla programmazione di Direct3D 12](directx-12-programming-guide.md)

[Uso delle barriere delle risorse per sincronizzare gli stati delle risorse in Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[Gestione della memoria in Direct3D 12](memory-management.md)
