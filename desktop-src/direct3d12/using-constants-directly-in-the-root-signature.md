---
title: Uso di costanti direttamente nella firma radice
description: Le applicazioni possono definire costanti radice nella firma radice, ognuna come un set di valori a 32 bit. Vengono visualizzati in HLSL (High Level Shading Language) come buffer costante. Si noti che i buffer costanti per motivi cronologici vengono visualizzati come set di valori a 4x32 bit.
ms.assetid: F9A2640F-D1FA-481C-BDF1-B15372E3C512
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3cd3980bede72d6e2f4b163abe11b249970eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103504"
---
# <a name="using-constants-directly-in-the-root-signature"></a>Uso di costanti direttamente nella firma radice

Le applicazioni possono definire costanti radice nella firma radice, ognuna come un set di valori a 32 bit. Vengono visualizzati in HLSL (High Level Shading Language) come buffer costante. Si noti che i buffer costanti per motivi cronologici vengono visualizzati come set di valori a 4x32 bit.

Ogni set di costanti utente viene considerato come una matrice scalare di valori a 32 bit, indicizzabile dinamicamente e in sola lettura dallo shader. L'indicizzazione fuori limite di un determinato set di costanti radice produce risultati non definiti. In HLSL è possibile fornire le definizioni della struttura dei dati affinché le costanti utente forniscano i tipi. Se, ad esempio, la firma radice definisce un set di 4 costanti radice, HLSL può sovrapporsi la struttura seguente.

``` syntax
struct DrawConstants
{
    uint foo;
    float2 bar;
    int moo;
};
ConstantBuffer<DrawConstants> myDrawConstants : register(b1, space0);
```

Le matrici non sono consentite nei buffer costanti per i quali viene eseguito il mapping alle costanti radice perché l'indicizzazione dinamica nello spazio della firma radice non è supportata. Ad esempio, non è valido avere una voce nel buffer costante come `float myArray[2];` . Un buffer costante di cui è stato eseguito il mapping alle costanti radice non può essere una matrice; non è pertanto possibile eseguire il mapping `cbuffer myCBArray[2]` in costanti radice.

Le costanti possono essere impostate parzialmente. Se, ad esempio, la firma radice definisce valori a 4 32 bit in *RootTableBindSlot* 2, è possibile impostare qualsiasi subset delle quattro costanti alla volta, mentre le altre restano invariate. Questa operazione può essere utile nei bundle che ereditano lo stato della firma radice e possono essere modificati parzialmente.

Quando si impostano le costanti, prestare attenzione al layout del buffer costante previsto dallo shader. È possibile, ad esempio, che le costanti vengano riempite a `vec4` limiti. Per verificare il layout previsto, controllare le informazioni di Reflection dallo shader HLSL.

Le API seguenti (dall'interfaccia [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) si riportano nell'impostazione delle costanti direttamente nella firma radice:

-   [**SetGraphicsRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)
-   [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants)
-   [**SetComputeRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)

Vedere anche la struttura delle [**\_ \_ costanti radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Firme radice](root-signatures.md)
</dt> </dl>

 

 




