---
title: Sintassi della funzione Effect (Direct3D 11)
description: Una funzione Effect viene scritta in HLSL ed è dichiarata con la sintassi descritta in questa sezione.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f569211d5f178b96cf7415478010285e7a836b58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727378"
---
# <a name="effect-function-syntax-direct3d-11"></a>Sintassi della funzione Effect (Direct3D 11)

Una funzione Effect viene scritta in HLSL ed è dichiarata con la sintassi descritta in questa sezione.

## <a name="syntax"></a>Sintassi

*ReturnType* *FunctionName* ( \[ *argomento* \] )

{

<dl> \[ *Istruzioni* \]
</dl>

};



| Nome         | Descrizione                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | Qualsiasi [tipo di HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)                                                                                                                                                                                                       |
| FunctionName | Stringa ASCII che identifica in modo univoco il nome della funzione shader.                                                                                                                                                                                            |
| ArgumentList | Uno o più argomenti separati da virgole (vedere [argomenti della funzione (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).                                                                                                                             |
| Istruzioni   | Una o più istruzioni (vedere le [istruzioni (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) che costituiscono il corpo della funzione. Se una funzione viene definita senza un corpo, viene considerato un prototipo; e devono essere ridefiniti con un corpo prima dell'uso. |



 

Una funzione Effect può essere uno shader oppure può essere semplicemente una funzione chiamata da uno shader. Una funzione viene identificata in modo univoco in base al nome, ai tipi dei relativi parametri e alla piattaforma di destinazione. è pertanto possibile eseguire l'overload delle funzioni. Qualsiasi funzione HLSL valida deve adattarsi a questo formato; per un elenco più dettagliato della sintassi per le funzioni HLSL, vedere [funzioni (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).

## <a name="example"></a>Esempio

Di seguito è riportato un esempio di una funzione pixel shader.


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

[Formato effetto](d3d11-effect-format.md)
</dt> </dl>

 

 