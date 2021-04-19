---
title: Interfacce di base (grafica Direct3D 12)
description: Le interfacce seguenti sono dichiarate in d3d12. h.
ms.assetid: A9BD5910-8FF2-4540-BB8E-E8EA5C10528C
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: a51e35fff74ab1d0251d64578de665ad4134a843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299930"
---
# <a name="core-interfaces"></a>Interfacce di base

Le interfacce seguenti sono dichiarate in d3d12. h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator) | Rappresenta le allocazioni di archiviazione per i comandi di unità di elaborazione grafica (GPU). |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist) | Interfaccia da cui [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) eredita da. Rappresenta un set ordinato di comandi eseguiti dalla GPU, consentendo in tal modo all'estensione di supportare altri elenchi di comandi rispetto a quelli per la grafica, ad esempio calcolo e copia. |
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) | Fornisce metodi per l'invio di elenchi di comandi, la sincronizzazione dell'esecuzione dell'elenco di comandi, la strumentazione della coda di comandi e l'aggiornamento dei mapping dei riquadri delle risorse. |
| [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature) | Un oggetto della firma del comando consente alle app di specificare il disegno indiretto, inclusi il formato del buffer, il tipo di comando e le associazioni di risorse da usare. |
| [**ID3D12DescriptorHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12descriptorheap) | Un heap del descrittore è una raccolta di allocazioni contigue di descrittori, un'allocazione per ogni descrittore. Gli heap del descrittore contengono molti tipi di oggetto che non fanno parte di un oggetto di stato della pipeline (PSO), ad esempio viste di risorse shader (SRVs), viste di accesso non ordinate (UAV), viste del buffer costante (CBVs) e Samplers. |
| [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) | Rappresenta una scheda virtuale; viene usato per creare allocatori di comandi, elenchi di comandi, code di comandi, barriere, risorse, oggetti di stato della pipeline, heap, firme radice, sampler e molte visualizzazioni di risorse. |
| [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) | Rappresenta una scheda virtuale ed espande l'intervallo di metodi fornito da [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device). |
| [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) | Rappresenta una scheda virtuale. Questa interfaccia estende [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) per creare oggetti stato della pipeline dalle descrizioni del flusso dello stato della pipeline. |
| [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) | Rappresenta una scheda virtuale. Questa interfaccia estende [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) per supportare la creazione di heap di diagnostica per scopi specifici nella memoria di sistema che viene mantenute anche in caso di errore GPU o di uno scenario rimosso da dispositivo. |
| [**ID3D12Device4**](/windows/win32/api/d3d12/nn-d3d12-id3d12device4) | Rappresenta una scheda virtuale. Questa interfaccia estende [ID3D12Device3](/windows/win32/api/d3d12/nn-d3d12-id3d12device3). |
| [**ID3D12Device5**](/windows/win32/api/d3d12/nn-d3d12-id3d12device5) | Rappresenta una scheda virtuale. Questa interfaccia estende [ID3D12Device4](/windows/win32/api/d3d12/nn-d3d12-id3d12device4). |
| [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) | Rappresenta una scheda virtuale. Questa interfaccia estende [ID3D12Device5](/windows/win32/api/d3d12/nn-d3d12-id3d12device5). |
| [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) | Interfaccia da cui ereditano altre interfacce principali, tra cui [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary), [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist), [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable)e [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature). Fornisce un metodo per tornare all'oggetto dispositivo in cui è stato creato. |
| [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) | Fornisce l'accesso in fase di esecuzione ai dati dei dati estesi (eseguire) rimossi dal dispositivo. |
| [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) | Questa interfaccia controlla le impostazioni dei dati estesi del dispositivo rimossi (eseguire). |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) | Rappresenta una recinzione, un oggetto usato per la sincronizzazione della CPU e una o più GPU.  |
| [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) | Rappresenta una recinzione. Questa interfaccia estende [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)e supporta il recupero dei flag utilizzati per creare la recinzione originale.  |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) | Incapsula un elenco di comandi grafici per il rendering. Include API per la strumentazione dell'esecuzione dell'elenco di comandi e per l'impostazione e la cancellazione dello stato della pipeline. |
| [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1) | Incapsula un elenco di comandi grafici per il rendering, estendendo il interfaccia per supportare le posizioni di esempio programmabili, le copie atomiche per l'implementazione di tecniche di latch tardivo e il test facoltativo dei limiti di profondità. |
| [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) | Incapsula un elenco di comandi grafici per il rendering, estendendo l'interfaccia per supportare la scrittura immediata di valori direttamente in un buffer. |
| [**ID3D12GraphicsCommandList3**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist3) | Incapsula un elenco di comandi grafici per il rendering. |
| [**ID3D12GraphicsCommandList4**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist4) | Incapsula un elenco di comandi grafici per il rendering, estendendo l'interfaccia per supportare il passaggio di traccia e di rendering del Ray. |
| [**ID3D12Heap**](/windows/win32/api/d3d12/nn-d3d12-id3d12heap) | Un heap è un'astrazione dell'allocazione di memoria contigua, utilizzata per gestire la memoria fisica. Questo heap può essere usato con oggetti [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) per supportare risorse posizionate o risorse riservate. |
| [**ID3D12LifetimeOwner**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimeowner) | Rappresenta un callback definito dall'applicazione utilizzato per ricevere una notifica delle modifiche di durata di un oggetto. |
| [**ID3D12LifetimeTracker**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimetracker) | Rappresenta le funzionalità per controllare la durata di un oggetto con rilevamento della durata. |
| [**ID3D12MetaCommand**](/windows/win32/api/d3d12/nn-d3d12-id3d12metacommand) | Rappresenta un meta Command. Un meta Command è un oggetto Direct3D 12 che rappresenta un algoritmo che viene accelerato da fornitori di hardware indipendenti (IHV). Si tratta di un riferimento opaco a un generatore di comandi implementato dal driver. |
| [**ID3D12Object**](/windows/win32/api/d3d12/nn-d3d12-id3d12object) | Interfaccia da cui ereditano [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) e [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) . Fornisce metodi per associare i dati privati e annotare i nomi degli oggetti. |
| [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable) | Interfaccia da cui molte altre interfacce principali ereditano da. Indica che il tipo di oggetto incapsula una certa quantità di memoria accessibile dalla GPU. ma non indica chiaramente se l'applicazione può modificare la residenza dell'oggetto.  |
| [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) | Gestisce una libreria di pipeline, in particolare il caricamento e il recupero di singoli PSO. |
| [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1) | Gestisce una libreria di pipeline. Questa interfaccia estende [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) per caricare PSO da una descrizione del flusso di stato della pipeline. |
| [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) | Rappresenta lo stato di tutti gli shader attualmente impostati, nonché alcuni oggetti di stato della funzione fissa. |
| [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) | Gestisce un heap di query. Un heap di query include una matrice di query, a cui fanno riferimento gli indici. |
| [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) | Incapsula una capacità generalizzata di CPU e GPU per la lettura e la scrittura in memoria fisica o heap. Contiene astrazioni per l'organizzazione e la manipolazione di semplici matrici di dati, nonché dati multidimensionali ottimizzati per il campionamento dello shader. |
| [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) | La firma radice definisce quali risorse sono associate alla pipeline grafica. Una firma radice viene configurata tramite l'app e collega gli elenchi di comandi alle risorse necessarie per gli shader. Attualmente sono presenti una grafica e una firma radice di calcolo per ogni app. |
| [**ID3D12RootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) | Contiene un metodo per restituire la struttura dei dati [**D3D12-root-Signature-desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) deserializzata di una firma radice serializzata versione 1,0.  |
| [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject) | Rappresenta una quantità variabile di stato di configurazione, inclusi gli shader, che un'applicazione gestisce come una singola unità e che viene assegnata a un driver in modo atomico per l'elaborazione, ad esempio la compilazione o l'ottimizzazione.  |
| [**ID3D12StateObjectProperties**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobjectproperties) | Fornisce metodi per ottenere e impostare le proprietà di un [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject).  |
| [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools) | Questa interfaccia viene utilizzata per configurare il runtime per strumenti come PIX. Non è previsto né supportato per altri scenari. |
| [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) | Contiene i metodi per restituire la struttura dei dati deserializzati [**D3D12-root-Signature-DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) di qualsiasi versione di una firma radice serializzata.  |

## <a name="related-topics"></a>Argomenti correlati

* [Riferimento principale](direct3d-12-core-reference.md)
* [Guida di riferimento a Direct3D 12](direct3d-12-reference.md)
* [Gerarchia di interfaccia](interface-hierarchy.md)