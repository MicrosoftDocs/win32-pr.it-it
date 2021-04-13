---
title: Interfacce Effects 11
description: Questa sezione contiene informazioni di riferimento per le interfacce COM (Component Object Model) dell'origine Effects 11.
ms.assetid: 1b997513-73f7-423a-8af3-1c9fa0d2f469
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215e319720f2afc4cf74f6c49056de35fb59d004
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104976898"
---
# <a name="effects-11-interfaces"></a>Interfacce Effects 11

Questa sezione contiene informazioni di riferimento per le interfacce COM (Component Object Model) dell'origine Effects 11.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)<br/>                                                       | Un'interfaccia [**ID3DX11Effect**](id3dx11effect.md) gestisce un set di oggetti di stato, risorse e shader per l'implementazione di un effetto di rendering.<br/>                                                                                                                                                    |
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)<br/>                             | L'interfaccia della variabile Blend accede allo stato di Blend.<br/>                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)<br/>             | Accede a un'istanza della classe.<br/>                                                                                                                                                                                                                                                                         |
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)<br/>                           | Un'interfaccia con buffer costante accede a buffer costanti o a buffer di trama.<br/>                                                                                                                                                                                                                          |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)<br/>               | Un'interfaccia della variabile di stencil Depth accede allo stato di stencil Depth.<br/>                                                                                                                                                                                                                                   |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)<br/>       | Un'interfaccia di profondità-stencil-visualizzazione-variabile accede a una visualizzazione stencil profondità.<br/>                                                                                                                                                                                                                             |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)<br/>                                             | L'interfaccia [**ID3DX11EffectGroup**](id3dx11effectgroup.md) accede a un gruppo di effetti.<br/> La durata di un oggetto [**ID3DX11EffectGroup**](id3dx11effectgroup.md) è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.<br/>                               |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)<br/>                     | Accede a una variabile di interfaccia.<br/>                                                                                                                                                                                                                                                                    |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)<br/>                           | Un'interfaccia della variabile di matrice accede a una matrice.<br/>                                                                                                                                                                                                                                                     |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)<br/>                                               | Un'interfaccia [**ID3DX11EffectPass**](id3dx11effectpass.md) incapsula le assegnazioni di stato all'interno di una tecnica.<br/> La durata di un oggetto [**ID3DX11EffectPass**](id3dx11effectpass.md) è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.<br/>           |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)<br/>                   | Un'interfaccia di rasterizzatore-variabile accede allo stato di rasterizzazione.<br/>                                                                                                                                                                                                                                         |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)<br/>       | Un'interfaccia di visualizzazione della destinazione di rendering accede a una destinazione di rendering.<br/>                                                                                                                                                                                                                                           |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)<br/>                         | Un'interfaccia del campionatore accede allo stato del campionatore.<br/>                                                                                                                                                                                                                                                        |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)<br/>                           | Un'interfaccia con variabile effetto-scalare accede ai valori scalari.<br/>                                                                                                                                                                                                                                        |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)<br/>           | Un'interfaccia shader-Resource accede a una risorsa shader.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)<br/>                           | Un'interfaccia di variabile shader accede a una variabile shader.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)<br/>                           | Un'interfaccia a variabili di stringa accede a una variabile di stringa.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)<br/>                                     | Un'interfaccia [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) è una raccolta di passaggi.<br/> La durata di un oggetto [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.<br/>               |
| [**ID3DX11EffectType**](id3dx11effecttype.md)<br/>                                               | L'interfaccia [**ID3DX11EffectType**](id3dx11effecttype.md) accede alle variabili di effetto per tipo.<br/> La durata di un oggetto [**ID3DX11EffectType**](id3dx11effecttype.md) è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.<br/>                          |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)<br/> | Accede a una visualizzazione di accesso non ordinato.<br/>                                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectVariable**](id3dx11effectvariable.md)<br/>                                       | L'interfaccia [**ID3DX11EffectVariable**](id3dx11effectvariable.md) è la classe di base per tutte le variabili di effetto.<br/> La durata di un oggetto [**ID3DX11EffectVariable**](id3dx11effectvariable.md) è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.<br/> |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)<br/>                           | Un'interfaccia a variabili di vettore accede a un vettore a quattro componenti.<br/>                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento agli effetti 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





