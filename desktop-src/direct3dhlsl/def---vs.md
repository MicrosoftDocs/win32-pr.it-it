---
title: def-vs
description: Definisce le costanti del vertex shader.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b5a55cb13eb7197986349c602ec35855a3f6364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104224015"
---
# <a name="def---vs"></a>def-vs

Definisce le costanti del vertex shader.

## <a name="syntax"></a>Sintassi



| def DST, float1, float2, float3, float4 |
|-----------------------------------------|



 

dove

-   DST è il registro di destinazione.
-   float1, float2, float3, float4 sono quattro numeri a virgola mobile.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| def                    | x    | x    | x    | x     | x    | x     |



 

L'istruzione def definisce una costante dello shader il cui valore viene caricato ogni volta che uno shader è impostato su un dispositivo. Sono denominate costanti immediate. Le costanti immediate hanno la precedenza sulle costanti impostate dai metodi API SetVertexShaderConstantF.

Esistono due modi per impostare una costante in uno shader.

1.  Usare def-vs per definire la costante direttamente all'interno di uno shader.

    def-vs può definire solo costanti a virgola mobile.

2.  Usare i metodi API per impostare una costante.
    -   Usare [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) per impostare una costante a virgola mobile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[defi-vs](defi---vs.md)
</dt> <dt>

[defb-vs](defb---vs.md)
</dt> </dl>

 

 