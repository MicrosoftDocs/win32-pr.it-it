---
title: def - vs
description: Definisce le costanti vertex shader.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e5e3d5cbeb4d60f7beffd70c30ba0775863a9782cfb365a4d40bdf5552a186f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855351"
---
# <a name="def---vs"></a>def - vs

Definisce le costanti vertex shader.

## <a name="syntax"></a>Sintassi



| def dst, float1, float2, float3, float4 |
|-----------------------------------------|



 

dove

-   dst è il registro di destinazione.
-   float1, float2, float3, float4 sono quattro numeri a virgola mobile.

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| def                    | x    | x    | x    | x     | x    | x     |



 

L'istruzione def definisce una costante shader il cui valore viene caricato ogni volta che uno shader viene impostato su un dispositivo. Queste sono chiamate costanti immediate. Le costanti immediate hanno la precedenza sulle costanti impostate dai metodi API SetVertexShaderConstantF.

Esistono due modi per impostare una costante in uno shader.

1.  Usare def - vs per definire la costante direttamente all'interno di uno shader.

    def: vs può definire solo costanti a virgola mobile.

2.  Usare i metodi API per impostare una costante.
    -   Usare [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) per impostare una costante a virgola mobile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[defi - vs](defi---vs.md)
</dt> <dt>

[defb - vs](defb---vs.md)
</dt> </dl>

 

 