---
title: Differenze tra gli effetti 10 e gli effetti 11
description: Questo argomento illustra le differenze tra Effetti 10 e Effetti 11.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b488015deae8cc93b9bc692c49d66ff1510bcc5639047fe253265be5b382a85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990121"
---
# <a name="differences-between-effects-10-and-effects-11"></a>Differenze tra gli effetti 10 e gli effetti 11

Questo argomento illustra le differenze tra Effetti 10 e Effetti 11.

## <a name="device-contexts-threading-and-cloning"></a>Contesti di dispositivo, threading e clonazione

L'interfaccia ID3D10Device è stata suddivisa in due interfacce in Direct3D 11: ID3D11Device e ID3D11DeviceContext. È possibile creare più oggetti ID3D11DeviceContext per facilitare l'esecuzione simultanea in più thread. Effects 11 estende questo concetto al framework Effetti.

Il runtime di Effects 11 è a thread singolo. Per questo motivo, non è consigliabile usare una singola istanza id3DX11Effect con più thread contemporaneamente.

Per usare il runtime di Effects 11 in più istanze, è necessario creare istanze ID3DX11Effect separate. Poiché anche ID3D11DeviceContext è a thread singolo, è necessario passare istanze ID3D11DeviceContext diverse a ogni istanza dell'effetto in Apply. È possibile usare questi contesti di dispositivo separati per creare elenchi di comandi in modo che il thread di rendering possa applicarli al contesto di dispositivo immediato.

Il modo più semplice per creare più effetti che incapsulano la stessa funzionalità, da usare su più thread, è creare un effetto e quindi creare copie clonate. La clonazione presenta i vantaggi seguenti rispetto alla creazione di più copie da zero:

1.  La routine di clonazione è più veloce della routine di creazione.
2.  Gli effetti clonati condividono shader creati, blocchi di stato e istanze di classe (quindi non devono essere ricreati).
3.  Gli effetti clonati possono condividere buffer costanti.
4.  Gli effetti clonati iniziano con lo stato corrispondente all'effetto corrente (i valori delle variabili, indipendentemente dal fatto che sia stato ottimizzato o meno).

Per [altre informazioni, vedere Clonazione](d3d11-graphics-programming-guide-effects-cloning.md) di un effetto.

## <a name="effect-pools-and-groups"></a>Pool di effetti e gruppi

Di gran lunga l'uso più diffuso dei pool di effetti in Direct3D 10 è stato per il raggruppamento dei materiali. I pool di effetti sono stati rimossi da Effects 11 e sono stati aggiunti gruppi, che è un metodo più efficiente per raggruppare i materiali.

Un gruppo di effetti è semplicemente un set di tecniche. Per altre informazioni, vedere Sintassi dei gruppi di effetti [(Direct3D 11).](d3d11-effect-group-syntax.md)

Si consideri la gerarchia di effetti seguente con quattro effetti figlio e un pool di effetti:


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



È possibile ottenere la stessa funzionalità in Effects 11 usando i gruppi:


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a>Nuove fasi shader

In Direct3D 11 sono disponibili tre nuove fasi dello shader: hull shader, domain shader e compute shader. Gli effetti 11 le gestisce in modo simile a vertex shader, geometry shader e pixel shader.

In Effects 11 sono stati aggiunti tre nuovi tipi di variabili:

-   HullShader
-   DomainShader
-   ComputeShader

Se si usano questi shader in una tecnica, è necessario etichettare tale tecnica "technique11" e non "technique10". Lo shader di calcolo non può essere impostato nello stesso passaggio di qualsiasi altro stato grafico (altri shader, blocchi di stato o destinazioni di rendering).

## <a name="new-texture-types"></a>Nuovi tipi di trama

Direct3D 11 supporta i tipi di trama seguenti:

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a>Viste di accesso non ordinate

Effects 11 supporta il recupero e l'impostazione dei nuovi tipi di visualizzazione di accesso non ordinati. Il funzionamento è simile a quello delle trame.

Si consideri questo esempio di HLSL effects:


```
  
RWTexture1D<float> myUAV;
```



È possibile impostare questa variabile in C++ come segue:


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



Direct3D 11 supporta i tipi di visualizzazione di accesso non ordinati seguenti:

