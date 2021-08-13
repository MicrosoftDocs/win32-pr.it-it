---
title: Sintassi delle variabili degli effetti (Direct3D 11)
description: Una variabile di effetto viene dichiarata con la sintassi descritta in questa sezione.
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25057f3cd2535a0b48072616c3dd59393f90a24fe044c1cdad8acea677a541ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538394"
---
# <a name="effect-variable-syntax-direct3d-11"></a>Sintassi delle variabili degli effetti (Direct3D 11)

Una variabile di effetto viene dichiarata con la sintassi descritta in questa sezione.

## <a name="syntax"></a>Sintassi

Sintassi di base:

*DataType* *VariableName:* \[ *SemanticName* \]  <  *Annotations*  >  \[ = InitialValue \] ;

Per [la sintassi completa, vedere Sintassi delle variabili (DirectX HLSL).](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)



| Nome         | Descrizione                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Qualsiasi [tipo di](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)blocco [di](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type)stato, di base, di trama, di visualizzazione di accesso non ordinato, di shader o di stato.                            |
| VariableName | Stringa ASCII che identifica in modo univoco il nome della variabile dell'effetto.                                                                                                                   |
| SemanticName | Stringa ASCII che indica informazioni aggiuntive su come usare una variabile. Una semantica è una stringa ASCII che può essere un valore di sistema predefinito o una stringa utente personalizzata. |
| Annotazioni  | Una o più informazioni fornite dall'utente (metadati) che vengono ignorate dal sistema di effetti. Per la sintassi, vedere [Sintassi delle annotazioni (Direct3D 11).](d3d11-effect-annotation-syntax.md)     |
| InitialValue | Valore predefinito della variabile.                                                                                                                                                          |



 

Una variabile di effetto dichiarata all'esterno di tutte le funzioni è considerata globale nell'ambito; Le variabili dichiarate all'interno di una funzione sono locali per tale funzione.

## <a name="example"></a>Esempio

Questo esempio illustra le variabili numeriche degli effetti globali.


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



Questo esempio illustra la dichiarazione di una variabile di trama globale.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



Il campionamento di una trama viene eseguito con un campionatore di trama. Per configurare un campionatore in un effetto, vedere il tipo [di campionatore](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

In questo esempio viene illustrata la dichiarazione di variabili di visualizzazione di accesso non ordinate globali.


```
RWStructuredBuffer<uint> bc : register(u2) < string name="bc"; >;
RWBuffer<uint> bRW;
struct S
{
   uint key;
   uint value;
};
AppendStructuredBuffer<S> asb : register(u5);
RWByteAddressBuffer rwbab : register(u1);
RWStructuredBuffer<uint> rwsb : register(u3);
RWTexture1D<float> rwt1d : register(u1);
RWTexture1DArray<uint> rwt1da : register(u4);
RWTexture2D<uint> rwt2d : register(u2);
RWTexture2DArray<uint> rwt2da : register(u6);
RWTexture3D<uint> rwt3d : register(u7); 
 This example illustrates declaring global shader variables.
VertexShader pVS = CompileShader( vs_5_0, VS() );
HullShader pHS = NULL;
DomainShader pDS = NULL;
GeometryShader pGS = ConstructGSWithSO( CompileShader( gs_5_0, VS() ), 
                                        "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                        "3:Texcoord.xyzw; 3:$SKIP.x;", 
                                        NULL, 
                                        NULL, 
                                        1 );
PixelShader pPS = NULL;
ComputeShader pCS = NULL;
This example illustrates declaring global state block variables.
BlendState myBS[2] < bool IsValid = true; >
{
  {
    BlendEnable[0] = false;
  },
  {
    BlendEnable[0] = true;
    SrcBlendAlpha[0] = Inv_Src_Alpha;
  }
};

RasterizerState myRS
{
      FillMode = Solid;
      CullMode = NONE;
      MultisampleEnable = true;
      DepthClipEnable = false;
};

DepthStencilState myDS
{
    DepthEnable = false;
    DepthWriteMask = Zero;
    DepthFunc = Less;
};
sampler mySS[2] : register(s3) 
{
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 3;
    },
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 4;
    }
};
  
  
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](d3d11-effect-format.md)
</dt> </dl>

 

 