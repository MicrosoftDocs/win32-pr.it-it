---
title: Heap condivisi
description: La condivisione è utile per le architetture a più processi e a più adapter.
ms.assetid: 67C6B1D4-BF76-45A9-BADC-7C9520C900EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4271055f88e38484041c225b6b17c6d75f0d98
ms.sourcegitcommit: d6102d9e2b26368142fe5b006c65acb50c98be65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/26/2019
ms.locfileid: "74103726"
---
# <a name="shared-heaps"></a>Heap condivisi

La condivisione è utile per le architetture a più processi e a più adapter.

-   [Panoramica della condivisione](#sharing-overview)
-   [Condivisione di heap tra processi](#sharing-heaps-across-processes)
-   [Condivisione degli heap tra gli adapter](#sharing-heaps-across-adapters)
-   [Argomenti correlati](#related-topics)

## <a name="sharing-overview"></a>Panoramica della condivisione

Gli heap condivisi consentono due operazioni: condividere i dati in un heap in uno o più processi e escludere una scelta non deterministica del layout di trama non definito per le risorse posizionate all'interno dell'heap. La condivisione degli heap tra gli adapter consente inoltre di eliminare la necessità di effettuare il marshalling della CPU dei dati.

Gli heap e le risorse di cui è stato eseguito il commit possono essere condivisi. La condivisione di una risorsa di cui è stato eseguito il commit condivide effettivamente l'heap implicito insieme alla descrizione della risorsa di cui è stato eseguito il commit, in modo che sia possibile eseguire il mapping di una descrizione della risorsa compatibile

Tutti i metodi sono a thread libero e ereditano la semantica D3D11 esistente della progettazione della condivisione dell'handle NT.

-   [**ID3D12Device::CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**ID3D12Device::OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
-   [**ID3D12Device::OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)

## <a name="sharing-heaps-across-processes"></a>Condivisione di heap tra processi

Gli heap condivisi vengono specificati con il \_ \_ membro condiviso del flag heap D3D12 \_ dell' [**enumerazione \_ \_ flag heap D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) .

Gli heap condivisi non sono supportati negli heap accessibili dalla CPU: il \_ caricamento del tipo di heap D3D12, il tipo di \_ \_ \_ heap D3D12 \_ \_ READBACK e il \_ tipo di heap D3D12 \_ \_ personalizzati senza \_ proprietà della pagina della CPU D3D12 \_ non sono \_ \_ \_ disponibili.

Se una scelta non deterministica del layout di trama non definito può compromettere in modo significativo scenari di rendering posticipati in alcune GPU, non è il comportamento predefinito per le risorse posizionate e sottoposte a commit. Il rendering posticipato non è associato ad alcune architetture GPU perché i layout di trama deterministico diminuiscono la larghezza di banda di memoria effettiva conseguita durante il rendering simultaneo a più trame di destinazione di rendering dello stesso formato e dimensioni. Le architetture GPU si evolvono dall'uso di layout di trama non deterministici per supportare i modelli swizzle standardizzati e i layout standardizzati in modo efficiente per il rendering posticipato.

Gli heap condivisi sono associati anche ad altri costi secondari:

-   I dati dell'heap condiviso non possono essere riciclati in modo flessibile come gli heap in-process a causa di problemi di divulgazione delle informazioni, quindi la memoria fisica viene zero'ed più spesso.
-   Si verifica un sovraccarico aggiuntivo della CPU e un maggiore utilizzo della memoria di sistema durante la creazione e la distruzione degli heap condivisi.

## <a name="sharing-heaps-across-adapters"></a>Condivisione degli heap tra gli adapter

Gli heap condivisi tra gli adapter vengono specificati con il \_ \_ membro della \_ \_ scheda incrociata D3D12 del flag dell'heap condiviso \_ dell'enum dei [**\_ \_ flag dell'heap di D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) .

Gli heap condivisi tra più adapter consentono a più adapter di condividere i dati senza che venga eseguito il marshalling dei dati tra di essi. Sebbene le diverse funzionalità dell'adapter determinino il modo in cui gli adattatori possono passare i dati tra di essi, l'abilitazione delle copie GPU aumenta la larghezza di banda effettiva. Alcuni layout di trama sono consentiti negli heap tra Adapter per supportare un interscambio di dati di trama, anche se tali layout non sono altrimenti supportati. È possibile che alcune restrizioni si applichino a tali trame, ad esempio solo il supporto della copia.

La condivisione tra Adapter funziona con gli heap creati chiamando [**ID3D12Device:: createheap ha provocato**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap). Le applicazioni possono quindi creare risorse tramite [**CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource). È consentita anche da risorse/heap creati da [**CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) , ma solo per \_ le risorse TEXTURE2D della dimensione della risorsa D3D12 di riga \_ \_ (fare riferimento alla [**\_ \_ dimensione della risorsa D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)). La condivisione tra adapter non funziona con [**CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).

Per la condivisione tra adapter, vengono applicate tutte le normali regole di condivisione delle risorse tra le code. Le applicazioni devono emettere le barriere appropriate per garantire la corretta sincronizzazione e coerenza tra i due adapter. Per coordinare la pianificazione degli elenchi di comandi inviati a più schede, le applicazioni devono utilizzare le barriere tra adapter. Non è disponibile alcun meccanismo per condividere le risorse tra adapter tra le versioni dell'API D3D. Le risorse condivise tra Adapter sono supportate solo nella memoria di sistema. Gli heap o le risorse condivise tra Adapter sono supportati negli heap \_ predefiniti del tipo di heap D3D12 e negli heap \_ \_ \_ \_ \_ personalizzati del tipo di heap D3D12 (con il pool di memoria L0 e le proprietà della pagina CPU della combinazione di scrittura). I driver devono assicurarsi che le operazioni di lettura/scrittura GPU per gli heap condivisi tra adapter siano coerenti con altre GPU nel sistema. Ad esempio, il driver potrebbe avere la necessità di escludere i dati dell'heap da risiedere nelle cache GPU che in genere non devono essere scaricate quando la CPU non può accedere direttamente ai dati dell'heap.

Le applicazioni devono limitare l'utilizzo degli heap tra Adapter solo agli scenari che richiedono la funzionalità fornita. Gli heap tra adapter si trovano nel pool di \_ memoria \_ D3D12 \_ L0, che non è sempre quello che suggerisce [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) . Il pool di memoria non è efficiente per le architetture di adapter discreti/NUMA. I layout di trama più efficienti non sono sempre disponibili.

Vengono applicate anche le seguenti limitazioni:

-   I flag dell'heap correlati ai livelli dell'heap devono essere \_ flag dell'heap D3D12 per \_ \_ consentire \_ tutti i \_ buffer \_ e le \_ trame.
-   \_ \_ È necessario impostare anche il flag dell'heap D3D12 \_ condiviso.
-   È necessario impostare il \_ \_ valore predefinito del tipo di heap D3D12 \_ o il \_ \_ tipo di heap D3D12 \_ personalizzato con il \_ pool di memoria D3D12 \_ \_ L0 e la \_ proprietà della pagina CPU D3D12 \_ \_ \_ non \_ disponibile.
-   Solo le risorse con \_ flag di risorsa D3D12 \_ \_ \_ \_ possono essere inserite in heap tra più adapter.

Per ulteriori informazioni sull'utilizzo di più schede, vedere la sezione sistemi con più [Adapter](multi-engine.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sottoallocazione negli heap](suballocation-within-heaps.md)
</dt> </dl>

 

 




