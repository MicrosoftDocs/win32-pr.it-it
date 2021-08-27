---
title: Impostazione e popolamento degli heap dei descrittori
description: I tipi di heap dei descrittori che possono essere impostati in un elenco di comandi sono quelli che contengono descrittori per i quali è possibile usare le tabelle dei descrittori (al massimo una di ognuna alla volta).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e2fcb7143b097709cb7a3c98669a7d20331bfa9553f4eac5f2cf45a1a90797
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119451"
---
# <a name="setting-and-populating-descriptor-heaps"></a>Impostazione e popolamento degli heap dei descrittori

I tipi di heap dei descrittori che possono essere impostati in un elenco di comandi sono quelli che contengono descrittori per i quali è possibile usare le tabelle dei descrittori (al massimo una di ognuna alla volta).

-   [Impostazione degli heap dei descrittori](#setting-and-populating-descriptor-heaps)
-   [Popolamento degli heap dei descrittori](#populating-descriptor-heaps)
-   [Argomenti correlati](#related-topics)

## <a name="setting-descriptor-heaps"></a>Impostazione degli heap dei descrittori

I tipi di heap dei descrittori che è possibile impostare in un elenco di comandi sono:

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

Anche gli heap impostati nell'elenco dei comandi devono essere stati creati come visibili allo shader. Esistono tre tipi di elenco di comandi: DIRECT, BUNDLE e COMPUTE.

Dopo l'impostazione di un heap descrittore in un elenco di comandi, le chiamate successive che definiscono le tabelle dei descrittori fanno riferimento all'heap descrittore corrente. Lo stato della tabella dei descrittori non è definito all'inizio di un elenco di comandi e dopo la modifica degli heap dei descrittori in un elenco di comandi. L'impostazione ridondante dello stesso heap descrittore non determina l'indefinizione delle impostazioni della tabella dei descrittori.

In un bundle, invece, gli heap dei descrittori possono essere impostati solo una volta (le chiamate ridondanti che impostano due volte lo stesso heap non generano un errore); In caso contrario, il comportamento non è definito. Gli heap dei descrittori impostati devono corrispondere allo stato quando un elenco di comandi chiama il bundle. In caso contrario, il comportamento non è definito. Ciò consente ai bundle di ereditare e modificare le impostazioni della tabella dei descrittori dell'elenco comandi. I bundle che non modificano le tabelle dei descrittori (ereditano solo le tabelle) non devono impostare un heap dei descrittori e erediteranno semplicemente dall'elenco dei comandi chiamanti.

Quando gli heap dei descrittori sono impostati (usando [**ID3D12GraphicsCommandList::SetDescriptorHeaps),**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)tutti gli heap usati vengono impostati in una singola chiamata (e tutti gli heap impostati in precedenza vengono non impostati dalla chiamata). Nella chiamata è possibile impostare al massimo un heap di ogni tipo elencato in precedenza.

## <a name="populating-descriptor-heaps"></a>Popolamento degli heap dei descrittori

Dopo che un'applicazione ha creato un heap descrittore, può usare i metodi nel dispositivo per generare i descrittori direttamente nell'heap o copiare i descrittori da una posizione a un'altra.

Il contenuto iniziale della memoria heap dei descrittori non è definito, pertanto la richiesta alla GPU o al driver di fare riferimento alla memoria non inizializzata per il rendering può causare risultati non definiti, ad esempio una reimpostazione del dispositivo.

Se l'applicazione configura un heap dei descrittori in modo che sia visibile alla CPU, la CPU può chiamare i metodi per creare descrittori nell'heap e copiare da una posizione all'altra (inclusi gli heap) in modo immediato e a thread libero. Se l'heap è stato configurato come SHADER_VISIBLE, la lettura da parte della CPU non è consentita.



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap dei descrittori](descriptor-heaps.md)
</dt> </dl>

 

 




