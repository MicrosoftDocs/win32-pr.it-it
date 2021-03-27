---
title: Differenze tra gli effetti 10 e gli effetti 11
description: In questo argomento vengono illustrate le differenze tra gli effetti 10 e gli effetti 11.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29af1b9e7aec72f96a62e0f62668b81a6eec8367
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728231"
---
# <a name="differences-between-effects-10-and-effects-11"></a>Differenze tra gli effetti 10 e gli effetti 11

In questo argomento vengono illustrate le differenze tra gli effetti 10 e gli effetti 11.

## <a name="device-contexts-threading-and-cloning"></a>Contesti di dispositivo, Threading e clonazione

L'interfaccia ID3D10Device è stata suddivisa in due interfacce in Direct3D 11: ID3D11Device e sul ID3D11DeviceContext. È possibile creare più ID3D11DeviceContexts per semplificare l'esecuzione simultanea su più thread. Effects 11 estende questo concetto al Framework Effects.

Il runtime di Effects 11 è a thread singolo. Per questo motivo, non è consigliabile usare una singola istanza di ID3DX11Effect con più thread contemporaneamente.

Per usare il runtime di Effects 11 su più istanze, è necessario creare istanze separate di ID3DX11Effect. Poiché sul ID3D11DeviceContext è anche a thread singolo, è necessario passare diverse istanze di sul ID3D11DeviceContext a ogni istanza dell'effetto su Apply. È possibile usare questi contesti di dispositivo distinti per creare elenchi di comandi, in modo che il thread di rendering possa applicarli nel contesto di dispositivo immediato.

Il modo più semplice per creare più effetti che incapsulano la stessa funzionalità, da usare su più thread, consiste nel creare un effetto e quindi eseguire copie clonate. La clonazione presenta i vantaggi seguenti rispetto alla creazione di più copie da zero:

1.  La routine di clonazione è più veloce rispetto alla routine di creazione.
2.  Gli effetti clonati condividono gli shader creati, i blocchi di stato e le istanze di classe (pertanto non devono essere ricreati).
3.  Gli effetti clonati possono condividere buffer costanti.
4.  Gli effetti clonati iniziano con lo stato che corrisponde all'effetto corrente (valori di variabile, indipendentemente dal fatto che sia stato ottimizzato).

Per ulteriori informazioni, vedere [clonazione di un effetto](d3d11-graphics-programming-guide-effects-cloning.md) .

## <a name="effect-pools-and-groups"></a>Gruppi e pool di effetti

Di gran lunga l'uso più diffuso dei pool di effetti in Direct3D 10 era per il raggruppamento di materiali. I pool di effetti sono stati rimossi dagli effetti 11 e sono stati aggiunti gruppi, un metodo più efficiente per raggruppare i materiali.

Un gruppo di effetti è semplicemente un set di tecniche. Per ulteriori informazioni, vedere la [sintassi del gruppo di effetti (Direct3D 11)](d3d11-effect-group-syntax.md) .

Si consideri la gerarchia degli effetti seguente con quattro effetti figlio e un pool di effetti:


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



## <a name="new-shader-stages"></a>Nuove fasi dello shader

In Direct3D 11 sono disponibili tre nuove fasi dello shader: Hull shader, Domain shader e compute shader. Effects 11 li gestisce in modo analogo ai vertex shader, alla geometria shader e ai pixel shader.

Sono stati aggiunti tre nuovi tipi di variabili agli effetti 11:

-   HullShader
-   DomainShader
-   ComputeShader

Se si usano questi shader in una tecnica, è necessario etichettare la tecnica "technique11" e non "technique10". Compute shader non può essere impostato nello stesso passaggio di qualsiasi altro stato di grafica (altri shader, blocchi di stato o destinazioni di rendering).

## <a name="new-texture-types"></a>Nuovi tipi di trama

Direct3D 11 supporta i tipi di trama seguenti:

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a>Viste di accesso non ordinate

Effects 11 supporta il recupero e l'impostazione dei nuovi tipi di visualizzazione di accesso non ordinato. Funziona in modo analogo alle trame.

Considerare questo esempio di effetti HLSL:


```
  
RWTexture1D<float> myUAV;
```



È possibile impostare questa variabile in C++ come indicato di seguito:


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



