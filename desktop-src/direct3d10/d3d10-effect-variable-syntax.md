---
description: Una variabile effect viene dichiarata con la sintassi seguente.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Sintassi delle variabili effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2422ba2cebf18c72a14d621ef13a98700aefd2858169c6e96566b455ec21d2ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497711"
---
# <a name="effect-variable-syntax-direct3d-10"></a>Sintassi delle variabili effect (Direct3D 10)

Una variabile effect viene dichiarata con la sintassi seguente.

## <a name="syntax"></a>Sintassi

*DataType* *VariableName* \[ : *SemanticName* \]  <  *Annotations* >;



| Nome         | Descrizione                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Qualsiasi [tipo di](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) trama o [di](../direct3dhlsl/dx-graphics-hlsl-to-type.md) base.                                                                        |
| VariableName | Stringa ASCII che identifica in modo univoco il nome della variabile dell'effetto.                                                                                                                   |
| SemanticName | Stringa ASCII che indica informazioni aggiuntive sull'uso di una variabile. Una semantica è una stringa ASCII che può essere un valore di sistema predefinito o una stringa utente personalizzata. |
| Annotazioni  | Una o più informazioni fornite dall'utente (metadati) che vengono ignorate dal sistema di effetti. Per la sintassi, vedere Sintassi delle [annotazioni (Direct3D 10).](d3d10-effect-annotation-syntax.md)     |



 

Una variabile di effetto dichiarata all'esterno di tutte le funzioni è considerata globale nell'ambito. Le variabili dichiarate all'interno di una funzione sono locali per tale funzione.

## <a name="example"></a>Esempio

[L'esempio BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa variabili globali senza semantica per i colori dei materiali, le proprietà della luce e le matrici di trasformazione.

Questo esempio illustra le variabili di effetto globale.


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



Questo esempio illustra le variabili di effetto locali per una funzione shader.


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



Questo esempio illustra i parametri di funzione con semantica.


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



Questo esempio illustra la dichiarazione di una variabile di trama.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



Il campionamento di una trama viene eseguito con un campionatore di trame. Per configurare un campionatore in un effetto, vedere il [tipo di campionatore](../direct3dhlsl/dx-graphics-hlsl-sampler.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](d3d10-effect-format.md)
</dt> </dl>

 

 
