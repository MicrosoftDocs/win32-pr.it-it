---
title: Associazione di risorse
description: Binding è il processo di collegamento di oggetti risorsa agli shader della pipeline grafica.
ms.assetid: CB0065EF-4E53-4E16-9F7E-09A261C360FB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086a14beec32447cb91e2a345f4fecda8d5480fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548853"
---
# <a name="resource-binding"></a>Associazione di risorse

Binding è il processo di collegamento di oggetti risorsa agli shader della pipeline grafica.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Panoramica dell'associazione di risorse](resource-binding-flow-of-control.md) | La chiave per l'associazione di risorse in DirectX 12 è costituita dai concetti di un *descrittore*, *tabelle di descrittore*, *heap di descrittori* e una *firma radice*. |
| [Differenze nel modello di associazione da Direct3D 11](binding-model.md) | Una delle principali decisioni di progettazione alla base dell'associazione DirectX12 consiste nel separarla da altre attività di gestione. Questa operazione impone alcuni requisiti nell'app per gestire determinati rischi potenziali. |
| [Descrittori](descriptors.md) | I descrittori sono l'unità primaria di binding per una singola risorsa in D3D12. |
| [Heap descrittore](descriptor-heaps.md) | Un heap del descrittore è una raccolta di allocazioni contigue di descrittori, un'allocazione per ogni descrittore. |
| [Tabelle descrittore](descriptor-tables.md) | Una tabella descrittore è logicamente una matrice di descrittori. |
| [Firme radice](root-signatures.md) | La firma radice definisce i tipi di risorse associati alla pipeline grafica. |
| [Esecuzione di query sulle funzionalità](capability-querying.md) | L'applicazione può individuare il livello di supporto per l'associazione di risorse e molte altre funzionalità, con una chiamata a [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). |
| [Associazione di risorse in HLSL](resource-binding-in-hlsl.md) | In questo argomento vengono descritte alcune funzionalità specifiche dell'utilizzo del [modello shader](/windows/desktop/direct3dhlsl/shader-model-5-1) HLSL (High Level Shader Language) 5,1 con Direct3D 12. Tutti i componenti hardware Direct3D 12 supportano il modello di shader 5,1, pertanto il supporto per questo modello non dipende dal livello di funzionalità hardware. |
| [Ottimizzazioni di UMA: trame accessibili per la CPU e swizzle standard](default-texture-mapping.md) | Le GPU di Universal Memory Architecture (UMA) offrono alcuni vantaggi di efficienza rispetto alle GPU discrete, soprattutto durante l'ottimizzazione per i dispositivi mobili. Fornire l'accesso alla CPU delle risorse quando la GPU è UMA può ridurre la quantità di copia eseguita tra CPU e GPU. Sebbene non sia consigliabile consigliare le applicazioni in modo cieco per garantire l'accesso alla CPU a tutte le risorse sulle progettazioni UMA, è possibile migliorare l'efficienza assegnando l'accesso alla CPU alle risorse appropriate. Diversamente dalle GPU discrete, la CPU può avere tecnicamente un puntatore a tutte le risorse a cui la GPU può accedere. |
| [Caricamenti Unordered Access View tipizzati](typed-unordered-access-view-loads.md) | Il caricamento tipizzato Unordered Access View (UAV) è la possibilità per uno shader di leggere da un UAV con un [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)specifico. |
| [Risorse affiancate al volume](volume-tiled-resources.md) | Le trame volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione dei riquadri è tridimensionale. |
| [Sottorisorse](subresources.md) | Viene descritto come una risorsa è divisa in sottorisorse e viene illustrato come fare riferimento a una singola, più o più sezioni di sottorisorse. |

## <a name="related-topics"></a>Argomenti correlati

* [Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
* [Esercitazioni video su DirectX Advanced Learning: associazione di risorse in DirectX 12](https://www.youtube.com/watch?v=Uwhhdktaofg)
* [Gestione della memoria](memory-management.md)