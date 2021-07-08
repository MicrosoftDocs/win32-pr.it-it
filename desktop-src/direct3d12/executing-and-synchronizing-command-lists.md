---
title: Esecuzione e sincronizzazione di elenchi di comandi
description: In Microsoft Direct3D 12 la modalità immediata delle versioni precedenti non è più presente.
ms.assetid: D5013102-2302-4D66-8F59-079C03BA65FD
keywords:
- elenco dei comandi
- sincronizzazione
- esecuzione
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d5362d0f093c7c1034e03d396ad28c40d4d600
ms.sourcegitcommit: 170bc12e9724d00cecbb96d57c7226c51e135dee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113489181"
---
# <a name="executing-and-synchronizing-command-lists"></a>Esecuzione e sincronizzazione di elenchi di comandi

In Microsoft Direct3D 12 la modalità immediata delle versioni precedenti non è più presente. Al contrario, le app creano elenchi di comandi e aggregazioni e quindi set di record di comandi GPU. Le code di comandi vengono usate per inviare elenchi di comandi da eseguire. Questo modello consente agli sviluppatori di avere un maggiore controllo sull'utilizzo efficiente delle unità di elaborazione grafica (GPU) e della CPU.

-   [Panoramica della coda di comandi](#command-queue-overview)
-   [Inizializzazione di una coda di comandi](#initializing-a-command-queue)
-   [Esecuzione di elenchi di comandi](#executing-command-lists)
-   [Accesso alle risorse da più code di comandi](#accessing-resources-from-multiple-command-queues)
-   [Sincronizzazione dell'esecuzione dell'elenco dei comandi tramite i recinti della coda di comandi](#synchronizing-command-list-execution-using-command-queue-fences)
-   [Sincronizzazione delle risorse accessibili dalle code di comandi](#synchronizing-resources-accessed-by-command-queues)
-   [Supporto della coda di comandi per le risorse affiancate](#command-queue-support-for-tiled-resources)
-   [Argomenti correlati](#related-topics)

## <a name="command-queue-overview"></a>Panoramica della coda di comandi

Le code di comandi Direct3D 12 sostituiscono la sincronizzazione di runtime e driver dell'invio immediato del lavoro in modalità, in precedenza non esposto allo sviluppatore, con API per la gestione esplicita di concorrenza, parallelismo e sincronizzazione. Le code dei comandi offrono i miglioramenti seguenti per gli sviluppatori:

-   Consente agli sviluppatori di evitare inefficienze accidentali causate da una sincronizzazione imprevista.
-   Consente agli sviluppatori di introdurre la sincronizzazione a un livello superiore in cui la sincronizzazione richiesta può essere determinata in modo più efficiente e accurato. Ciò significa che il runtime e il driver di grafica dedicano meno tempo alla progettazione reattiva del parallelismo.
-   Rende più esplicite le operazioni costose.

Questi miglioramenti consentono o migliorano gli scenari seguenti:

-   Maggiore parallelismo: le applicazioni possono usare code più approfondite per i carichi di lavoro in background, ad esempio la decodifica video, quando hanno code separate per il lavoro in primo piano.
-   Lavoro asincrono e con priorità bassa della GPU: il modello di coda dei comandi consente l'esecuzione simultanea di operazioni atomiche e operazioni GPU con priorità bassa che consentono a un thread GPU di utilizzare i risultati di un altro thread non sincronizzato senza blocco.
-   Lavoro di calcolo ad alta priorità: questa progettazione consente agli scenari che richiedono l'interruzione del rendering 3D per eseguire una piccola quantità di operazioni di calcolo ad alta priorità in modo che il risultato possa essere ottenuto in anticipo per l'elaborazione aggiuntiva nella CPU.

## <a name="initializing-a-command-queue"></a>Inizializzazione di una coda di comandi

Le code di comandi possono essere create chiamando [**ID3D12Device::CreateCommandQueue.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) Questo metodo accetta [**un tipo D3D12 \_ COMMAND LIST \_ \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type) che indica il tipo di coda da creare e, di conseguenza, il tipo di comandi che è possibile inviare a tale coda. Tenere presente che i bundle possono essere chiamati solo da elenchi di comandi diretti e non possono essere inviati direttamente a una coda. I tipi di coda supportati sono:

-   [**TIPO DI ELENCO DEI COMANDI D3D12 \_ \_ \_ \_ DIRECT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**CALCOLO TIPO ELENCO COMANDI D3D12 \_ \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**COPIA TIPO ELENCO COMANDI D3D12 \_ \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)

In generale, le code e gli elenchi di comandi DIRECT accettano qualsiasi comando, le code COMPUTE e gli elenchi di comandi accettano i comandi correlati di calcolo e copia e le code COPY e gli elenchi di comandi accettano solo comandi di copia.

## <a name="executing-command-lists"></a>Esecuzione di elenchi di comandi

Dopo aver registrato un elenco di comandi e recuperato la coda di comandi predefinita o creato un nuovo elenco, è possibile eseguire gli elenchi di comandi chiamando [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

Le applicazioni possono inviare elenchi di comandi a qualsiasi coda di comandi da più thread. Il runtime eseguirà il lavoro di serializzazione di queste richieste nell'ordine di invio.

Il runtime convaliderà l'elenco di comandi inviati ed elimina la chiamata a [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) se viene violata una delle restrizioni. Le chiamate verranno eliminate per i motivi seguenti:

-   L'elenco di comandi fornito è un bundle, non un elenco di comandi diretti.
-   [**ID3D12GraphicsCommandList::Close**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close) non è stato chiamato nell'elenco di comandi fornito per completare la registrazione.
-   [**ID3D12CommandAllocator::Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandallocator-reset) è stato chiamato sull'allocatore di comandi associato all'elenco dei comandi da quando è stato registrato. Per altre informazioni sugli allocatori dei comandi, vedere [Creazione e registrazione di elenchi di comandi e aggregazioni.](recording-command-lists-and-bundles.md)
-   Il limite della coda dei comandi indica che un'esecuzione precedente dell'elenco di comandi non è stata ancora completata. I recinti della coda dei comandi sono descritti in dettaglio di seguito.
-   Gli stati prima e dopo le query, impostati con chiamate a [**ID3D12GraphicsCommandList::BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**ID3D12GraphicsCommandList::EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery), non corrispondono correttamente.
-   Gli stati prima e dopo le barriere di transizione delle risorse non corrispondono correttamente. Per altre informazioni, vedere Uso delle [barriere delle risorse per sincronizzare gli stati delle risorse.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

## <a name="accessing-resources-from-multiple-command-queues"></a>Accesso alle risorse da più code di comandi

Il runtime impone un paio di regole che limitano l'accesso delle risorse da più code di comandi. Le regole sono le seguenti:

1. Non è possibile scrivere una risorsa da più code di comandi contemporaneamente. Quando una risorsa è passata a uno stato scrivibile in una coda, viene considerata esclusivamente di proprietà di tale coda e deve passare a uno stato di lettura o COMMON (vedere [**D3D12_RESOURCE_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)) prima che sia accessibile da un'altra coda.

2. In uno stato di lettura, una risorsa può essere letta contemporaneamente da più code di comandi, inclusi i processi, in base al relativo stato di lettura.

Per altre informazioni sulle restrizioni di accesso alle risorse e sull'uso delle barriere delle risorse per sincronizzare l'accesso alle risorse, vedere Uso delle barriere delle risorse [per sincronizzare gli stati delle risorse.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

## <a name="synchronizing-command-list-execution-using-command-queue-fences"></a>Sincronizzazione dell'esecuzione dell'elenco dei comandi tramite i recinti della coda di comandi

Il supporto per più code di comandi paralleli in Direct3D 12 offre maggiore flessibilità e controllo sulla definizione delle priorità del lavoro asincrono sulla GPU. Questa progettazione implica anche che le app devono gestire in modo esplicito la sincronizzazione del lavoro, soprattutto quando gli elenchi di comandi in una coda dipendono dalle risorse gestite da un'altra coda di comandi. Alcuni esempi includono l'attesa del completamento di un'operazione in una coda di calcolo in modo che il risultato possa essere usato per un'operazione di rendering nella coda 3D e l'attesa del completamento di un'operazione 3D in modo che un'operazione nella coda di calcolo possa accedere a una risorsa per la scrittura. Per abilitare la sincronizzazione del lavoro tra le code, Direct3D 12 usa il concetto di recinti, rappresentati nell'API [**dall'interfaccia ID3D12Fence.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)

Un limite è un numero intero che rappresenta l'unità di lavoro corrente in fase di elaborazione. Quando l'app fa avanzare il limite chiamando [**ID3D12CommandQueue::Signal,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal)il numero intero viene aggiornato. Le app possono controllare il valore di un limite e determinare se un'unità di lavoro è stata completata per decidere se un'operazione successiva può essere avviata.

## <a name="synchronizing-resources-accessed-by-command-queues"></a>Sincronizzazione delle risorse accessibili dalle code di comandi

In Direct3D 12 la sincronizzazione dello stato di alcune risorse viene implementata con barriere di risorse. In ogni barriera di risorse, un'app dichiara gli stati prima e dopo di una risorsa. Un esempio comune è la transizione di una risorsa tra una visualizzazione risorse shader e una visualizzazione di destinazione di rendering. Nella maggior parte dei casi, queste barriere di risorse vengono gestite all'interno di elenchi di comandi. Quando i livelli di debug sono abilitati, il sistema impone che gli stati prima e dopo di tutte le risorse corrispondano, garantendo che la risorsa si trova nello stato corretto per una determinata operazione in corrispondenza di una transizione della barriera.

Per altre informazioni sulla sincronizzazione dello stato delle risorse, vedere Uso [delle barriere delle risorse per sincronizzare gli stati delle risorse.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

## <a name="command-queue-support-for-tiled-resources"></a>Supporto della coda di comandi per le risorse affiancate

I metodi per la gestione delle risorse affiancate, esposti tramite l'interfaccia [**ID3D11DeviceContext2**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) in Direct3D 11, vengono forniti dall'interfaccia [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) in Direct3D 12. Questi metodi includono:



| Metodo                                                              | Descrizione                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings)     | Copia i mapping da una risorsa affiancata di origine a una risorsa affiancata di destinazione.<br/>                 |
| [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) | Aggiorna i mapping delle posizioni dei riquadri nelle risorse affiancate alle posizioni di memoria in un heap delle risorse.<br/> |



 

Per altre informazioni sull'uso di risorse affiancate nelle app Direct3D 12, vedere Risorse affiancate [direct3D11.](/windows/desktop/direct3d11/tiled-resources)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Invio di lavoro in Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