-   RWBuffer
-   RWByteAddressBuffer
-   RWStructuredBuffer
-   RWTexture1D
-   RWTexture1DArray
-   RWTexture2D
-   RWTexture2DArray
-   RWTexture3D

## <a name="interfaces-and-class-instances"></a>Interfacce e istanze di classe

Per la sintassi di interfacce e classi, [vedere Interfacce e classi](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

Per l'uso di interfacce e classi negli effetti, vedere [Interfacce e classi in Effetti](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).

## <a name="addressable-stream-out"></a>Flusso indirizzabile in uscita

In Direct3D 10, gli shader geometry possono eseguire l'output di un flusso di dati nell'unità di output del flusso e nell'unità di rasterizzazione. In Direct3D11, gli shader geometry possono eseguire l'output di un massimo di quattro flussi di dati nell'unità di output del flusso e al massimo di uno di questi flussi all'unità di rasterizzazione. La **funzione intrinseca ConstructGSWithSO** è stata aggiornata per riflettere questa nuova funzionalità.

Per [altre informazioni, vedere Sintassi di stream out.](d3d11-graphics-reference-effect-streamout.md)

## <a name="setting-and-unsetting-device-state"></a>Impostazione e annullamento dell'impostazione dello stato del dispositivo

In Effects 10 è possibile creare buffer costanti e buffer di trama gestiti dall'utente usando le funzioni [**ID3D10EffectConstantBuffer::SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) e [**SetTextureBuffer.**](id3dx11effectconstantbuffer-settexturebuffer.md) Dopo aver chiamato queste funzioni, il runtime di Effects 10 non gestisce più il buffer costante o il buffer di trama e l'utente deve riempire i dati usando l'interfaccia ID3D10Device.

In Effetti 11 è anche possibile rendere i blocchi di stato (stato di fusione, stato del rasterizzatore, stato depth-stencil e stato del campionatore) gestiti dall'utente usando le chiamate seguenti:

-   [**ID3DX11EffectBlendVariable::SetBlendState**](id3dx11effectblendvariable-setblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::SetRasterizerState**](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::SetSampler**](id3dx11effectsamplervariable-setsampler.md)

Dopo aver chiamato queste funzioni, il runtime di Effects 11 non gestisce più le variabili del blocco di stato e i valori rimangono invariati. Si noti che poiché i blocchi di stato non sono modificabili, l'utente deve impostare un nuovo blocco di stato per modificare i valori.

È anche possibile ripristinare lo stato gestito non utente di buffer costanti, buffer di trama e blocchi di stato. Se si deselezionano queste variabili, il runtime di Effects 11 continuerà ad aggiornarle quando necessario. È possibile usare le chiamate seguenti per annullare l'impostata delle variabili gestite dall'utente:

-   [**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [**ID3DX11EffectBlendVariable::UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a>Macchina virtuale effetti

La macchina virtuale effetti, che ha valutato espressioni complesse al di fuori delle funzioni, è stata rimossa.

Gli esempi seguenti di espressioni complesse non sono supportati:

1.  SetPixelShader( myPSArray( i \* 3 + j ) );
2.  SetPixelShader( myPSArray( (float)i );
3.  FILTER = i + 2;

Sono supportati gli esempi seguenti di espressioni non complesse:

1.  SetPixelShader( myPS );
2.  SetPixelShader( myPS \[ i \] );
3.  SetPixelShader( myPS \[ uIndex \] ); // uIndex è una variabile uint
4.  FILTER = i;
5.  FILTER = ANISOTROP;

Queste espressioni possono essere visualizzate nelle espressioni di blocco di stato (ad esempio FILTER) e nelle espressioni di passaggio (ad esempio SetPixelShader).

## <a name="source-availability-and-location"></a>Disponibilità e posizione dell'origine

Effects 10 è stato distribuito in D3D10.dll. Effects 11 viene distribuito come origine, con Visual Studio soluzioni corrispondenti per compilarlo. Quando si creano applicazioni di tipo effetti, è consigliabile includere l'origine Effects 11 direttamente in tali applicazioni.

È possibile ottenere Effects 11 da [Effects for Direct3D 11 Update](https://github.com/Microsoft/FX11).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 