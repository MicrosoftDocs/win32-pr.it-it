---
title: Sincronizzazione multimotore
description: Questo argomento illustra la sincronizzazione dell'accesso a più motori indipendenti disponibili nella maggior parte delle GPU moderne.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d60704e411a1ba45dd4902ad9101a416391743dd
ms.sourcegitcommit: 622d149edf775af5a9633c2d12ccfddf7000b8fd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2020
ms.locfileid: "104548777"
---
# <a name="multi-engine-synchronization"></a>Sincronizzazione multimotore

La maggior parte delle GPU moderne contiene più motori indipendenti che offrono funzionalità specializzate. Molti hanno uno o più motori di copia dedicati e un motore di calcolo, in genere distinti dal motore 3D. Ognuno di questi motori può eseguire comandi in parallelo tra loro. Direct3D 12 offre un accesso con granularità fine ai motori 3D, di calcolo e di copia, usando code ed elenchi di comandi.

## <a name="gpu-engines"></a>Motori GPU

Il diagramma seguente mostra i thread della CPU del titolo, ciascuno dei quali popola una o più code di copia, calcolo e 3D. La coda 3D può gestire tutti e tre i motori GPU; la coda di calcolo può guidare i motori di calcolo e di copia; e la coda di copia semplicemente il motore di copia.

Poiché i diversi thread popolano le code, non è possibile fornire una semplice garanzia dell'ordine di esecuzione, quindi la necessità di meccanismi di sincronizzazione &mdash; quando il titolo li richiede.

![quattro thread che inviano comandi a tre code](images/gpu-engines.png)

Nell'immagine seguente viene illustrato il modo in cui un titolo può pianificare il lavoro tra più motori GPU, inclusa la sincronizzazione tra i motori quando necessario: Mostra i carichi di lavoro per motore con dipendenze tra i motori. In questo esempio il motore di copia copia prima di tutto la geometria necessaria per il rendering. Il motore 3D attende il completamento di queste copie ed esegue il rendering di un pre-pass sulla geometria. Questa operazione viene quindi utilizzata dal motore di calcolo. I risultati dell' [**invio**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)del motore di calcolo, insieme a diverse operazioni di copia di trama nel motore di copia, vengono usati dal motore 3D per la chiamata di [**progetto**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) finale.

![copia, grafica e motori di calcolo che comunicano](images/gpu-sync.png)

Lo pseudo-codice seguente illustra come un titolo può inviare un carico di lavoro di questo tipo.

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

Lo pseudo-codice seguente illustra la sincronizzazione tra i motori di copia e 3D per ottenere l'allocazione di memoria simile a heap tramite un buffer circolare. I titoli hanno la flessibilità di scegliere il giusto equilibrio tra l'ottimizzazione del parallelismo (tramite un buffer di grandi dimensioni) e la riduzione dell'utilizzo della memoria e della latenza (tramite un buffer di piccole dimensioni).

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

## <a name="multi-engine-scenarios"></a>Scenari multimotore

Direct3D 12 consente di evitare l'esecuzione accidentale di inefficienze dovute a ritardi di sincronizzazione imprevisti. Consente inoltre di introdurre la sincronizzazione a un livello superiore in cui è possibile determinare la sincronizzazione necessaria con maggiore precisione. Un secondo problema per cui gli indirizzi multimotore è quello di rendere più complesse le operazioni più complesse, incluse le transizioni tra 3D e video che erano tradizionalmente costose a causa della sincronizzazione tra più contesti kernel.

In particolare, è possibile risolvere gli scenari seguenti con Direct3D 12.

