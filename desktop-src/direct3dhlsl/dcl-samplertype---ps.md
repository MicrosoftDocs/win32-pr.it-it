---
title: dcl_samplerType (sm2, sm3 - ps asm)
description: Dichiarare un pixel shader sampler.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 764c3b992cd248a8900c3762c7c9e68abd3bed973ca4f7d44b1705122984f321
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726741"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a>dcl \_ samplerType (sm2, sm3 - ps asm)

Dichiarare un pixel shader sampler.

## <a name="syntax"></a>Sintassi

dcl \_ samplerType s\#



 

dove:

-   \_samplerType definisce il tipo di dati sampler. In questo modo viene determinato il numero di coordinate richieste da ogni coordinata di trama durante il campionamento. Sono definite le dimensioni delle coordinate di trama seguenti.
    -   \_2d
    -   \_Cubo
    -   \_Volume
-   s \# identifica un campionatore, dove s è un'abbreviazione del campionatore e \# è il numero del campionatore. I campionatori sono pseudoregistri perché non è possibile leggerli o scriverli direttamente.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
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

 

 




