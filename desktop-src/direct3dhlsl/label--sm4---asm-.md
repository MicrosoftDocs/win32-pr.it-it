---
title: label (sm4 - asm)
description: Indica l'inizio di una subroutine.
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9075aa14d72893d7c7862361b44ff636dd9bb6fda62563087ca2404bd1d70b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986461"
---
# <a name="label-sm4---asm"></a>label (sm4 - asm)

Indica l'inizio di una subroutine.



| etichetta l\# |
|-----------|



 



| Elemento                                                       | Descrizione                         |
|------------------------------------------------------------|-------------------------------------|
| <span id="l_"></span><span id="L_"></span>*L\#*<br/> | \[in \] Numero dell'etichetta.<br/> |



 

## <a name="remarks"></a>Commenti

**Un'etichetta** può essere visualizzata solo dopo un'istruzione [**ret**](ret--sm4---asm-.md) che non è annidata in alcuna istruzione di controllo di flusso.

Il codice prima della prima **etichetta** in un programma è il programma principale. Tutte le subroutine vengono visualizzate alla fine del programma, indicate dalle **istruzioni label.**

Nell'esempio seguente viene illustrato come utilizzare questa istruzione.

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                    if_nz r0.x
                        ret
                    endif
                    ...
                ret
```

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





