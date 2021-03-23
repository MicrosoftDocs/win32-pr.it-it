---
title: Esecuzione e sincronizzazione degli elenchi di comandi
description: In Microsoft Direct3D 12 la modalità immediata delle versioni precedenti non è più presente.
ms.assetid: D5013102-2302-4D66-8F59-079C03BA65FD
keywords:
- Elenco comandi
- sincronizzazione
- esecuzione
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef910463ba3a771ac142d41309ae590884e3bc9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548900"
---
# <a name="executing-and-synchronizing-command-lists"></a>Esecuzione e sincronizzazione degli elenchi di comandi

In Microsoft Direct3D 12 la modalità immediata delle versioni precedenti non è più presente. Al contrario, le app creano elenchi di comandi e bundle, quindi registrano set di comandi GPU. Le code di comando vengono usate per inviare elenchi di comandi da eseguire. Questo modello consente agli sviluppatori di avere un maggiore controllo sull'utilizzo efficiente di GPU (Graphics Processing Unit) e CPU.

-   [Panoramica della coda di comandi](#command-queue-overview)
-   [Inizializzazione di una coda di comandi](#initializing-a-command-queue)
-   [Esecuzione di elenchi di comandi](#executing-command-lists)
-   [Accesso alle risorse da più code dei comandi](#accessing-resources-from-multiple-command-queues)
-   [Sincronizzazione dell'esecuzione dell'elenco dei comandi mediante le schermate della coda dei comandi](#synchronizing-command-list-execution-using-command-queue-fences)
-   [Sincronizzazione delle risorse accessibili dalle code dei comandi](#synchronizing-resources-accessed-by-command-queues)
-   [Supporto della coda dei comandi per le risorse affiancate](#command-queue-support-for-tiled-resources)
-   [Argomenti correlati](#related-topics)

## <a name="command-queue-overview"></a>Panoramica della coda di comandi

Le code dei comandi Direct3D 12 sostituiscono la sincronizzazione del runtime e del driver dell'invio del lavoro in modalità immediata, in precedenza non esposto allo sviluppatore, con le API per la gestione esplicita della concorrenza, il parallelismo e la sincronizzazione. Le code dei comandi offrono i miglioramenti seguenti per gli sviluppatori:

-   Consente agli sviluppatori di evitare inefficienze accidentali dovute a una sincronizzazione imprevista.
-   Consente agli sviluppatori di introdurre la sincronizzazione a un livello superiore in cui la sincronizzazione necessaria può essere determinata in modo più efficiente e accurato. Ciò significa che il runtime e il driver di grafica dedicano meno tempo al parallelismo ingegneristico.
-   Semplifica le operazioni di costo più esplicite.

Questi miglioramenti abilitano o migliorano gli scenari seguenti:

-   Maggiore parallelismo: le applicazioni possono usare code più profonde per i carichi di lavoro in background, ad esempio la decodifica video, quando hanno code separate per il lavoro in primo piano.
-   Lavoro GPU asincrono e con priorità bassa: il modello di coda dei comandi consente l'esecuzione simultanea di operazioni di GPU a priorità bassa e operazioni atomiche che consentono a un thread GPU di utilizzare i risultati di un altro thread non sincronizzato senza bloccarsi.
-   Lavoro di calcolo ad alta priorità: questa progettazione consente scenari che richiedono l'interruzione del rendering 3D per eseguire una piccola quantità di lavoro di calcolo con priorità alta, in modo che il risultato possa essere ottenuto in anticipo per un'ulteriore elaborazione della CPU.

## <a name="initializing-a-command-queue"></a>Inizializzazione di una coda di comandi

È possibile creare le code dei comandi chiamando [**ID3D12Device:: CreateCommandQueue**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandqueue). Questo metodo accetta un [**\_ tipo di \_ elenco \_ di comandi D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type) che indica il tipo di coda da creare e, di conseguenza, il tipo di comandi che possono essere inviati a tale coda. Tenere presente che i bundle possono essere chiamati solo da elenchi di comandi diretti e non possono essere inviati direttamente a una coda. I tipi di coda supportati sono:

-   [**\_Tipo di elenco comandi di D3D12 \_ \_ \_ diretto**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**\_Tipo di \_ elenco di comandi \_ D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**\_ \_ \_ Copia tipo elenco comandi \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)

In generale, le code e gli elenchi di comandi diretti accettano qualsiasi comando, le code di calcolo e gli elenchi di comandi accettano i comandi di calcolo e copia e le code e gli elenchi di comandi accettano solo i comandi di copia.

## <a name="executing-command-lists"></a>Esecuzione di elenchi di comandi

Una volta registrato un elenco di comandi e recuperato la coda dei comandi predefinita o ne è stato creato uno nuovo, è possibile eseguire gli elenchi di comandi chiamando [**ID3D12CommandQueue:: oggetti executecommandlist**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

Le applicazioni possono inviare elenchi di comandi a qualsiasi coda dei comandi da più thread. Il runtime eseguirà il lavoro di serializzazione di queste richieste nell'ordine di invio.

Il runtime convaliderà l'elenco dei comandi inviati ed eliminerà la chiamata a [**oggetti executecommandlist**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) se viene violata una qualsiasi restrizione. Le chiamate verranno eliminate per i motivi seguenti:

-   L'elenco dei comandi fornito è un bundle, non un elenco di comandi diretto.
-   [**ID3D12GraphicsCommandList:: Close**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close) non è stato chiamato sull'elenco di comandi fornito per completare la registrazione.
-   [**ID3D12CommandAllocator:: Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandallocator-reset) è stato chiamato sull'allocatore di comandi associato all'elenco di comandi perché è stato registrato. Per altre informazioni sugli allocatori di comandi, vedere [creazione e registrazione di elenchi di comandi e bundle](recording-command-lists-and-bundles.md).
-   Il limite della coda dei comandi indica che un'esecuzione precedente dell'elenco di comandi non è ancora stata completata. Le barriere della coda di comandi sono descritte in dettaglio di seguito.
-   Gli Stati before e After delle query, impostati con chiamate a [**ID3D12GraphicsCommandList:: BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**ID3D12GraphicsCommandList:: EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery), non corrispondono correttamente.
-   Gli Stati before e After degli ostacoli alla transizione delle risorse non corrispondono correttamente. Per ulteriori informazioni, vedere [utilizzo delle barriere delle risorse per sincronizzare gli Stati delle risorse](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="accessing-resources-from-multiple-command-queues"></a>Accesso alle risorse da più code dei comandi

Esistono un paio di regole imposte dal runtime che limitano l'accesso alle risorse da più code dei comandi. Le regole sono le seguenti:

<dl> 1. Non è possibile scrivere una risorsa da più code di comando contemporaneamente. Quando una risorsa è passata a uno stato scrivibile in una coda, viene considerata esclusivamente di proprietà di tale coda ed è necessario passare a uno stato di lettura o comune (vedere <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">**\_ \_ gli Stati delle risorse D3D12**</a>) prima che sia possibile accedervi da un'altra coda.  </dl>
<dl> 2. Quando si trova in uno stato di lettura, una risorsa può essere letta simultaneamente da più code di comandi, inclusi tra i processi, in base allo stato di lettura. </dl>

Per altre informazioni sulle restrizioni di accesso alle risorse e sull'uso di barriere per la sincronizzazione dell'accesso alle risorse, vedere [uso delle barriere delle risorse per sincronizzare gli Stati delle risorse](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="synchronizing-command-list-execution-using-command-queue-fences"></a>Sincronizzazione dell'esecuzione dell'elenco dei comandi mediante le schermate della coda dei comandi

Il supporto per più code di comandi parallele in Direct3D 12 offre maggiore flessibilità e controllo sulla definizione delle priorità del lavoro asincrono sulla GPU. Questo progetto significa anche che le app devono gestire in modo esplicito la sincronizzazione del lavoro, soprattutto quando gli elenchi di comandi in una coda dipendono dalle risorse che vengono gestite da un'altra coda dei comandi. Alcuni esempi includono l'attesa del completamento di un'operazione in una coda di calcolo in modo che il risultato possa essere usato per un'operazione di rendering nella coda 3D e in attesa del completamento di un'operazione 3D in modo che un'operazione nella coda di calcolo possa accedere a una risorsa per la scrittura. Per abilitare la sincronizzazione del lavoro tra le code, Direct3D 12 USA il concetto di recinzioni, rappresentate nell'API dall'interfaccia [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) .

Una recinzione è un numero intero che rappresenta l'unità di lavoro corrente in fase di elaborazione. Quando l'app sposta il limite, chiamando [**ID3D12CommandQueue:: Signal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal), viene aggiornato l'intero. Le app possono verificare il valore di una recinzione e determinare se un'unità di lavoro è stata completata per decidere se un'operazione successiva può essere avviata.

## <a name="synchronizing-resources-accessed-by-command-queues"></a>Sincronizzazione delle risorse accessibili dalle code dei comandi

In Direct3D 12 la sincronizzazione dello stato di alcune risorse viene implementata con le barriere delle risorse. In ogni barriera delle risorse, un'applicazione dichiara gli Stati before e after di una risorsa. Un esempio comune è la transizione di una risorsa tra una visualizzazione delle risorse dello shader e la visualizzazione di una destinazione di rendering. Nella maggior parte dei casi, queste barriere delle risorse vengono gestite all'interno degli elenchi di comandi. Quando i livelli di debug sono abilitati, il sistema impone che gli Stati before e after di tutte le risorse corrispondano, garantendo che la risorsa si trovi nello stato corretto per una determinata operazione in una transizione di barriera.

Per ulteriori informazioni sulla sincronizzazione dello stato delle risorse, vedere [utilizzo delle barriere delle risorse per sincronizzare gli Stati delle risorse](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="command-queue-support-for-tiled-resources"></a>Supporto della coda dei comandi per le risorse affiancate

I metodi per la gestione delle risorse affiancate, esposti tramite l'interfaccia [**ID3D11DeviceContext2**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) in Direct3D 11, sono forniti dall'interfaccia [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) in Direct3D 12. Questi metodi includono:



| Metodo                                                              | Descrizione                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings)     | Copia i mapping da una risorsa di origine affiancata a una risorsa affiancata di destinazione.<br/>                 |
| [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) | Aggiorna i mapping delle posizioni dei riquadri nelle risorse affiancate alle posizioni di memoria in un heap delle risorse.<br/> |



 

Per altre informazioni sull'uso di risorse affiancate in app Direct3D 12, vedere [risorse affiancate di Direct3D11](/windows/desktop/direct3d11/tiled-resources).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Invio di lavoro in Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

