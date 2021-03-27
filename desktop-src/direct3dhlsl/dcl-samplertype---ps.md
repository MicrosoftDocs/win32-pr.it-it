---
title: dcl_samplerType (SM2, SM3-PS ASM)
description: Dichiarare un campionatore pixel shader.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 934931d6063ac264a2e6685104f8ed6fbdaaa64e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046121"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a>DCL \_ samplerType (SM2, SM3-PS ASM)

Dichiarare un campionatore pixel shader.

## <a name="syntax"></a>Sintassi



|                      |
|----------------------|
| samplerType di DCL \_\# |



 

dove:

-   \_samplerType definisce il tipo di dati del campionatore. Determina il numero di coordinate necessarie per ogni coordinata di trama durante il campionamento. Sono definite le dimensioni delle coordinate di trama seguenti.
    -   \_2D
    -   \_cubo
    -   \_volume
-   s \# identifica un campionatore dove s è un'abbreviazione del campionatore e \# è il numero di campionatore. I sampler sono pseudo-registri perché non è possibile leggerli o scriverli direttamente.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| \_samplerType DCL      |      |      |      |      | x    | x    | x     | x    | x     |



 

Tutte le \_ istruzioni samplerType di DCL devono essere visualizzate prima della prima istruzione eseguibile.

## <a name="example"></a>Esempio


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




