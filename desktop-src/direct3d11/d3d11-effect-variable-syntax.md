---
title: Sintassi della variabile Effect (Direct3D 11)
description: Una variabile Effect viene dichiarata con la sintassi descritta in questa sezione.
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67710642060ffea642434ba2d23a77cec2fb8bc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473182"
---
# <a name="effect-variable-syntax-direct3d-11"></a><span data-ttu-id="188b8-103">Sintassi della variabile Effect (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="188b8-103">Effect Variable Syntax (Direct3D 11)</span></span>

<span data-ttu-id="188b8-104">Una variabile Effect viene dichiarata con la sintassi descritta in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="188b8-104">An effect variable is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="188b8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="188b8-105">Syntax</span></span>

<span data-ttu-id="188b8-106">Sintassi di base:</span><span class="sxs-lookup"><span data-stu-id="188b8-106">Basic syntax:</span></span>

<span data-ttu-id="188b8-107">*DataType* *variablename* \[ *: semanticname* \]  <  *Annotations*  >  \[ = InitialValue \] ;</span><span class="sxs-lookup"><span data-stu-id="188b8-107">*DataType* *VariableName* \[ *: SemanticName* \] < *Annotations* > \[ = InitialValue \];</span></span>

<span data-ttu-id="188b8-108">Per la sintassi completa, vedere [sintassi delle variabili (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) .</span><span class="sxs-lookup"><span data-stu-id="188b8-108">See [Variable Syntax (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) for full syntax.</span></span>



| <span data-ttu-id="188b8-109">Nome</span><span class="sxs-lookup"><span data-stu-id="188b8-109">Name</span></span>         | <span data-ttu-id="188b8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="188b8-110">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="188b8-111">DataType</span><span class="sxs-lookup"><span data-stu-id="188b8-111">DataType</span></span>     | <span data-ttu-id="188b8-112">Qualsiasi tipo di [base](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [trama](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), visualizzazione di accesso non ordinato, shader o tipo di blocco di stato.</span><span class="sxs-lookup"><span data-stu-id="188b8-112">Any [basic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [texture](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), unordered access view, shader or state block type.</span></span>                            |
| <span data-ttu-id="188b8-113">VariableName</span><span class="sxs-lookup"><span data-stu-id="188b8-113">VariableName</span></span> | <span data-ttu-id="188b8-114">Stringa ASCII che identifica in modo univoco il nome della variabile di effetto.</span><span class="sxs-lookup"><span data-stu-id="188b8-114">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="188b8-115">Semanticname</span><span class="sxs-lookup"><span data-stu-id="188b8-115">SemanticName</span></span> | <span data-ttu-id="188b8-116">Stringa ASCII che indica informazioni aggiuntive sulla modalità di utilizzo di una variabile.</span><span class="sxs-lookup"><span data-stu-id="188b8-116">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="188b8-117">Una semantica è una stringa ASCII che può essere un valore di sistema predefinito o una stringa utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="188b8-117">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="188b8-118">annotazioni</span><span class="sxs-lookup"><span data-stu-id="188b8-118">Annotations</span></span>  | <span data-ttu-id="188b8-119">Una o più parti di informazioni (metadati) fornite dall'utente ignorate dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="188b8-119">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="188b8-120">Per la sintassi, vedere [sintassi delle annotazioni (Direct3D 11)](d3d11-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="188b8-120">For syntax, see [Annotation Syntax (Direct3D 11)](d3d11-effect-annotation-syntax.md).</span></span>     |
| <span data-ttu-id="188b8-121">InitialValue</span><span class="sxs-lookup"><span data-stu-id="188b8-121">InitialValue</span></span> | <span data-ttu-id="188b8-122">Valore predefinito della variabile.</span><span class="sxs-lookup"><span data-stu-id="188b8-122">The default value of the variable.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="188b8-123">Una variabile di effetto dichiarata al di fuori di tutte le funzioni è considerata globale nell'ambito. le variabili dichiarate all'interno di una funzione sono locali a tale funzione.</span><span class="sxs-lookup"><span data-stu-id="188b8-123">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="188b8-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="188b8-124">Example</span></span>

<span data-ttu-id="188b8-125">Questo esempio illustra le variabili numeriche degli effetti globali.</span><span class="sxs-lookup"><span data-stu-id="188b8-125">This example illustrates global effect numeric variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="188b8-126">Questo esempio illustra le variabili di effetto locali a una funzione shader.</span><span class="sxs-lookup"><span data-stu-id="188b8-126">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="188b8-127">In questo esempio vengono illustrati i parametri della funzione con semantica.</span><span class="sxs-lookup"><span data-stu-id="188b8-127">This example illustrates function parameters that have semantics.</span></span>


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



<span data-ttu-id="188b8-128">In questo esempio viene illustrata la dichiarazione di una variabile di trama globale.</span><span class="sxs-lookup"><span data-stu-id="188b8-128">This example illustrates declaring a global texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="188b8-129">Campionamento di una trama viene eseguita con un campionatore di trame.</span><span class="sxs-lookup"><span data-stu-id="188b8-129">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="188b8-130">Per configurare un campionatore in un effetto, vedere il [tipo di campionatore](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span><span class="sxs-lookup"><span data-stu-id="188b8-130">To set up a sampler in an effect, see the [sampler type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

<span data-ttu-id="188b8-131">In questo esempio viene illustrata la dichiarazione di variabili di visualizzazione di accesso non ordinato globali.</span><span class="sxs-lookup"><span data-stu-id="188b8-131">This example illustrates declaring global unordered access view variables.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="188b8-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="188b8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="188b8-133">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="188b8-133">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 