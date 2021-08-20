---
title: Oggetti modello shader 5.1
description: Gli oggetti seguenti sono stati aggiunti al modello shader 5.1.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f253c9d6a82e5a464e55761625ba8f88dd7953e3f293fc142a69019a3889830
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671632"
---
# <a name="shader-model-51-objects"></a>Oggetti modello shader 5.1

Gli oggetti seguenti sono stati aggiunti al modello shader 5.1.

Per le viste [ordine rasterizzatore](/windows/desktop/direct3d11/rasterizer-order-views) (disponibili in D3D11.3 e D3D12), gli oggetti seguenti sono nuovi e sono consentiti solo nel pixel shader. Si noti che i metodi supportati sono identici agli oggetti UAV corrispondenti.



| Oggetto rasterizzatore                                   | Oggetto UAV                                                              |
|------------------------------------|---------------------------------------------------------------|
| RasterizerOrderedBuffer            | [**RWBuffer**](sm5-object-rwbuffer.md)                       |
| RasterizerOrderedByteAddressBuffer | [**RWByteAddressBuffer**](sm5-object-rwbyteaddressbuffer.md) |
| RasterizerOrderedStructuredBuffer  | [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md)   |
| RasterizerOrderedTexture1D         | [**RWTexture1D**](sm5-object-rwtexture1d.md)                 |
| RasterizerOrderedTexture1DArray    | [**RWTexture1DArray**](sm5-object-rwtexture1darray.md)       |
| RasterizerOrderedTexture2D         | [**RWTexture2D**](sm5-object-rwtexture2d.md)                 |
| RasterizerOrderedTexture2DArray    | [**RWTexture2DArray**](sm5-object-rwtexture2darray.md)       |
| RasterizerOrderedTexture3D         | [**RWTexture3D**](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 5.1](shader-model-5-1.md)
</dt> <dt>

[Funzionalità di HLSL Shader Model 5.1 per Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 
