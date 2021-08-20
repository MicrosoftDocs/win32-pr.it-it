---
title: Registro booleano costante (informazioni di riferimento su HLSL PS)
description: Questo registro è una raccolta di bit usati nelle istruzioni di controllo di flusso statiche (ad esempio, se bool - ps - else - ps - endif - ps).
ms.assetid: fb4abe19-d0cf-48ac-866e-4be60cc86bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e86a447d9c0a8ec2d57d2cc7a3f2b7e25714d0d29f2c09add72ab17780b8d8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090394"
---
# <a name="constant-boolean-register-hlsl-ps-reference"></a>Registro booleano costante (informazioni di riferimento su HLSL PS)

Questo registro è una raccolta di bit usati nelle istruzioni di controllo del flusso statico (ad esempio, [se bool - ps](if-bool---ps.md)else -  -  [ps](else---ps.md)  -  [endif - ps](endif---ps.md)). Ne esistono 16, pertanto uno shader può avere 16 condizioni di ramo indipendenti. Possono essere impostati usando [defb - ps](defb---ps.md) o [**SetPixelShaderConstantB.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)

Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.

-   Per Direct3D 9, le costanti impostate con defx assegnano valori allo spazio costante dello shader. La durata di una costante dichiarata con defx è limitata solo all'esecuzione di tale shader. Al contrario, le costanti impostate usando le API SetXXXShaderConstantX inizializzano le costanti nello spazio globale. Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) fino a quando non viene chiamato SetxxxShaderConstants.
-   Per Direct3D 8, le costanti impostate con defx o le API assegnano entrambi valori allo spazio costante dello shader. Ogni volta che viene eseguito lo shader, le costanti vengono usate dallo shader corrente indipendentemente dalla tecnica usata per impostarli.



| Versioni pixel shader     | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| Registro booleano costante |      |      |      |      |      |       | x    | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 