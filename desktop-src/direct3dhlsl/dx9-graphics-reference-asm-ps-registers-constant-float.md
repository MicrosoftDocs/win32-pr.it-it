---
title: Registro float costante (riferimenti per HLSL PS)
description: Registro di input del pixel shader per una costante a virgola mobile 4D.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05bb382b745d172ea4b81f9920154e7c79a58c2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399461"
---
# <a name="constant-float-register-hlsl-ps-reference"></a>Registro float costante (riferimenti per HLSL PS)

Registro di input del pixel shader per una costante a virgola mobile 4D.

Possono essere impostate con [def-PS](def---ps.md) o [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).

Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.

-   Per Direct3D 9, le costanti impostate con DeFX assegnano valori allo spazio costante dello shader. Il ciclo di vita di una costante dichiarata con DeFX è limitato solo all'esecuzione di tale shader. Viceversa, le costanti impostate utilizzando le API SetXXXShaderConstantX inizializzano costanti nello spazio globale. Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) finché non viene chiamato SetxxxShaderConstants.
-   Per Direct3D 8, le costanti impostate con DeFX o le API assegnano entrambi valori allo spazio costante dello shader. Ogni volta che viene eseguito lo shader, le costanti vengono utilizzate dallo shader corrente indipendentemente dalla tecnica utilizzata per impostarle.

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio che dichiara due costanti a virgola mobile all'interno di uno shader.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Queste costanti vengono caricate ogni volta che viene chiamato [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) .

Se si impostano valori costanti con l'API, non è necessaria alcuna dichiarazione dello shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 