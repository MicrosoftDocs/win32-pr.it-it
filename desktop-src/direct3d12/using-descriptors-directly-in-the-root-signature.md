---
title: Uso dei descrittori direttamente nella firma radice
description: Per evitare la necessità di passare attraverso un heap descrittore, è possibile inserire un descrittore direttamente nella firma radice.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9d459f3195a4cf722ea210edbe63e5c1bf3cc8
ms.sourcegitcommit: 170bc12e9724d00cecbb96d57c7226c51e135dee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113489172"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>Uso dei descrittori direttamente nella firma radice

Per evitare la necessità di passare attraverso un heap descrittore, è possibile inserire un descrittore direttamente nella firma radice. Questi descrittori utilizzano una grande quantità di spazio nella firma radice (vedere Limiti della firma [radice),](/windows/win32/direct3d12/root-signature-limits)quindi è consigliabile usarli con moderamento.

Un esempio di utilizzo potrebbe essere quello di inserire nel layout radice una visualizzazione buffer costante (CBV) che cambia per ogni disegno. In questo modo lo spazio dell'heap dei descrittori non deve essere allocato dall'applicazione per ogni disegno e salva che punta a una tabella di descrittori nella nuova posizione nell'heap dei descrittori. Inserendo un elemento nella firma radice, l'applicazione si limita a consegnare la responsabilità del controllo delle versioni al driver. ma questa è l'infrastruttura già presente nei driver.

Per il rendering che usa un numero estremamente contenuto di risorse, l'uso di tabelle/heap dei descrittori potrebbe non essere necessario se tutti i descrittori necessari possono essere inseriti direttamente nella firma radice.

Questi sono gli unici tipi di descrittori supportati nella firma radice.

- Visualizzazione buffer costante (CBV).
- Visualizzazioni di risorse shader/viste di accesso non ordinato (UAV) di risorse buffer in cui la conversione del formato non è necessaria (buffer non tipici). Alcuni esempi di buffer non tipici che possono essere associati a descrittori radice includono `StructuredBuffer<type>` `RWStructuredBuffer<type>` , e `ByteAddressBuffer` `RWByteAddressBuffer` . I buffer tipici, ad `Buffer<uint>` esempio e , non `Buffer<float2>` possono.
- SRV di strutture di accelerazione raytracing, in firme radice locali o globali. 

A un UAV nella radice non possono essere associati contatori. I descrittori nella firma radice vengono visualizzati come singoli descrittori separati che &mdash; non possono essere indicizzati dinamicamente.

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

Nell'esempio precedente non può essere dichiarato come matrice, come in se ne verrà eseguito il mapping a un `mySceneData` `cbuffer mySceneData[2]` descrittore nella firma radice. Ciò è dovuto al fatto che l'indicizzazione tra descrittori non è supportata nella firma radice. Se si desidera, è possibile definire singoli buffer costanti separati e definirli ognuno come voce separata nella firma radice. Si noti che `mySceneData` all'interno di è presente una matrice `bar[2]` . L'indicizzazione dinamica all'interno del buffer costante è valida. Un descrittore nella firma radice si comporta esattamente come lo stesso descrittore se vi si accedesse tramite un &mdash; heap descrittore. Questo comportamento è in contrasto con le costanti di inlining direttamente nella firma radice, che appare anche come un buffer costante, ad eccezione del vincolo che l'indicizzazione dinamica all'interno delle costanti inline non è consentita, quindi non sarebbe consentita in tale `bar[2]` posizione.

Queste API (dall'interfaccia [**ID3D12GraphicsCommandList)**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) sono per l'impostazione dei descrittori direttamente nella firma radice.

-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetGraphicsRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetGraphicsRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetGraphicsRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!NOTE]  
> Non esiste alcun concetto di matrice di *descrittori radice* in Direct3D 12. Le matrici di descrittori sono supportate solo negli heap dei descrittori.

## <a name="related-topics"></a>Argomenti correlati

* [Firme radice](root-signatures.md)