-   Lavoro GPU asincrono e con priorità bassa. Ciò consente l'esecuzione simultanea di operazioni di GPU a priorità bassa e operazioni atomiche che consentono a un thread GPU di utilizzare i risultati di un altro thread non sincronizzato senza bloccarsi.
-   Lavoro di calcolo con priorità alta. Con il calcolo in background è possibile interrompere il rendering 3D per eseguire una piccola quantità di lavoro di calcolo con priorità alta. I risultati di questo lavoro possono essere ottenuti in anticipo per un'ulteriore elaborazione sulla CPU.
-   Lavoro di calcolo in background. Una coda separata con priorità bassa per i carichi di lavoro di calcolo consente a un'applicazione di usare cicli GPU di riserva per eseguire calcoli in background senza impatto negativo sulle attività di rendering (o altre) primarie. Le attività in background possono includere la decompressione di risorse o l'aggiornamento di simulazioni o strutture di accelerazione. Le attività in background devono essere sincronizzate raramente sulla CPU (approssimativamente una volta per fotogramma) per evitare blocchi o rallentare il lavoro in primo piano.
-   Streaming e caricamento dei dati. Una coda di copia separata sostituisce i concetti D3D11 dei dati iniziali e l'aggiornamento delle risorse. Sebbene l'applicazione sia responsabile di ulteriori dettagli nel modello Direct3D 12, questa responsabilità viene fornita con energia. L'applicazione può controllare la quantità di memoria di sistema dedicata al buffering dei dati di caricamento. L'app può scegliere quando e in che modo eseguire la sincronizzazione (CPU e GPU, bloccando e non bloccando) ed è possibile tenere traccia dello stato di avanzamento e controllare la quantità di lavoro in coda.
-   Maggiore parallelismo. Le applicazioni possono usare code più profonde per i carichi di lavoro in background (ad esempio, decodifica video) quando hanno code separate per il lavoro in primo piano.

In Direct3D 12 il concetto di coda dei comandi è la rappresentazione API di una sequenza di lavoro approssimativamente seriale inviata dall'applicazione. Le barriere e altre tecniche consentono l'esecuzione di questo lavoro in una pipeline o non in ordine, ma l'applicazione Visualizza solo una sequenza temporale di completamento singola. Corrisponde al contesto immediato in D3D11.

## <a name="synchronization-apis"></a>API di sincronizzazione

### <a name="devices-and-queues"></a>Dispositivi e code

Il dispositivo Direct3D 12 dispone di metodi per creare e recuperare le code dei comandi di tipi e priorità diversi. La maggior parte delle applicazioni deve usare le code di comando predefinite perché consentono l'uso condiviso da parte di altri componenti. Le applicazioni con requisiti di concorrenza aggiuntivi possono creare code aggiuntive. Le code vengono specificate dal tipo di elenco dei comandi utilizzato.

Vedere i seguenti metodi di creazione di [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).

