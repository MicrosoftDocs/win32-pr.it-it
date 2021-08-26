---
title: Registro float costante (informazioni di riferimento su HLSL PS)
description: Registro di input pixel shader per una costante a virgola mobile 4D.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 025c7e7609e7e0d19c15dfa24e27b9f174114e9287a9e09d01d2436b4ef2ef8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982851"
---
# <a name="constant-float-register-hlsl-ps-reference"></a>Registro float costante (informazioni di riferimento su HLSL PS)

Registro di input pixel shader per una costante a virgola mobile 4D.

Possono essere impostate usando [def - ps](def---ps.md) o [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).

Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.

-   Per Direct3D 9, le costanti impostate con defx assegnano valori allo spazio costante dello shader. La durata di una costante dichiarata con defx è limitata solo all'esecuzione dello shader. Al contrario, le costanti impostate usando le API SetXXXShaderConstantX inizializzano le costanti nello spazio globale. Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) fino a quando non viene chiamato SetxxxShaderConstants.
-   Per Direct3D 8, le costanti impostate con defx o le API assegnano entrambi valori allo spazio costante dello shader. Ogni volta che lo shader viene eseguito, le costanti vengono usate dallo shader corrente indipendentemente dalla tecnica usata per impostarle.

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio che dichiara due costanti a virgola mobile all'interno di uno shader.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Queste costanti vengono caricate ogni volta che [**viene chiamato SetPixelShader.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)

Se si impostano valori costanti con l'API, non è necessaria alcuna dichiarazione shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 