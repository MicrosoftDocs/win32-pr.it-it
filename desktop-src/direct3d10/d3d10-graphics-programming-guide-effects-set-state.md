---
description: Alcune costanti di effetto devono essere inizializzate. Vedere il codice di base per l'impostazione delle variabili di effetto in Direct3D 10.
ms.assetid: 743261a8-fdd8-492e-be8a-4faeb9b6f986
title: Impostare lo stato dell'effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df7133276b6392abca8d75eed16de896fb58f84
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404724"
---
# <a name="set-effect-state-direct3d-10"></a><span data-ttu-id="26828-104">Impostare lo stato dell'effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="26828-104">Set Effect State (Direct3D 10)</span></span>

<span data-ttu-id="26828-105">Alcune costanti di effetto devono essere inizializzate.</span><span class="sxs-lookup"><span data-stu-id="26828-105">Some effect constants only need to be initialized.</span></span> <span data-ttu-id="26828-106">Dopo l'inizializzazione, lo stato dell'effetto viene impostato sul dispositivo per l'intero ciclo di rendering.</span><span class="sxs-lookup"><span data-stu-id="26828-106">Once initialized, the effect state is set to the device for the entire render loop.</span></span> <span data-ttu-id="26828-107">È necessario aggiornare altre variabili ogni volta che viene chiamato il ciclo di rendering.</span><span class="sxs-lookup"><span data-stu-id="26828-107">Other variables need to be updated each time the render loop is called.</span></span> <span data-ttu-id="26828-108">Il codice di base per l'impostazione delle variabili di effetto è illustrato di seguito, per ognuno dei tipi di variabili.</span><span class="sxs-lookup"><span data-stu-id="26828-108">The basic code for setting effect variables is shown below, for each of the types of variables.</span></span>

<span data-ttu-id="26828-109">Un effetto incapsula tutto lo stato di rendering necessario per eseguire un passaggio di rendering.</span><span class="sxs-lookup"><span data-stu-id="26828-109">An effect encapsulates all of the render state required to do a rendering pass.</span></span> <span data-ttu-id="26828-110">In termini di API, esistono tre tipi di stato incapsulati in un effetto.</span><span class="sxs-lookup"><span data-stu-id="26828-110">In terms of the API, there are three types of state encapsulated in an effect.</span></span>