-   [**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : crea una coda di comandi basata su informazioni in una struttura di [**\_ Descrizione della \_ coda \_ di comandi Direct3D 12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .
-   [**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : crea un elenco di comandi di tipo tipo [**\_ \_ elenco di \_ comandi Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).
-   [**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : crea una recinzione, notando i flag nei [**\_ \_ flag di recinzione Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Le barriere vengono utilizzate per sincronizzare le code.

Le code di tutti i tipi (3D, COMPUTE e Copy) condividono la stessa interfaccia e sono basate su tutti gli elenchi di comandi.

Vedere i metodi seguenti per [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).

-   [**Oggetti executecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : Invia una matrice di elenchi di comandi per l'esecuzione. Ogni elenco di comandi definito da [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).
-   [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : imposta un valore di recinzione quando la coda (in esecuzione sulla GPU) raggiunge un determinato punto.
-   [**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : la coda attende fino a quando il limite specificato non raggiunge il valore specificato.

Si noti che i bundle non vengono utilizzati da alcuna coda e pertanto questo tipo non può essere utilizzato per creare una coda.

### <a name="fences"></a>Barriere

L'API multimotore fornisce API esplicite per creare e sincronizzare usando le schermate. Una recinzione è un costrutto di sincronizzazione controllato da un valore UINT64. I valori di recinzione vengono impostati dall'applicazione. Un'operazione di segnalazione modifica il valore della recinzione e un blocco dell'operazione di attesa fino a quando il limite non raggiunge il valore richiesto o un valore superiore. Un evento può essere generato quando una recinzione raggiunge un determinato valore.

Vedere i metodi dell'interfaccia [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) .

-   [**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : restituisce il valore corrente della recinzione.
-   [**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : determina l'attivazione di un evento quando la barriera raggiunge un valore specificato.
-   [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : imposta la barriera sul valore specificato.

Le recinzioni consentono l'accesso alla CPU al valore di limite corrente e le attese e i segnali della CPU.

Il metodo [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) sull'interfaccia [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) aggiorna una recinzione dal lato CPU. Questo aggiornamento viene eseguito immediatamente. Il metodo [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) su [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) aggiorna una recinzione dal lato GPU. Questo aggiornamento si verifica dopo il completamento di tutte le altre operazioni nella coda dei comandi.

Tutti i nodi in una configurazione a più motori possono leggere e reagire a qualsiasi limite che raggiunga il valore corretto.

Le applicazioni impostano i propri valori di recinzione, un punto di partenza valido potrebbe aumentare una barriera una volta per ogni fotogramma.

Una recinzione *può* essere *riavvolta*. Ciò significa che non è necessario incrementare solo il valore del limite. Se un'operazione di **segnalazione** viene accodata in due code di comando diverse o se due thread della CPU chiamano il **segnale** su un limite, è possibile che si verifichi una gara per determinare quale **segnale** viene completato per ultimo e quindi quale valore di limite è quello che resterà. Se una recinzione viene riavvolta, eventuali nuove attese (incluse le richieste **SetEventOnCompletion** ) verranno confrontate con il nuovo valore di limite inferiore e pertanto potrebbero non essere soddisfatte, anche se il valore della recinzione era in precedenza sufficientemente elevato da soddisfarle. Se si verifica una corsa, tra un valore che soddisferà un'attesa in attesa e un valore inferiore che non sarà, l'attesa *verrà* soddisfatta indipendentemente dal valore che rimane in seguito.

Le API di recinzione forniscono funzionalità di sincronizzazione potenti, ma possono creare problemi di debug potenzialmente difficili. È consigliabile usare ogni limite solo per indicare lo stato di avanzamento in una sequenza temporale per impedire le gare tra i SignalR.

### <a name="copy-and-compute-command-lists"></a>Elenchi di comandi di copia e calcolo

Tutti e tre i tipi di elenco dei comandi usano l'interfaccia [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) , ma solo un subset dei metodi è supportato per le copie e le risorse di calcolo.

Gli elenchi di comandi di copia e calcolo possono usare i metodi seguenti.

-   [**Chiudi**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**CopyResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**CopyTiles**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

Gli elenchi di comandi Compute possono usare anche i metodi seguenti.

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
-   [**SetPredication**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

Gli elenchi di comandi di calcolo devono impostare un oggetto PSO di calcolo quando si chiama [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

I bundle non possono essere usati con le code o gli elenchi di comandi di calcolo o copia.

## <a name="pipelined-compute-and-graphics-example"></a>Esempio di calcolo e di grafica in pipeline

Questo esempio Mostra come usare la sincronizzazione della recinzione per creare una pipeline di lavoro di calcolo in una coda (a cui fa riferimento `pComputeQueue` ) che viene utilizzata dalla grafica lavorare sulla coda `pGraphicsQueue` . Il lavoro di calcolo e di grafica viene sottoposto a pipeline con la coda grafica che utilizza il risultato del lavoro di calcolo da diversi frame e viene utilizzato un evento CPU per limitare il lavoro totale in coda.

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

Per supportare questo pipelining, deve essere presente un buffer di `ComputeGraphicsLatency+1` copie diverse dei dati che passano dalla coda di calcolo alla coda grafica. Gli elenchi di comandi devono usare UAV e il riferimento indiretto per leggere e scrivere dalla "versione" appropriata dei dati nel buffer. La coda di calcolo deve attendere il completamento della lettura da parte della coda grafica dei dati per il frame N prima di poter scrivere il frame `N+ComputeGraphicsLatency` .

Si noti che la quantità di coda di calcolo elaborata in relazione alla CPU non dipende direttamente dalla quantità di buffering necessaria. Tuttavia, l'accodamento del lavoro della GPU oltre la quantità di spazio disponibile nel buffer è meno importante.

Un meccanismo alternativo per evitare riferimenti indiretti consiste nel creare più elenchi di comandi corrispondenti a ognuna delle versioni "rinominate" dei dati. Nell'esempio seguente viene usata questa tecnica durante l'estensione dell'esempio precedente per consentire l'esecuzione più asincrona delle code di calcolo e di grafica.

## <a name="asynchronous-compute-and-graphics-example"></a>Esempio di calcolo e di grafica asincrono

Questo esempio seguente consente di eseguire il rendering asincrono della grafica dalla coda di calcolo. Tra le due fasi è ancora presente una quantità fissa di dati memorizzati nel buffer, ma ora il lavoro della grafica viene eseguito in modo indipendente e usa i risultati più aggiornati della fase di calcolo, come noto sulla CPU, quando il lavoro della grafica viene accodato. Questa operazione è utile se il lavoro di grafica è stato aggiornato da un'altra origine, ad esempio l'input dell'utente. È necessario che siano presenti più elenchi di comandi per consentire il `ComputeGraphicsLatency` funzionamento dei frame di grafica per volta e che la funzione `UpdateGraphicsCommandList` rappresenti l'aggiornamento dell'elenco dei comandi per includere i dati di input più recenti e la lettura dai dati di calcolo dal buffer appropriato.

La coda di calcolo deve comunque attendere il completamento della coda grafica con i buffer di pipe, ma viene introdotta una terza recinzione ( `pGraphicsComputeFence` ) in modo che lo stato di avanzamento della grafica che legge il lavoro di calcolo e lo stato di avanzamento della grafica in generale possano essere rilevati. Ciò riflette il fatto che ora i fotogrammi grafici consecutivi possono leggere dallo stesso risultato di calcolo o ignorare un risultato di calcolo. Una progettazione più efficiente ma leggermente più complessa usa solo la barriera grafica singola e archivia un mapping ai frame di calcolo usati da ogni frame di grafica.

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

## <a name="multi-queue-resource-access"></a>Accesso alle risorse in più code

Per accedere a una risorsa in più di una coda, un'applicazione deve rispettare le regole seguenti.

-   L'accesso alle risorse (vedere [**\_ \_ gli Stati delle risorse Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) è determinato dall'oggetto Queue della classe del tipo di coda not. Esistono due classi di tipo Queue: COMPUTE/3D Queue è una classe di tipo, Copy è una seconda classe di tipi. Pertanto, una risorsa che presenta una barriera allo \_ stato della risorsa non pixel shader in \_ \_ una coda 3D può essere usata in tale stato in qualsiasi coda 3D o di calcolo, in base ai requisiti di sincronizzazione che richiedono la serializzazione della maggior parte delle Scritture. Gli Stati delle risorse condivisi tra le due classi di tipi (origine di copia \_ e \_ destinazione di copia) sono considerati stati diversi per ogni classe di tipo. In questo modo, se una risorsa esegue una transizione a copia \_ dest in una coda di copia, non è accessibile come destinazione della copia dalle code 3D o di calcolo e viceversa.

    Da riepilogare.

    -   Una coda "oggetto" è un'unica coda.
    -   Una coda "Type" è una delle tre seguenti: COMPUTE, 3D e Copy.
    -   Una coda "Type class" è una delle due seguenti: COMPUTE/3D e Copy.

-   I flag di copia (COPY \_ dest e copy \_ source) usati come stati iniziali rappresentano gli Stati nella classe 3D/Compute Type. Per usare una risorsa inizialmente in una coda di copia, deve iniziare nello stato comune. Lo stato comune può essere usato per tutti gli utilizzi in una coda di copia usando le transizioni di stato implicite. 
-   Anche se lo stato della risorsa è condiviso tra tutte le code di calcolo e 3D, non è consentito scrivere contemporaneamente nella risorsa in code diverse. "Simultaneamente" indica che non è stata eseguita la sincronizzazione. l'esecuzione non sincronizzata non è possibile in alcuni componenti hardware. Si applicano le regole seguenti.

    -   Una sola coda può scrivere in una risorsa alla volta.
    -   Più code possono leggere dalla risorsa, purché non leggano i byte modificati dal writer (la lettura dei byte scritti simultaneamente produce risultati non definiti).
    -   È necessario utilizzare una recinzione per sincronizzare dopo la scrittura prima che un'altra coda possa leggere i byte scritti o effettuare qualsiasi accesso in scrittura.

-   I buffer indietro presentati devono trovarsi nello \_ stato comune della risorsa Direct3D 12 \_ \_ . 

## <a name="related-topics"></a>Argomenti correlati

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)

[Uso delle barriere delle risorse per sincronizzare gli Stati delle risorse in Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[Gestione della memoria in Direct3D 12](memory-management.md)
