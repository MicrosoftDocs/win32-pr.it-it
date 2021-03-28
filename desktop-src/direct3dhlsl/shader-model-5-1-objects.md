---
title: Oggetti modello shader 5,1
description: Al modello di shader 5,1 sono stati aggiunti gli oggetti seguenti.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616afd8e4036988b6f91cb09cddf0db26c1dd480
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338062"
---
# <a name="shader-model-51-objects"></a>Oggetti modello shader 5,1

Al modello di shader 5,1 sono stati aggiunti gli oggetti seguenti.

Per le [visualizzazioni degli ordini di rasterizzazione](/windows/desktop/direct3d11/rasterizer-order-views) (disponibili in D3D 11.3 e D3D12), gli oggetti seguenti sono nuovi e sono consentiti solo nella pixel shader. Si noti che i metodi supportati sono identici agli oggetti UAV corrispondenti.



|                                    |                                                               |
|------------------------------------|---------------------------------------------------------------|
| Oggetto rasterizzatore                  | UAV (oggetto)                                                    |
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

[Modello Shader 5,1](shader-model-5-1.md)
</dt> <dt>

[Funzionalità del modello HLSL shader 5,1 per Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 