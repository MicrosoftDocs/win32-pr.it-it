---
title: Impostazione e popolamento degli heap descrittore
description: I tipi di heap del descrittore che è possibile impostare in un elenco di comandi sono quelli che contengono descrittori per cui è possibile usare le tabelle dei descrittori (al massimo uno per volta).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e3a1b6c4863827e1d8e1bdfb33a0a64420211d
ms.sourcegitcommit: 584b35959515bc5e4a104e8cf5270513f146f590
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "104548813"
---
# <a name="setting-and-populating-descriptor-heaps"></a>Impostazione e popolamento degli heap descrittore

I tipi di heap del descrittore che è possibile impostare in un elenco di comandi sono quelli che contengono descrittori per cui è possibile usare le tabelle dei descrittori (al massimo uno per volta).

-   [Impostazione degli heap del descrittore](#setting-and-populating-descriptor-heaps)
-   [Popolamento degli heap descrittore](#populating-descriptor-heaps)
-   [Argomenti correlati](#related-topics)

## <a name="setting-descriptor-heaps"></a>Impostazione degli heap del descrittore

I tipi di heap dei descrittori che è possibile impostare in un elenco di comandi sono:

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

Gli heap impostati nell'elenco dei comandi devono essere anche stati creati come shader visibile. Sono disponibili tre tipi di elenco di comandi: DIRECT, BUNDLE e COMPUTE.

Dopo aver impostato un heap dei descrittori in un elenco di comandi, le chiamate successive che definiscono le tabelle dei descrittori fanno riferimento all'heap descrittore corrente. Lo stato della tabella descrittore non è definito all'inizio di un elenco di comandi e dopo che gli heap del descrittore sono stati modificati in un elenco di comandi. L'impostazione ridondante dello stesso heap del descrittore non determina l'indefinizione delle impostazioni della tabella del descrittore.

In un bundle, al contrario, gli heap del descrittore possono essere impostati solo una volta (le chiamate ridondanti che imposta lo stesso heap due volte non generano un errore); in caso contrario, il comportamento non è definito. Gli heap del descrittore impostati devono corrispondere allo stato quando un elenco di comandi chiama il bundle; in caso contrario, il comportamento non è definito. In questo modo, i bundle possono ereditare e modificare le impostazioni della tabella descrittore dell'elenco dei comandi. I bundle che non modificano le tabelle dei descrittori (ereditano solo) non devono necessariamente impostare un heap del descrittore e erediteranno solo dall'elenco dei comandi chiamante.

Quando gli heap del descrittore sono impostati (usando [**ID3D12GraphicsCommandList:: SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), tutti gli heap usati vengono impostati in una singola chiamata (e tutti gli heap impostati in precedenza vengono annullati dalla chiamata). Nella chiamata è possibile impostare al massimo un heap di ogni tipo elencato sopra.

## <a name="populating-descriptor-heaps"></a>Popolamento degli heap descrittore

Dopo che un'applicazione ha creato un heap del descrittore, può usare i metodi del dispositivo per generare descrittori direttamente nell'heap o copiare i descrittori da una posizione a un'altra.

Il contenuto iniziale della memoria heap del descrittore non è definito, pertanto chiedere alla GPU o al driver di fare riferimento alla memoria non inizializzata per il rendering può causare risultati non definiti, ad esempio la reimpostazione del dispositivo.

Se l'applicazione configura un heap del descrittore in modo che sia visibile alla CPU, la CPU può chiamare i metodi per creare descrittori nell'heap e copiarli da una posizione all'altra (inclusi gli heap) in modo immediato e senza thread. Se l'heap è stato configurato come SHADER_VISIBLE, la lettura dalla CPU non è consentita.



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap descrittore](descriptor-heaps.md)
</dt> </dl>

 

 




