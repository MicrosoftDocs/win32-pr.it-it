---
title: Interfacce di base (grafica Direct3D 12)
description: Le interfacce seguenti sono dichiarate in d3d12.h.
ms.assetid: A9BD5910-8FF2-4540-BB8E-E8EA5C10528C
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: f204484b3565564f72e815bd21cf8e449ee55e4c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884301"
---
# <a name="core-interfaces"></a>Interfacce di base

Le interfacce seguenti sono dichiarate in d3d12.h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator) | Rappresenta le allocazioni di spazio di archiviazione per i comandi gpu (Graphics Processing Unit). |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist) | Interfaccia da cui [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) eredita. Rappresenta un set ordinato di comandi eseguiti dalla GPU, consentendo al tempo stesso all'estensione di supportare elenchi di comandi diversi da quelli per la grafica(ad esempio calcolo e copia). |
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) | Fornisce metodi per l'invio di elenchi di comandi, la sincronizzazione dell'esecuzione dell'elenco dei comandi, la strumentazione della coda di comandi e l'aggiornamento dei mapping dei riquadri delle risorse. |
| [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature) | Un oggetto firma del comando consente alle app di specificare il disegno indiretto, inclusi il formato del buffer, il tipo di comando e le associazioni di risorse da usare. |
| [**ID3D12DescriptorHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12descriptorheap) | Un heap dei descrittori è una raccolta di allocazioni contigue di descrittori, un'allocazione per ogni descrittore. Gli heap dei descrittori contengono molti tipi di oggetto che non fanno parte di un oggetto stato della pipeline (PSO), ad esempio viste di risorse shader(SPV), viste di accesso non ordinate (UAV), visualizzazioni buffer costanti (CBV) e campionatori. |
| [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) | Rappresenta una scheda virtuale. viene usato per creare allocatori di comandi, elenchi di comandi, code di comandi, recinti, risorse, oggetti di stato della pipeline, heap, firme radice, campionatori e molte visualizzazioni di risorse. |
| [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) | Rappresenta una scheda virtuale ed espande l'intervallo di metodi forniti da [**ID3D12Device.**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) |
| [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) | Rappresenta una scheda virtuale. Questa interfaccia estende [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) per creare oggetti di stato della pipeline dalle descrizioni del flusso di stato della pipeline. |
| [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) | Rappresenta una scheda virtuale. Questa interfaccia estende [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) per supportare la creazione di heap di diagnostica per scopi speciali nella memoria di sistema che vengono mantenuti anche in caso di uno scenario di errore GPU o dispositivo rimosso. |
| [**ID3D12Device4**](/windows/win32/api/d3d12/nn-d3d12-id3d12device4) | Rappresenta una scheda virtuale. Questa interfaccia estende [ID3D12Device3.](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) |
| [**ID3D12Device5**](/windows/win32/api/d3d12/nn-d3d12-id3d12device5) | Rappresenta una scheda virtuale. Questa interfaccia estende [ID3D12Device4.](/windows/win32/api/d3d12/nn-d3d12-id3d12device4) |
| [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) | Rappresenta una scheda virtuale. Questa interfaccia estende [ID3D12Device5.](/windows/win32/api/d3d12/nn-d3d12-id3d12device5) |
| [**ID3D12Device7**](/windows/win32/api/d3d12/nn-d3d12-id3d12device7) | Rappresenta una scheda virtuale. Questa interfaccia estende [ID3D12Device6.](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) |
| [**ID3D12Device8**](/windows/win32/api/d3d12/nn-d3d12-id3d12device8) | Rappresenta una scheda virtuale. Questa interfaccia estende [ID3D12Device7.](/windows/win32/api/d3d12/nn-d3d12-id3d12device7) |
| [**ID3D12Device9**](/windows/win32/api/d3d12/nn-d3d12-id3d12device9) | Rappresenta una scheda virtuale. Questa interfaccia estende [ID3D12Device8](/windows/win32/api/d3d12/nn-d3d12-id3d12device8) per aggiungere metodi per gestire le cache degli shader. |
| [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) | Interfaccia da cui ereditano altre interfacce di base, tra cui [**ID3D12PipelineLibrary,**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) [**ID3D12CommandList,**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist) [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable)e [**ID3D12RootSignature.**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) Fornisce un metodo per tornare all'oggetto dispositivo in cui è stato creato. |
| [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) | Fornisce l'accesso in fase di esecuzione ai dati DRED (Device Removed Extended Data). |
| [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) | Questa interfaccia controlla le impostazioni DRED (Device Removed Extended Data). |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) | Rappresenta un limite, un oggetto utilizzato per la sincronizzazione della CPU e di una o più GPU.  |
| [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) | Rappresenta un limite. Questa interfaccia estende [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)e supporta il recupero dei flag usati per creare il limite originale.  |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) | Incapsula un elenco di comandi grafici per il rendering. Include le API per instrumentare l'esecuzione dell'elenco di comandi e per impostare e cancellare lo stato della pipeline. |
| [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1) | Incapsula un elenco di comandi grafici per il rendering, estendendo l'inteface per supportare le posizioni dei campioni programmabili, copie atomiche per l'implementazione di tecniche di latch tardivo e test facoltativo dei limiti di profondità. |
| [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) | Incapsula un elenco di comandi grafici per il rendering, estendendo l'interfaccia per supportare la scrittura di valori immediati direttamente in un buffer. |
| [**ID3D12GraphicsCommandList3**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist3) | Incapsula un elenco di comandi grafici per il rendering. |
| [**ID3D12GraphicsCommandList4**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist4) | Incapsula un elenco di comandi grafici per il rendering, estendendo l'interfaccia per supportare il ray tracing e i passaggi di rendering. |
| [**ID3D12Heap**](/windows/win32/api/d3d12/nn-d3d12-id3d12heap) | Un heap è un'astrazione dell'allocazione di memoria contigua, usata per gestire la memoria fisica. Questo heap può essere usato con oggetti [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) per supportare le risorse posizionate o riservate. |
| [**ID3D12LifetimeOwner**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimeowner) | Rappresenta un callback definito dall'applicazione utilizzato per ricevere una notifica delle modifiche di durata di un oggetto . |
| [**ID3D12LifetimeTracker**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimetracker) | Rappresenta le funzionalità per il controllo della durata di un oggetto con rilevamento della durata. |
| [**ID3D12MetaCommand**](/windows/win32/api/d3d12/nn-d3d12-id3d12metacommand) | Rappresenta un meta comando. Un meta comando è un oggetto Direct3D 12 che rappresenta un algoritmo accelerato da fornitori di hardware indipendenti (IHV). Si tratta di un riferimento opaco a un generatore di comandi implementato dal driver. |
| [**ID3D12Object**](/windows/win32/api/d3d12/nn-d3d12-id3d12object) | Interfaccia da cui [**ereditano ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) e [**ID3D12DeviceChild.**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) Fornisce metodi per associare dati privati e annotare i nomi degli oggetti. |
| [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable) | Interfaccia da cui ereditano molte altre interfacce di base. Indica che il tipo di oggetto incapsula una quantità di memoria accessibile dalla GPU; ma non indica se l'applicazione può modificare la residenza dell'oggetto.  |
| [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) | Gestisce una libreria di pipeline, in particolare il caricamento e il recupero di singoli pso. |
| [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1) | Gestisce una libreria di pipeline. Questa interfaccia estende [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) per caricare oggetti Criteri di gruppo da una descrizione del flusso di stato della pipeline. |
| [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) | Rappresenta lo stato di tutti gli shader attualmente impostati, nonché di alcuni oggetti di stato della funzione fissa. |
| [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) | Gestisce un heap di query. Un heap di query contiene una matrice di query, a cui fanno riferimento gli indici. |
| [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) | Incapsula una capacità generalizzata della CPU e della GPU di leggere e scrivere nella memoria fisica o negli heap. Contiene astrazioni per organizzare e modificare matrici di dati semplici, nonché dati multidimensionali ottimizzati per il campionamento di shader. |
| [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) | La firma radice definisce le risorse associate alla pipeline grafica. Una firma radice viene configurata dall'app e collega gli elenchi di comandi alle risorse richieste dagli shader. Attualmente sono disponibili una grafica e una firma radice di calcolo per ogni app. |
| [**ID3D12RootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) | Contiene un metodo per restituire la struttura di dati [**D3D12-ROOT-SIGNATURE-DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) deserializzata di una firma radice serializzata versione 1.0.  |
| [**ID3D12SDKConfiguration**](/windows/win32/api/d3d12/nn-d3d12-id3d12sdkconfiguration) | Fornisce metodi di configurazione dell'SDK. |
| [**ID3D12ShaderCacheSession**](/windows/win32/api/d3d12/nn-d3d12-id3d12shadercachesession) | Rappresenta una sessione della cache shader. |
| [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject) | Rappresenta una quantità variabile di stato di configurazione, inclusi gli shader, che un'applicazione gestisce come singola unità e che viene assegnato atomicamente a un driver per l'elaborazione, ad esempio la compilazione o l'ottimizzazione.  |
| [**ID3D12StateObjectProperties**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobjectproperties) | Fornisce metodi per ottenere e impostare le proprietà di un [**oggetto ID3D12StateObject.**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject)  |
| [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools) | Questa interfaccia viene usata per configurare il runtime per strumenti come PIX. Non è previsto o supportato per qualsiasi altro scenario. |
| [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) | Contiene metodi per restituire la struttura di dati [**D3D12-ROOT-SIGNATURE-DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) deserializzata di qualsiasi versione di una firma radice serializzata.  |

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni di riferimento di base](direct3d-12-core-reference.md)
* [Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
* [Gerarchia dell'interfaccia](interface-hierarchy.md)