-   [<span data-ttu-id="26828-111">Stato costante</span><span class="sxs-lookup"><span data-stu-id="26828-111">Constant State</span></span>](#constant-state)
-   [<span data-ttu-id="26828-112">Stato shader</span><span class="sxs-lookup"><span data-stu-id="26828-112">Shader State</span></span>](#shader-state)
-   [<span data-ttu-id="26828-113">Stato trama</span><span class="sxs-lookup"><span data-stu-id="26828-113">Texture State</span></span>](#texture-state)

## <a name="constant-state"></a><span data-ttu-id="26828-114">Stato costante</span><span class="sxs-lookup"><span data-stu-id="26828-114">Constant State</span></span>

<span data-ttu-id="26828-115">In primo luogo, dichiarare le variabili in un effetto usando i tipi di dati HLSL.</span><span class="sxs-lookup"><span data-stu-id="26828-115">First, declare variables in an effect using HLSL data types.</span></span>


```
//--------------------------------------------------------------------------------------
// Global variables
//--------------------------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
```



<span data-ttu-id="26828-116">In secondo piano, dichiarare le variabili nell'applicazione che possono essere impostate dall'applicazione e quindi aggiornare le variabili dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="26828-116">Second, declare variables in the application that can be set by the application, and will then update the effect variables.</span></span>


```
           
    D3DXMATRIX  mWorldViewProjection;
    D3DXVECTOR3 vLightDir[MAX_LIGHTS];
    D3DXVECTOR4 vLightDiffuse[MAX_LIGHTS];
    D3DXMATRIX  mWorld;
    D3DXMATRIX  mView;
    D3DXMATRIX  mProj;

    // Get the projection and view matrix from the camera class
    mWorld = g_mCenterMesh * *g_Camera.GetWorldMatrix();
    mProj = *g_Camera.GetProjMatrix();
    mView = *g_Camera.GetViewMatrix();

    
OnD3D10CreateDevice()
{
  ...
    g_pLightDir = g_pEffect10->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect10->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect10->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect10->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect10->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect10->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect10->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect10->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



<span data-ttu-id="26828-117">In terzo piano, usare i metodi di aggiornamento per impostare il valore delle variabili nell'applicazione nelle variabili dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="26828-117">Third, use the update methods to set the value of the variables in the application in the effect variables.</span></span>


```
           
OnD3D10FrameRender()
{
    ...
    g_pLightDir->SetRawValue( vLightDir, 0, sizeof(D3DXVECTOR3)*MAX_LIGHTS );
    g_pLightDiffuse->SetFloatVectorArray( (float*)vLightDiffuse, 0, MAX_LIGHTS );
    g_pmWorldViewProjection->SetMatrix( (float*)&mWorldViewProjection );
    g_pmWorld->SetMatrix( (float*)&mWorld );
    g_pfTime->SetFloat( (float)fTime );
    g_pnNumLights->SetInt( g_nNumActiveLights );
}
```



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a><span data-ttu-id="26828-118">Due modi per ottenere lo stato in una variabile di effetto</span><span class="sxs-lookup"><span data-stu-id="26828-118">Two Ways to Get the State in an Effect Variable</span></span>

<span data-ttu-id="26828-119">Esistono due modi per ottenere lo stato contenuto in una variabile di effetto.</span><span class="sxs-lookup"><span data-stu-id="26828-119">There are two ways to get the state contained in an effect variable.</span></span> <span data-ttu-id="26828-120">Dato un effetto caricato in memoria.</span><span class="sxs-lookup"><span data-stu-id="26828-120">Given an effect that has been loaded into memory.</span></span>

<span data-ttu-id="26828-121">Un modo è ottenere lo stato del campionatore da [**un'interfaccia ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) di cui è stato eseguito il cast come interfaccia del campionatore.</span><span class="sxs-lookup"><span data-stu-id="26828-121">One way is to get the sampler state from an [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) that has been cast as a sampler interface.</span></span>


```
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
        hr = (l_pD3D10EffectVariable->AsSampler())->GetBackingStore( 0, 
            &sampler_desc );
}
```



<span data-ttu-id="26828-122">L'altro modo è ottenere lo stato del campionatore da [**un'interfaccia ID3D10SamplerState**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate).</span><span class="sxs-lookup"><span data-stu-id="26828-122">The other way is to get the sampler state from an [**ID3D10SamplerState Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate).</span></span>


```
ID3D10SamplerState* l_ppSamplerState = NULL;
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
    {
        hr = (l_pD3D10EffectVariable->AsSampler())->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a><span data-ttu-id="26828-123">Stato shader</span><span class="sxs-lookup"><span data-stu-id="26828-123">Shader State</span></span>

<span data-ttu-id="26828-124">Lo stato dello shader viene dichiarato e assegnato in una tecnica di effetto, all'interno di un passaggio.</span><span class="sxs-lookup"><span data-stu-id="26828-124">Shader state is declared and assigned in an effect technique, within a pass.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



<span data-ttu-id="26828-125">Questa operazione funziona esattamente come se non si usasse un effetto.</span><span class="sxs-lookup"><span data-stu-id="26828-125">This works just like it would if you were not using an effect.</span></span> <span data-ttu-id="26828-126">Sono disponibili tre chiamate, una per ogni tipo di shader (vertice, geometria e pixel).</span><span class="sxs-lookup"><span data-stu-id="26828-126">There are three calls, one for each type of shader (vertex, geometry, and pixel).</span></span> <span data-ttu-id="26828-127">Il primo, SetVertexShader, chiama [**ID3D10Device::VSSetShader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader).</span><span class="sxs-lookup"><span data-stu-id="26828-127">The first one, SetVertexShader, calls [**ID3D10Device::VSSetShader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader).</span></span> <span data-ttu-id="26828-128">CompileShader è una funzione di effetto speciale che accetta il profilo shader (vs 4 0) e il nome della funzione \_ \_ vertex shader (RenderVS).</span><span class="sxs-lookup"><span data-stu-id="26828-128">CompileShader is a special effect function that takes the shader profile(vs\_4\_0) and the name of the vertex shader function (RenderVS).</span></span> <span data-ttu-id="26828-129">In altre parole, ognuna di queste chiamate SetXXXShader compila la funzione shader associata e restituisce un puntatore allo shader compilato.</span><span class="sxs-lookup"><span data-stu-id="26828-129">In other words, each of these SetXXXShader calls compiles their associated shader function and returns a pointer to the compiled shader.</span></span>

## <a name="texture-state"></a><span data-ttu-id="26828-130">Stato trama</span><span class="sxs-lookup"><span data-stu-id="26828-130">Texture State</span></span>

<span data-ttu-id="26828-131">Lo stato della trama è un po' più complesso rispetto all'impostazione di una variabile, perché i dati di trama non vengono semplicemente letti come una variabile, ma vengono campionati da una trama.</span><span class="sxs-lookup"><span data-stu-id="26828-131">Texture state is a little more complex than setting a variable, because texture data is not simply read like a variable, it is sampled from a texture.</span></span> <span data-ttu-id="26828-132">Pertanto, è necessario definire la variabile di trama (proprio come una variabile normale, ad eccezione del fatto che usa un tipo di trama) ed è necessario definire le condizioni di campionamento.</span><span class="sxs-lookup"><span data-stu-id="26828-132">Therefore, you must define the texture variable (just like a normal variable except it uses a texture type) and you must define the sampling conditions.</span></span> <span data-ttu-id="26828-133">Di seguito è riportato un esempio di dichiarazione di variabile di trama e di dichiarazione dello stato di campionamento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="26828-133">Here is an example of a texture variable declaration and the corresponding sampling state declaration.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



<span data-ttu-id="26828-134">Di seguito è riportato un esempio di impostazione di una trama da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="26828-134">Here is an example of setting a texture from an application.</span></span> <span data-ttu-id="26828-135">In questo esempio la trama viene archiviata nei dati della mesh, caricati al momento della creazione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="26828-135">In this example, the texture is stored in the mesh data, that was loaded when the effect was created.</span></span>

<span data-ttu-id="26828-136">Il primo passaggio consiste nell'ottenere un puntatore alla trama dall'effetto (dalla mesh).</span><span class="sxs-lookup"><span data-stu-id="26828-136">The first step is getting a pointer to the texture from the effect (from the mesh).</span></span>


```
ID3D10EffectShaderResourceVariable* g_ptxDiffuse = NULL;

    // Obtain variables
    g_ptxDiffuse = g_pEffect10->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



<span data-ttu-id="26828-137">Il secondo passaggio consiste nel specificare una vista per l'accesso alla trama.</span><span class="sxs-lookup"><span data-stu-id="26828-137">The second step is specifying a view for accessing the texture.</span></span> <span data-ttu-id="26828-138">La vista definisce un modo generale per accedere ai dati dalla risorsa trama.</span><span class="sxs-lookup"><span data-stu-id="26828-138">The view defines a general way to access the data from the texture resource.</span></span>


```
   
OnD3D10FrameRender()
{
  ID3D10ShaderResourceView* pDiffuseRV = NULL;

   ...
   pDiffuseRV = g_Mesh10.GetMaterial(pSubset->MaterialID)->pDiffuseRV10;
   g_ptxDiffuse->SetResource( pDiffuseRV );
   ...
}   
```



<span data-ttu-id="26828-139">Per altre informazioni sulla visualizzazione delle risorse, vedere [Visualizzazioni trama (Direct3D 10).](d3d10-graphics-programming-guide-resources-access-views.md)</span><span class="sxs-lookup"><span data-stu-id="26828-139">For more information about viewing resources, see [Texture Views (Direct3D 10)](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="26828-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26828-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26828-141">Rendering di un effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="26828-141">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



