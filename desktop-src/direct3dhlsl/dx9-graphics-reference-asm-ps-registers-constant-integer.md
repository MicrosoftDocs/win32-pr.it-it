---
title: Registro di valori interi costanti (informazioni di riferimento su HLSL PS)
description: I registri di valori interi costanti vengono usati solo dal ciclo ps e rep - ps.
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce2d9ba19f97439da098563639bc8940cdae2f202a6f24cdd1940e25cfc14e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489382"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a>Registro di valori interi costanti (informazioni di riferimento su HLSL PS)

I registri di valori interi costanti vengono usati [solo dal ciclo ps](loop---ps.md) e rep - [ps](rep---ps.md).

Possono essere impostati usando [defi - ps](defi---ps.md) o [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).

Se usato come argomento per il [ciclo - istruzione ps:](loop---ps.md)

-   .x è il conteggio delle iterazioni. ([rep - ps](rep---ps.md) usa solo questo componente).
-   .y è il valore iniziale per il contatore del ciclo.
-   .z è il passaggio di incremento per il contatore del ciclo.



| Versioni pixel shader     | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| Registro di valori interi costanti |      |      |      |      |      |       | x    | x    | x     |



 

Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.

-   Per Direct3D 9, le costanti impostate con defx assegnano valori allo spazio costante dello shader. La durata di una costante dichiarata con defx è limitata all'esecuzione di tale shader. Al contrario, le costanti impostate usando le API SetXXXShaderConstantX inizializzano le costanti nello spazio globale. Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) fino a quando non viene chiamato SetxxxShaderConstants.
-   Per Direct3D 8, le costanti impostate con defx o le API assegnano entrambi valori allo spazio costante dello shader. Ogni volta che viene eseguito lo shader, le costanti vengono usate dallo shader corrente indipendentemente dalla tecnica usata per impostarli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 