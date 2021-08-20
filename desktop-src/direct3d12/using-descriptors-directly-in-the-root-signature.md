---
title: Uso dei descrittori direttamente nella firma radice
description: Per evitare la necessità di passare attraverso un heap descrittore, è possibile inserire un descrittore direttamente nella firma radice.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3f32b423b017477e66ea3ae32eee509ec455d85
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813223"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>Uso dei descrittori direttamente nella firma radice

Per evitare la necessità di passare attraverso un heap descrittore, è possibile inserire un descrittore direttamente nella firma radice. Questi descrittori prendono molto spazio nella firma radice (vedere Limiti della firma [radice),](./root-signature-limits.md)quindi è consigliabile usarli con parsimonio.

Un esempio di utilizzo potrebbe essere quello di inserire nel layout radice una visualizzazione del buffer costante (CBV) che cambia per disegno. Ciò significa che lo spazio dell'heap del descrittore non deve essere allocato dall'applicazione per ogni disegno e salva che punta a una tabella descrittore nella nuova posizione nell'heap dei descrittori. Inserendo qualcosa nella firma radice, l'applicazione sta semplicemente consegnando la responsabilità del controllo delle versioni al driver; ma questa è l'infrastruttura già presente nei driver.

Per il rendering che usa pochissime risorse, l'uso di tabelle/heap dei descrittori potrebbe non essere necessario se tutti i descrittori necessari possono essere inseriti direttamente nella firma radice.

Questi sono gli unici tipi di descrittori supportati nella firma radice.

- Visualizzazione del buffer costante (CBV).
- Viste di risorse shader /viste di accesso non ordinato (UAV) delle risorse del buffer in cui la conversione del formato non è necessaria (buffer non tipici). Alcuni esempi di buffer non tipici che possono essere associati ai descrittori radice includono `StructuredBuffer<type>` `RWStructuredBuffer<type>` , e `ByteAddressBuffer` `RWByteAddressBuffer` . Buffer tipici, ad `Buffer<uint>` esempio e `Buffer<float2>` non possono.
- SRV delle strutture di accelerazione raytracing, nelle firme radice locali o globali. 

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

Nell'esempio precedente non può essere dichiarato come matrice, come in se ne verrà eseguito il mapping a un `mySceneData` `cbuffer mySceneData[2]` descrittore nella firma radice. Questo perché l'indicizzazione tra descrittori non è supportata nella firma radice. Se lo si desidera, è possibile definire singoli buffer costanti separati e definirli ognuno come voce separata nella firma radice. Si noti che `mySceneData` all'interno di è presente una matrice `bar[2]` . L'indicizzazione dinamica all'interno del buffer costante è valida, un descrittore nella firma radice si comporta esattamente come lo stesso descrittore si comporterebbe se vi si accedesse tramite un &mdash; heap dei descrittori. Questo comportamento è in contrasto con l'inlining delle costanti direttamente nella firma radice, che appare anche come un buffer costante, ad eccezione del vincolo che l'indicizzazione dinamica all'interno delle costanti inline non è consentita, quindi non sarebbe `bar[2]` consentita.

Queste API (dall'interfaccia [**ID3D12GraphicsCommandList)**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) sono per l'impostazione dei descrittori direttamente nella firma radice.

-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetGraphicsRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetGraphicsRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetGraphicsRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!NOTE]  
> Non esiste alcun concetto di matrice *di descrittori radice* in Direct3D 12. Le matrici di descrittori sono supportate solo negli heap dei descrittori.

## <a name="related-topics"></a>Argomenti correlati

* [Firme radice](root-signatures.md)