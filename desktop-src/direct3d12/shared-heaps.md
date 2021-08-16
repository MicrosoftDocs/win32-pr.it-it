---
title: Heap condivisi
description: La condivisione è utile per architetture a più processi e schede.
ms.assetid: 67C6B1D4-BF76-45A9-BADC-7C9520C900EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e1bc0826651334d3d137466cc34d194fb79ae4900075b9a145859c5fd37fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300812"
---
# <a name="shared-heaps"></a>Heap condivisi

La condivisione è utile per architetture a più processi e schede.

-   [Panoramica della condivisione](#sharing-overview)
-   [Condivisione di heap tra processi](#sharing-heaps-across-processes)
-   [Condivisione di heap tra schede](#sharing-heaps-across-adapters)
-   [Argomenti correlati](#related-topics)

## <a name="sharing-overview"></a>Panoramica della condivisione

Gli heap condivisi consentono due operazioni: la condivisione dei dati in un heap tra uno o più processi e la preclitura di una scelta non deterministica di layout di trama non definito per le risorse posizionate all'interno dell'heap. La condivisione di heap tra schede elimina anche la necessità di effettuare il marshalling della CPU dei dati.

Sia gli heap che le risorse di cui è stato eseguito il commit possono essere condivisi. La condivisione di una risorsa di cui è stato eseguito il commit condivide effettivamente l'heap implicito insieme alla descrizione della risorsa di cui è stato eseguito il commit, in modo che sia possibile eseguire il mapping di una descrizione di risorsa compatibile all'heap da un altro dispositivo.

Tutti i metodi sono a thread libero ed ereditano la semantica D3D11 esistente della progettazione di condivisione degli handle NT.

-   [**ID3D12Device::CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**ID3D12Device::OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
-   [**ID3D12Device::OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)

## <a name="sharing-heaps-across-processes"></a>Condivisione di heap tra processi

Gli heap condivisi vengono specificati con il membro D3D12 \_ HEAP \_ FLAG SHARED \_ [**dell'enumerazione D3D12 \_ HEAP \_ FLAGS.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)

Gli heap condivisi non sono supportati negli heap accessibili dalla CPU: D3D12 \_ HEAP \_ TYPE \_ UPLOAD, D3D12 \_ HEAP TYPE \_ \_ READBACK e D3D12 \_ HEAP TYPE CUSTOM senza \_ \_ D3D12 \_ CPU PAGE PROPERTY NOT \_ \_ \_ \_ AVAILABLE.

Precluding a non-deterministic choice of undefined texture layout can significantly impaired rendering scenarios on some GPU, so it is not the default behavior for placed and committed resources. Il rendering posticipato è compromesso in alcune architetture GPU perché i layout di trama deterministici riducono la larghezza di banda di memoria effettiva ottenuta quando il rendering viene eseguito simultaneamente su più trame di destinazione di rendering dello stesso formato e dimensione. Le architetture GPU si evolvono dall'uso di layout di trama non deterministici per supportare in modo efficiente modelli di swizzle standardizzati e layout standardizzati per il rendering posticipato.

Anche gli heap condivisi sono associati ad altri costi secondari:

-   I dati dell'heap condiviso non possono essere riciclati in modo flessibile come gli heap in-process a causa di problemi di diffusione di informazioni, quindi la memoria fisica è zero più spesso.
-   Si verifica un sovraccarico aggiuntivo della CPU minore e un maggiore utilizzo della memoria di sistema durante la creazione e la distruzione di heap condivisi.

## <a name="sharing-heaps-across-adapters"></a>Condivisione di heap tra schede

Gli heap condivisi tra schede vengono specificati con il membro SHARED CROSS ADAPTER D3D12 HEAP FLAG SHARED dell'enumerazione \_ \_ \_ \_ \_ [**D3D12 \_ HEAP \_ FLAGS.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)

Gli heap condivisi tra adattatori consentono a più schede di condividere i dati senza che la CPU eserviti il marshalling dei dati tra di essi. Anche se le diverse funzionalità dell'adattatore determinano l'efficienza con cui le schede possono passare dati tra di esse, la semplice abilitazione delle copie GPU aumenta la larghezza di banda effettiva ottenuta. Alcuni layout di trama sono consentiti negli heap degli adattatori incrociati per supportare un interscambio di dati di trama, anche se tali layout di trama non sono altrimenti supportati. A tali trame possono essere applicate alcune restrizioni, ad esempio solo il supporto della copia.

La condivisione tra adattatori funziona con gli heap creati chiamando [**ID3D12Device::CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap). Le applicazioni possono quindi creare risorse [**tramite CreatePlacedResource.**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource) È consentito anche dalle risorse o dagli heap creati da [**CreateCommittedResource,**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) ma solo per le risorse D3D12 RESOURCE DIMENSION TEXTURE2D principali della riga \_ \_ \_ (vedere [**D3D12 \_ RESOURCE \_ DIMENSION).**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension) La condivisione tra adattatori non funziona [**con CreateReservedResource.**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource)

Per la condivisione tra schede, vengono comunque applicate tutte le normali regole di condivisione delle risorse tra code. Le applicazioni devono rilasciare le barriere appropriate per garantire la sincronizzazione e la coerenza appropriate tra le due schede. Le applicazioni devono usare i recinti tra adattatori per coordinare la pianificazione degli elenchi di comandi inviati a più schede. Non esiste alcun meccanismo per condividere le risorse tra schede tra le versioni dell'API D3D. Le risorse condivise tra adattatori sono supportate solo nella memoria di sistema. Le risorse/heap condivisi tra adattatori sono supportati negli heap D3D12 HEAP TYPE DEFAULT e NEGLI heap PERSONALIZZATI DI TIPO \_ \_ HEAP \_ D3D12 (con il pool di memoria \_ \_ L0 e le proprietà della pagina \_ DELLA CPU per la combinazione di scrittura). I driver devono assicurarsi che le operazioni di lettura/scrittura della GPU per gli heap condivisi tra schede siano coerenti con altre GPU nel sistema. Ad esempio, il driver potrebbe dover escludere i dati dell'heap da cache GPU che in genere non devono essere scaricate quando la CPU non può accedere direttamente ai dati dell'heap.

Le applicazioni devono limitare l'utilizzo degli heap tra adattatori solo agli scenari che richiedono la funzionalità che forniscono. Gli heap degli adattatori incrociati si trovano in D3D12 MEMORY POOL L0, che non è sempre quello suggerito da \_ \_ \_ [**GetCustomHeapProperties.**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) Questo pool di memoria non è efficiente per le architetture di adapter DISCRETE/NUMA. E i layout di trama più efficienti non sono sempre disponibili.

Vengono applicate anche le seguenti limitazioni:

-   I flag dell'heap correlati ai livelli heap devono essere FLAG HEAP D3D12 \_ \_ ALLOW ALL \_ \_ \_ BUFFERS E \_ \_ TEXTURES.
-   È necessario impostare anche IL FLAG HEAP D3D12 \_ \_ \_ SHARED.
-   È necessario impostare D3D12 HEAP TYPE DEFAULT o \_ \_ \_ D3D12 \_ HEAP TYPE CUSTOM con \_ \_ D3D12 \_ MEMORY POOL \_ \_ L0 e D3D12 \_ CPU PAGE PROPERTY NOT \_ \_ \_ \_ AVAILABLE.
-   Solo le risorse con D3D12 RESOURCE FLAG ALLOW CROSS ADAPTER possono essere \_ inserite negli heap degli \_ \_ \_ \_ adattatori incrociati.

Per altre informazioni sull'uso di più schede, vedere la [sezione Sistemi a più](multi-engine.md) schede.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sottoallocazione all'interno degli heap](suballocation-within-heaps.md)
</dt> </dl>

 

 




