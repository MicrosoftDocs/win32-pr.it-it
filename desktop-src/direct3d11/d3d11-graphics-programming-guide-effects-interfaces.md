---
title: Interfacce di sistema effetto (Direct3D 11)
description: Il sistema degli effetti definisce diverse interfacce per la gestione dello stato dell'effetto.
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708545"
---
# <a name="effect-system-interfaces-direct3d-11"></a>Interfacce di sistema effetto (Direct3D 11)

Il sistema degli effetti definisce diverse interfacce per la gestione dello stato dell'effetto. Esistono due tipi di interfacce: quelle usate dal runtime per eseguire il rendering di un effetto e delle interfacce di reflection per ottenere e impostare le variabili di effetto.

-   [Interfacce di runtime degli effetti](#effect-runtime-interfaces)
-   [Interfacce di Reflection effetto](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Interfacce di runtime degli effetti

Usare le interfacce di runtime per eseguire il rendering di un effetto.



| Interfacce di runtime                                       | Descrizione                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)                   | Raccolta di uno o più gruppi e tecniche per il rendering. |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)           | Raccolta di assegnazioni di stato.                             |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) | Raccolta di uno o più passaggi.                            |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)         | Raccolta di una o più tecniche.                        |



 

## <a name="effect-reflection-interfaces"></a>Interfacce di Reflection effetto

La reflection è implementata nel sistema di effetti per supportare la lettura e la scrittura dello stato dell'effetto. Sono disponibili diversi modi per accedere alle variabili di effetto.

### <a name="setting-groups-of-effect-state"></a>Impostazione dei gruppi di stato effetto

Usare queste interfacce per ottenere e impostare un gruppo di stato.



| Interfacce di Reflection                                                          | Descrizione                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)               | Ottenere e impostare lo stato di Blend.         |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md) | Ottenere e impostare lo stato di stencil Depth. |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)     | Ottiene e imposta lo stato di rasterizzazione.    |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)           | Ottiene e imposta lo stato del campionatore.       |



 

### <a name="setting-effect-resources"></a>Impostazione delle risorse degli effetti

Usare queste interfacce per ottenere e impostare le risorse.



| Interfacce di Reflection                                                                        | Descrizione                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)                           | Accedere ai dati in un buffer di trama o in un buffer costante. |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)       | Accedere ai dati in una risorsa di stencil di profondità.            |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)       | Accedere ai dati in una destinazione di rendering.                     |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)           | Accedere ai dati in una risorsa shader.                   |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md) | Accedere ai dati in una visualizzazione di accesso non ordinata.            |



 

### <a name="setting-other-effect-variables"></a>Impostazione di altre variabili di effetto

Usare queste interfacce per ottenere e impostare lo stato in base al tipo di variabile.



| Interfacce di Reflection                                                            | Descrizione               |
|----------------------------------------------------------------------------------|---------------------------|
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) | Ottenere un'istanza della classe.     |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)         | Ottenere e impostare un'interfaccia. |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)               | Ottenere e impostare una matrice.     |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)               | Ottenere e impostare un valore scalare.     |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)               | Ottiene una variabile shader.    |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)               | Ottenere e impostare una stringa.     |
| [**ID3DX11EffectType**](id3dx11effecttype.md)                                   | Ottiene un tipo di variabile.      |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)               | Ottenere e impostare un vettore.     |



 

Tutte le interfacce di Reflection derivano da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Guida alla programmazione per Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

 




