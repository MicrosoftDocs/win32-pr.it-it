---
title: Uso dei descrittori direttamente nella firma radice
description: Le applicazioni possono inserire descrittori direttamente nella firma radice per evitare di dover passare attraverso un heap del descrittore.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd97a7d68f5c9b51b6d15d3b71c6e30d04bb36e5
ms.sourcegitcommit: 83afb2f3e9e5d37f3f5a11e975515e9ed8b044ff
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "104548886"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>Uso dei descrittori direttamente nella firma radice

Le applicazioni possono inserire descrittori direttamente nella firma radice per evitare di dover passare attraverso un heap del descrittore. Questi descrittori hanno una grande quantità di spazio nella firma radice (vedere la sezione limiti della firma radice), per cui le applicazioni devono utilizzarle sporadicamente.

Un esempio di utilizzo è quello di inserire una visualizzazione del buffer costante (CBV) che sta cambiando per disegno nel layout radice in modo che lo spazio dell'heap di descrittore non debba essere allocato dall'applicazione per ogni disegno (e salvare puntando una tabella di descrittori nella nuova posizione nell'heap del descrittore). Inserendo qualcosa nella firma radice, l'applicazione passa semplicemente la responsabilità del controllo delle versioni al driver, ma si tratta di un'infrastruttura già disponibile.

Per il rendering che utilizza un numero molto ridotto di risorse, l'utilizzo della tabella o dell'heap del descrittore potrebbe non essere necessario se tutti i descrittori necessari possono essere inseriti direttamente nella firma radice.

Gli unici tipi di descrittori supportati nella firma radice sono:
- CBVs.
- Viste delle risorse shader (SRVs)/unordered Access views (UAV) delle risorse del buffer in cui il formato SRV/UAV contiene solo componenti FLOAT/UINT/SINT di 32 bit (non è prevista alcuna conversione del formato).
- SRVs delle strutture di accelerazione raytracing, in firme radice locali o globali. 

UAV nella radice non possono avere contatori associati. I descrittori nella firma radice vengono visualizzati come singoli descrittori separati &mdash; che non possono essere indicizzati dinamicamente.

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

Nell'esempio precedente non `mySceneData` può essere dichiarato come una matrice, come in `cbuffer mySceneData[2]` se verrà eseguito il mapping a un descrittore nella firma radice, poiché l'indicizzazione tra i descrittori non è supportata nella firma radice. L'applicazione può definire singoli buffer costanti distinti e definirli ciascuno come voce distinta nella firma radice, se lo si desidera. Si noti che in `mySceneData` precedenza è presente una matrice `bar[2]` . L'indicizzazione dinamica all'interno del buffer costante è valida: un descrittore nella firma radice si comporta esattamente come lo stesso descrittore si comporterebbe in caso di accesso tramite un heap dei descrittori. Si tratta di un contrasto con le costanti di incorporamento direttamente nella firma radice, che appare anche come un buffer costante, tranne nel caso in cui non sia consentito l'indicizzazione dinamica all'interno delle costanti inline. non è quindi `bar[2]` consentito.

Le API seguenti (dall'interfaccia [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) sono per impostare i descrittori direttamente nella firma radice:

-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetGraphicsRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetGraphicsRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetGraphicsRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!Note]  
> In Direct3D 12 non esiste alcun concetto di "matrice descrittore radice". Le matrici di descrittori sono supportate solo negli heap del descrittore.

## <a name="related-topics"></a>Argomenti correlati

[Firme radice](root-signatures.md)
