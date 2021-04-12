---
description: Una funzione Effect viene scritta in HLSL ed è dichiarata con la sintassi seguente.
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: Sintassi della funzione Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483197"
---
# <a name="effect-function-syntax-direct3d-10"></a>Sintassi della funzione Effect (Direct3D 10)

Una funzione Effect viene scritta in HLSL ed è dichiarata con la sintassi seguente.

## <a name="syntax"></a>Sintassi

*ReturnType* *FunctionName* ( \[ *argomento* \] )

{

<dl> \[ *Istruzioni* \]
</dl>

};



| Nome         | Descrizione                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | Qualsiasi [tipo di HLSL](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)                                                                                                                                                                                                       |
| FunctionName | Stringa ASCII che identifica in modo univoco il nome della funzione shader.                                                                                                                                                                                            |
| ArgumentList | Uno o più argomenti separati da virgole (vedere [argomenti della funzione (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).                                                                                                                             |
| Istruzioni   | Una o più istruzioni (vedere le [istruzioni (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) che costituiscono il corpo della funzione. Se una funzione viene definita senza un corpo, viene considerato un prototipo; e devono essere ridefiniti con un corpo prima dell'uso. |



 

Una funzione Effect può essere uno shader oppure può essere semplicemente una funzione chiamata da uno shader. Una funzione viene identificata in modo univoco in base al nome, ai tipi dei relativi parametri e alla piattaforma di destinazione. è pertanto possibile eseguire l'overload delle funzioni. Qualsiasi funzione HLSL valida deve adattarsi a questo formato; per un elenco più dettagliato della sintassi per le funzioni HLSL, vedere [funzioni (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).

## <a name="example"></a>Esempio

L' [esempio BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) USA sia un pixel shader che un vertex shader. La funzione pixel shader è denominata RenderScenePS ed è illustrata di seguito.


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

 

 
