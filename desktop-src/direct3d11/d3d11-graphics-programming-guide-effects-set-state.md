---
title: Impostare lo stato dell'effetto (Direct3D 11)
description: È necessario inizializzare alcune costanti di effetto.
ms.assetid: f94ba82e-fc67-4e4d-a49d-20e1163bdff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df65e164c2df01f78ae9ea9ab83a547b977335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515529"
---
# <a name="set-effect-state-direct3d-11"></a>Impostare lo stato dell'effetto (Direct3D 11)

È necessario inizializzare alcune costanti di effetto. Una volta inizializzato, lo stato dell'effetto viene impostato sul dispositivo per l'intero ciclo di rendering. È necessario aggiornare altre variabili ogni volta che viene chiamato il ciclo di rendering. Di seguito è riportato il codice di base per l'impostazione delle variabili di effetto, per ognuno dei tipi di variabili.

Un effetto incapsula tutti gli Stati di rendering necessari per eseguire un passaggio di rendering. In termini di API, esistono tre tipi di stato incapsulati in un effetto.

-   [Stato costante](#constant-state)
-   [Stato dello shader](#shader-state)
-   [Stato trama](#texture-state)

## <a name="constant-state"></a>Stato costante

Per prima cosa, dichiarare le variabili in un effetto usando i tipi di dati HLSL.


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



In secondo luogo, dichiarare le variabili nell'applicazione che possono essere impostate dall'applicazione e aggiorneranno le variabili di effetto.


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



In terzo luogo, usare i metodi Update per impostare il valore delle variabili nell'applicazione nelle variabili di effetto.


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

Esistono due modi per ottenere lo stato contenuto in una variabile effetto. Dato un effetto che è stato caricato in memoria.

Un modo consiste nell'ottenere lo stato del campionatore da un [**ID3DX11EffectVariable**](id3dx11effectvariable.md) di cui è stato eseguito il cast come interfaccia del campionatore.


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



Un altro modo consiste nell'ottenere lo stato del campionatore da un [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).


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



## <a name="shader-state"></a>Stato dello shader

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



Questa operazione funziona esattamente come se non si stesse usando un effetto. Sono disponibili tre chiamate, una per ogni tipo di shader (vertice, geometria e pixel). Il primo, SetVertexShader, chiama [**sul ID3D11DeviceContext:: VSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader). CompileShader è una funzione di effetto speciale che accetta il profilo dello shader (vs \_ 4 \_ 0) e il nome della funzione vertex shader (RenderVS). In altre parole, ciascuna di queste chiamate CompileShader compila la funzione shader associata e restituisce un puntatore allo shader compilato.

Si noti che non è necessario impostare tutti gli Stati dello shader. Questo passaggio non include alcuna chiamata a SetHullShader o SetDomainShader, vale a dire che lo scafo e gli shader del dominio attualmente associati rimarranno invariati.

## <a name="texture-state"></a>Stato trama

Lo stato della trama è leggermente più complesso rispetto all'impostazione di una variabile, perché i dati della trama non sono semplicemente letti come una variabile, vengono campionati da una trama. Pertanto, è necessario definire la variabile di trama (proprio come una variabile normale ad eccezione del fatto che usa un tipo di trama) ed è necessario definire le condizioni di campionamento. Di seguito è riportato un esempio di una dichiarazione di variabile di trama e la dichiarazione dello stato di campionamento corrispondente.


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



Di seguito è riportato un esempio di impostazione di una trama da un'applicazione. In questo esempio, la trama viene archiviata nei dati della mesh, che è stata caricata quando è stato creato l'effetto.

Il primo passaggio consiste nell'ottenere un puntatore alla trama dall'effetto (dalla mesh).


```
ID3D11EffectShaderResourceVariable* g_ptxDiffuse = NULL;

// Obtain variables
g_ptxDiffuse = g_pEffect11->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



Il secondo passaggio consiste nel specificare una visualizzazione per accedere alla trama. La visualizzazione definisce un modo generale per accedere ai dati dalla risorsa trama.


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



Dal punto di vista dell'applicazione, le visualizzazioni di accesso non ordinato vengono gestite in modo analogo alle viste delle risorse dello shader. Tuttavia, nelle funzioni pixel shader e compute shader, i dati della vista di accesso non ordinati vengono letti da/scritti direttamente in. Non è possibile eseguire l'esempio da una visualizzazione di accesso non ordinata.

Per ulteriori informazioni sulla visualizzazione delle risorse, vedere [risorse](overviews-direct3d-11-resources.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un effetto (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