Direct3D 11 supporta i tipi di vista di accesso non ordinati seguenti:

-   RWBuffer
-   RWByteAddressBuffer
-   RWStructuredBuffer
-   RWTexture1D
-   RWTexture1DArray
-   RWTexture2D
-   RWTexture2DArray
-   RWTexture3D

## <a name="interfaces-and-class-instances"></a>Interfacce e istanze di classe

Per la sintassi dell'interfaccia e della classe, vedere [interfacce e classi](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

Per l'uso di interfacce e classi in effetti, vedere [interfacce e classi in effetti](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).

## <a name="addressable-stream-out"></a>Flusso indirizzabile in uscita

In Direct3D 10, Geometry shaders può restituire un flusso di dati all'unità di output del flusso e all'unità di rasterizzazione. In Direct3D11, la geometria shader può restituire fino a quattro flussi di dati all'unità di output del flusso e al massimo uno di questi flussi per l'unità di rasterizzazione. La funzione intrinseca **ConstructGSWithSO** è stata aggiornata per riflettere questa nuova funzionalità.

Per ulteriori informazioni, vedere la [sintassi di streaming](d3d11-graphics-reference-effect-streamout.md) .

## <a name="setting-and-unsetting-device-state"></a>Impostazione e disimpostazione dello stato del dispositivo

Negli effetti 10, è possibile rendere i buffer costanti e i buffer di trama gestiti dall'utente usando le funzioni [**ID3D10EffectConstantBuffer:: SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) e [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) . Dopo aver chiamato queste funzioni, il runtime di Effects 10 non gestisce più il buffer costante o il buffer di trama e l'utente deve riempire i dati usando l'interfaccia ID3D10Device.

In Effects 11 è inoltre possibile rendere gestiti dall'utente i blocchi di stato (stato di Blend, stato di rasterizzazione, stato dello stencil Depth e stato del campionatore) tramite le chiamate seguenti:

-   [**ID3DX11EffectBlendVariable::SetBlendState**](id3dx11effectblendvariable-setblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::SetRasterizerState**](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable:: sesampler**](id3dx11effectsamplervariable-setsampler.md)

Una volta chiamate queste funzioni, il runtime di Effects 11 non gestisce più le variabili del blocco di stato e i valori rimarranno invariati. Si noti che poiché i blocchi di stato non sono modificabili, l'utente deve impostare un nuovo blocco di stato per modificare i valori.

È anche possibile ripristinare i buffer costanti, i buffer di trama e i blocchi di stato allo stato non gestito dall'utente. Se si impostano queste variabili, il runtime di Effects 11 continuerà ad aggiornarle quando necessario. Per annullare le variabili gestite dall'utente, è possibile usare le chiamate seguenti:

-   [**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [**ID3DX11EffectBlendVariable::UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a>Effetti della macchina virtuale

La macchina virtuale Effects, che ha valutato espressioni complesse al di fuori delle funzioni, è stata rimossa.

Gli esempi di espressioni complesse seguenti non sono supportati:

1.  SetPixelShader (myPSArray (i \* 3 + j));
2.  SetPixelShader (myPSArray ((float) i);
3.  FILTER = i + 2;

Sono supportati gli esempi seguenti di espressioni non complesse:

1.  SetPixelShader( myPS );
2.  SetPixelShader (myPS \[ i \] );
3.  SetPixelShader (myPS \[ uIndex \] );//uIndex è una variabile uint
4.  FILTRO = i;
5.  FILTER = ANISOTROPICO;

Queste espressioni possono essere visualizzate nelle espressioni di blocco di stato (ad esempio filtro) e nelle espressioni Pass (ad esempio SetPixelShader).

## <a name="source-availability-and-location"></a>Disponibilità e percorso di origine

Gli effetti 10 sono stati distribuiti in D3D10.dll. Effects 11 viene distribuito come origine, con le soluzioni di Visual Studio corrispondenti per compilarlo. Quando si creano applicazioni di tipo Effects, è consigliabile includere l'origine Effects 11 direttamente in tali applicazioni.

È possibile ottenere gli effetti 11 dagli [effetti per l'aggiornamento di Direct3D 11](https://github.com/Microsoft/FX11).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 