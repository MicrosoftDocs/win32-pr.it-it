---
title: Oggetti modello shader 5.1
description: Gli oggetti seguenti sono stati aggiunti al modello shader 5.1.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376ce272e789501e21f5866be37f56daf31bc829
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825718"
---
# <a name="shader-model-51-objects"></a>Oggetti modello shader 5.1

Gli oggetti seguenti sono stati aggiunti al modello shader 5.1.

Per le viste [ordine rasterizzatore](/windows/desktop/direct3d11/rasterizer-order-views) (disponibili in D3D11.3 e D3D12), gli oggetti seguenti sono nuovi e sono consentiti solo nella pixel shader. Si noti che i metodi supportati sono identici agli oggetti UAV corrispondenti.



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

 

 
