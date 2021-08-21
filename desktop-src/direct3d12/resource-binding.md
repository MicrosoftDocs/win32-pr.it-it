---
title: Associazione di risorse
description: Il binding è il processo di collegamento di oggetti risorsa agli shader della pipeline grafica.
ms.assetid: CB0065EF-4E53-4E16-9F7E-09A261C360FB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93ca7fb75e65c58aee2b2dffbb220830e2911f2c8d7ce9186a09926fa11373f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912245"
---
# <a name="resource-binding"></a>Associazione di risorse

Il binding è il processo di collegamento di oggetti risorsa agli shader della pipeline grafica.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Panoramica dell'associazione di risorse](resource-binding-flow-of-control.md) | La chiave per l'associazione di risorse in DirectX 12 sono i concetti di un descrittore, le tabelle dei descrittori, gli heap *dei* descrittori e una firma *radice.* |
| [Differenze nel modello di binding rispetto a Direct3D 11](binding-model.md) | Una delle principali decisioni di progettazione alla base dell'associazione DirectX12 è separarla da altre attività di gestione. In questo modo vengono richiesti alcuni requisiti all'app per gestire determinati rischi potenziali. |
| [Descrittori](descriptors.md) | I descrittori sono l'unità principale di binding per una singola risorsa in D3D12. |
| [Heap dei descrittori](descriptor-heaps.md) | Un heap dei descrittori è una raccolta di allocazioni contigue di descrittori, un'allocazione per ogni descrittore. |
| [Tabelle dei descrittori](descriptor-tables.md) | Una tabella di descrittori è logicamente una matrice di descrittori. |
| [Firme radice](root-signatures.md) | La firma radice definisce i tipi di risorse associati alla pipeline grafica. |
| [Esecuzione di query sulla funzionalità](capability-querying.md) | L'applicazione può individuare il livello di supporto per l'associazione di risorse e molte altre funzionalità, con una chiamata a [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). |
| [Associazione di risorse in HLSL](resource-binding-in-hlsl.md) | Questo argomento descrive alcune funzionalità specifiche dell'uso del modello di shader HLSL (High Level Shader [Language) 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) con Direct3D 12. Tutto l'hardware Direct3D 12 supporta il modello shader 5.1, quindi il supporto per questo modello non dipende dal livello di funzionalità hardware. |
| [Ottimizzazioni UMA: trame accessibili dalla CPU e swizzle standard](default-texture-mapping.md) | Le GPU UMA (Universal Memory Architecture) offrono alcuni vantaggi in termini di efficienza rispetto alle GPU discrete, soprattutto per l'ottimizzazione per i dispositivi mobili. Concedere alle risorse l'accesso alla CPU quando la GPU è UMA può ridurre la quantità di copia che si verifica tra CPU e GPU. Anche se non è consigliabile che le applicazioni consegneranno alla CPU l'accesso alla CPU a tutte le risorse nelle progettazioni UMA, è possibile migliorare l'efficienza assegnando alle risorse l'accesso alla CPU giusto. A differenza delle GPU discrete, la CPU può tecnicamente avere un puntatore a tutte le risorse a cui la GPU può accedere. |
| [Caricamenti Unordered Access View tipi](typed-unordered-access-view-loads.md) | Unordered Access View (UAV) Typed Load (UAV) è la possibilità per uno shader di leggere da un UAV con un formato [**DXGI \_ specifico.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) |
| [Risorse affiancate del volume](volume-tiled-resources.md) | Le trame di volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione dei riquadri è tridimensionale. |
| [Sottorisorse](subresources.md) | Viene descritto come una risorsa viene divisa in sottorisorse e come fare riferimento a una singola, più o sezione di sottorisorse. |

## <a name="related-topics"></a>Argomenti correlati

* [Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
* [Esercitazioni video sull'apprendimento avanzato di DirectX: Associazione di risorse in DirectX 12](https://www.youtube.com/watch?v=Uwhhdktaofg)
* [Gestione della memoria](memory-management.md)