---
description: Una funzione effect viene scritta in HLSL ed è dichiarata con la sintassi seguente.
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: Sintassi della funzione Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b30e964e18ebbc2b5607ed83c11fa10ba2bdaa76862a7efb7ab78cd87c6478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914557"
---
# <a name="effect-function-syntax-direct3d-10"></a>Sintassi della funzione Effect (Direct3D 10)

Una funzione effect viene scritta in HLSL ed è dichiarata con la sintassi seguente.

## <a name="syntax"></a>Sintassi

*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )

{

<dl> \[ *Istruzioni* \]
</dl>

};



| Nome         | Descrizione                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | Qualsiasi [tipo HLSL](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)                                                                                                                                                                                                       |
| FunctionName | Stringa ASCII che identifica in modo univoco il nome della funzione shader.                                                                                                                                                                                            |
| ArgumentList | Uno o più argomenti, separati da virgole (vedere [Argomenti di funzione (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).                                                                                                                             |
| Istruzioni   | Una o più istruzioni (vedere [Istruzioni (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)che costituiscono il corpo della funzione. Se una funzione viene definita senza un corpo, viene considerata un prototipo. e devono essere ridefiniti con un corpo prima dell'uso. |



 

Una funzione di effetto può essere uno shader o semplicemente una funzione chiamata da uno shader. Una funzione viene identificata in modo univoco in base al nome, ai tipi dei relativi parametri e alla piattaforma di destinazione. Pertanto, è possibile eseguire l'overload delle funzioni. Qualsiasi funzione HLSL valida deve essere adatta a questo formato. Per un elenco più dettagliato della sintassi per le funzioni HLSL, vedere [Funzioni (DirectX HLSL).](../direct3dhlsl/dx-graphics-hlsl-functions.md)

## <a name="example"></a>Esempio

[L'esempio BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa sia un pixel shader che un vertex shader. La pixel shader chiamata RenderScenePS ed è illustrata di seguito.


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](d3d10-effect-format.md)
</dt> </dl>

 

 
