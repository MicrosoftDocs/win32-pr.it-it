---
description: Una variabile Effect viene dichiarata con la sintassi seguente.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Sintassi della variabile Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8068571ff393e83ba0ae11eb2f9cb62f0bbb49df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401449"
---
# <a name="effect-variable-syntax-direct3d-10"></a>Sintassi della variabile Effect (Direct3D 10)

Una variabile Effect viene dichiarata con la sintassi seguente.

## <a name="syntax"></a>Sintassi

*DataType* *variablename* \[ : *semanticname* \]  <  *annotazioni* >;



| Nome         | Descrizione                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Qualsiasi tipo di [trama](../direct3dhlsl/dx-graphics-hlsl-to-type.md) o di [base](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) .                                                                        |
| VariableName | Stringa ASCII che identifica in modo univoco il nome della variabile di effetto.                                                                                                                   |
| Semanticname | Stringa ASCII che indica informazioni aggiuntive sulla modalità di utilizzo di una variabile. Una semantica è una stringa ASCII che può essere un valore di sistema predefinito o una stringa utente personalizzata. |
| annotazioni  | Una o più parti di informazioni (metadati) fornite dall'utente ignorate dal sistema di effetti. Per la sintassi, vedere [sintassi delle annotazioni (Direct3D 10)](d3d10-effect-annotation-syntax.md).     |



 

Una variabile di effetto dichiarata al di fuori di tutte le funzioni è considerata globale nell'ambito. le variabili dichiarate all'interno di una funzione sono locali a tale funzione.

## <a name="example"></a>Esempio

L' [esempio BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa variabili globali senza semantica per colori materiali, proprietà chiare e matrici di trasformazione.

Questo esempio illustra le variabili di effetto globale.


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



Questo esempio illustra le variabili di effetto locali a una funzione shader.


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



In questo esempio vengono illustrati i parametri della funzione con semantica.


```
VS_OUTPUT RenderSceneVS( float4 vPos : SV_POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
  ...
}
```



In questo esempio viene illustrata la dichiarazione di una variabile di trama.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



Campionamento di una trama viene eseguita con un campionatore di trame. Per configurare un campionatore in un effetto, vedere il [tipo di campionatore](../direct3dhlsl/dx-graphics-hlsl-sampler.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](d3d10-effect-format.md)
</dt> </dl>

 

 
