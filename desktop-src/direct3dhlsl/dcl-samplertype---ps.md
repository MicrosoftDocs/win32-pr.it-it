---
title: dcl_samplerType (sm2, sm3 - ps asm)
description: Dichiarare un pixel shader di esempio.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7a6da220e50b43ce990c090c61d1caf84afec653
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129668"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a>dcl \_ samplerType (sm2, sm3 - ps asm)

Dichiarare un pixel shader di esempio.

## <a name="syntax"></a>Sintassi

dcl \_ samplerType s\#



 

dove:

-   \_samplerType definisce il tipo di dati sampler. Questo determina il numero di coordinate richieste da ogni coordinata di trama durante il campionamento. Vengono definite le dimensioni delle coordinate di trama seguenti.
    -   \_2d
    -   \_Cubo
    -   \_Volume
-   s \# identifica un campionatore dove s è un'abbreviazione del campionatore e \# è il numero del campionatore. I campionatori sono pseudoregistri perché non è possibile leggerli o scrivervi direttamente.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dcl \_ samplerType      |      |      |      |      | x    | x    | x     | x    | x     |



 

Tutte le istruzioni dcl \_ samplerType devono essere visualizzate prima della prima istruzione eseguibile.

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

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




