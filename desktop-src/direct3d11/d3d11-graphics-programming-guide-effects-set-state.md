---
title: Impostare lo stato dell'effetto (Direct3D 11)
description: Alcune costanti di effetto devono solo essere inizializzate. Vedere il codice di base per l'impostazione delle variabili di effetto in Direct3D 12.
ms.assetid: f94ba82e-fc67-4e4d-a49d-20e1163bdff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c64f9e642e867e9398722d4590a4c2ce9193b4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407664"
---
# <a name="set-effect-state-direct3d-11"></a>Impostare lo stato dell'effetto (Direct3D 11)

Alcune costanti di effetto devono solo essere inizializzate. Una volta inizializzato, lo stato dell'effetto viene impostato sul dispositivo per l'intero ciclo di rendering. Le altre variabili devono essere aggiornate ogni volta che viene chiamato il ciclo di rendering. Il codice di base per l'impostazione delle variabili di effetto è illustrato di seguito, per ognuno dei tipi di variabili.

Un effetto incapsula tutto lo stato di rendering necessario per eseguire un passaggio di rendering. In termini di API, esistono tre tipi di stato incapsulati in un effetto.

-   [Stato costante](#constant-state)
-   [Stato shader](#shader-state)
-   [Stato trama](#texture-state)

## <a name="constant-state"></a>Stato costante

In primo luogo, dichiarare le variabili in un effetto usando i tipi di dati HLSL.


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



In secondo momento, dichiarare nell'applicazione le variabili che possono essere impostate dall'applicazione e quindi aggiornare le variabili di effetto.


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

    
OnD3D11CreateDevice()
{
  ...
    g_pLightDir = g_pEffect11->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect11->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect11->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect11->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect11->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect11->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect11->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect11->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



In terzo modo, usare i metodi update per impostare il valore delle variabili nell'applicazione nelle variabili di effetto.


```
           
OnD3D11FrameRender()
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



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a>Due modi per ottenere lo stato in una variabile di effetto

Esistono due modi per ottenere lo stato contenuto in una variabile di effetto. Dato un effetto caricato in memoria.

Un modo è ottenere lo stato del campionatore da un [**id3DX11EffectVariable**](id3dx11effectvariable.md) di cui è stato eseguito il cast come interfaccia del campionatore.


```
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid() )
        hr = (l_pD3D11EffectVariable->GetBackingStore( 0, 
            &sampler_desc );
}
```



L'altro modo è ottenere lo stato del campionatore da [**id3D11SamplerState.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)


```
ID3D11SamplerState* l_ppSamplerState = NULL;
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid )
    {
        hr = l_pD3D11EffectVariable->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a>Stato shader

Lo stato dello shader viene dichiarato e assegnato in una tecnica di effetto, all'interno di un passaggio.


```
VertexShader vsRenderScene = CompileShader( vs_4_0, RenderSceneVS( 1, true, true );  
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( vsRenderScene );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



Questa operazione funziona esattamente come se non si usasse un effetto. Sono disponibili tre chiamate, una per ogni tipo di shader (vertice, geometria e pixel). Il primo, SetVertexShader, chiama [**ID3D11DeviceContext::VSSetShader.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader) CompileShader è una funzione di effetto speciale che accetta il profilo shader (vs 4 0) e il nome della funzione \_ \_ vertex shader (RenderVS). In altre parole, ognuna di queste chiamate CompileShader compila la funzione shader associata e restituisce un puntatore allo shader compilato.

Si noti che non è necessario impostare tutto lo stato dello shader. Questo passaggio non include alcuna chiamata a SetHullShader o SetDomainShader, vale a dire che gli shader della forma e del dominio attualmente associati rimangono invariati.

## <a name="texture-state"></a>Stato trama

Lo stato della trama è un po' più complesso rispetto all'impostazione di una variabile, perché i dati della trama non vengono semplicemente letti come una variabile, ma vengono campionati da una trama. Pertanto, è necessario definire la variabile di trama (proprio come una variabile normale, ad eccezione del fatto che usa un tipo di trama) ed è necessario definire le condizioni di campionamento. Di seguito è riportato un esempio di dichiarazione di variabile di trama e di dichiarazione dello stato di campionamento corrispondente.


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



Di seguito è riportato un esempio di impostazione di una trama da un'applicazione. In questo esempio la trama viene archiviata nei dati della mesh, caricati al momento della creazione dell'effetto.

Il primo passaggio consiste nell'ottenere un puntatore alla trama dall'effetto (dalla mesh).


```
ID3D11EffectShaderResourceVariable* g_ptxDiffuse = NULL;

// Obtain variables
g_ptxDiffuse = g_pEffect11->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



Il secondo passaggio consiste nel specificare una visualizzazione per l'accesso alla trama. La vista definisce un modo generale per accedere ai dati dalla risorsa trama.


```
   
OnD3D11FrameRender()
{
  ID3D11ShaderResourceView* pDiffuseRV = NULL;

  ...
  pDiffuseRV = g_Mesh11.GetMaterial(pSubset->MaterialID)->pDiffuseRV11;
  g_ptxDiffuse->SetResource( pDiffuseRV );
  ...
}   
```



Dal punto di vista dell'applicazione, le visualizzazioni di accesso non ordinato vengono gestite in modo analogo alle visualizzazioni delle risorse shader. Tuttavia, nell'effetto delle pixel shader e compute shader, i dati della visualizzazione di accesso non ordinati vengono letti o scritti direttamente in . Non è possibile eseguire il campionamento da una visualizzazione di accesso non ordinata.

Per altre informazioni sulla visualizzazione delle risorse, vedere [Risorse.](overviews-direct3d-11-resources.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un effetto (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




