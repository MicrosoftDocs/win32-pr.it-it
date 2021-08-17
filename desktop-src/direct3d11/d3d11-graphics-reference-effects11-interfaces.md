---
title: Interfacce di Effects 11
description: Questa sezione contiene informazioni di riferimento per le interfacce COM (Component Object Model) dell'origine Effects 11.
ms.assetid: 1b997513-73f7-423a-8af3-1c9fa0d2f469
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b20713f5a40b2d8b85edb92166b7e64af18fefee62e5267adcffa25356c6f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118537703"
---
# <a name="effects-11-interfaces"></a>Interfacce di Effects 11

Questa sezione contiene informazioni di riferimento per le interfacce COM (Component Object Model) dell'origine Effects 11.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)<br/>                                                       | [**Un'interfaccia ID3DX11Effect**](id3dx11effect.md) gestisce un set di oggetti di stato, risorse e shader per l'implementazione di un effetto di rendering.<br/>                                                                                                                                                    |
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)<br/>                             | L'interfaccia blend-variable accede allo stato di blend.<br/>                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)<br/>             | Accede a un'istanza della classe .<br/>                                                                                                                                                                                                                                                                         |
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)<br/>                           | Un'interfaccia constant-buffer accede ai buffer costanti o ai buffer di trama.<br/>                                                                                                                                                                                                                          |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)<br/>               | Un'interfaccia depth-stencil-variable accede allo stato depth-stencil.<br/>                                                                                                                                                                                                                                   |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)<br/>       | Un'interfaccia depth-stencil-view-variable accede a una visualizzazione depth-stencil.<br/>                                                                                                                                                                                                                             |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)<br/>                                             | [**L'interfaccia ID3DX11EffectGroup**](id3dx11effectgroup.md) accede a un gruppo Effect.<br/> La durata di un [**oggetto ID3DX11EffectGroup**](id3dx11effectgroup.md) è uguale alla durata dell'oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.<br/>                               |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)<br/>                     | Accede a una variabile di interfaccia.<br/>                                                                                                                                                                                                                                                                    |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)<br/>                           | Un'interfaccia matrice-variabile accede a una matrice.<br/>                                                                                                                                                                                                                                                     |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)<br/>                                               | [**Un'interfaccia ID3DX11EffectPass**](id3dx11effectpass.md) incapsula le assegnazioni di stato all'interno di una tecnica.<br/> La durata di un [**oggetto ID3DX11EffectPass**](id3dx11effectpass.md) è uguale alla durata dell'oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.<br/>           |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)<br/>                   | Un'interfaccia rasterizer-variable accede allo stato del rasterizzatore.<br/>                                                                                                                                                                                                                                         |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)<br/>       | Un'interfaccia render-target-view accede a una destinazione di rendering.<br/>                                                                                                                                                                                                                                           |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)<br/>                         | Un'interfaccia del campionatore accede allo stato del campionatore.<br/>                                                                                                                                                                                                                                                        |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)<br/>                           | Un'interfaccia effect-scalar-variable accede ai valori scalari.<br/>                                                                                                                                                                                                                                        |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)<br/>           | Un'interfaccia shader-risorsa accede a una risorsa shader.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)<br/>                           | Un'interfaccia di variabile shader accede a una variabile shader.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)<br/>                           | Un'interfaccia stringa-variabile accede a una variabile stringa.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)<br/>                                     | [**Un'interfaccia ID3DX11EffectTechnique**](id3dx11effecttechnique.md) è una raccolta di passaggi.<br/> La durata di un [**oggetto ID3DX11EffectTechnique**](id3dx11effecttechnique.md) è uguale alla durata dell'oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.<br/>               |
| [**ID3DX11EffectType**](id3dx11effecttype.md)<br/>                                               | [**L'interfaccia ID3DX11EffectType**](id3dx11effecttype.md) accede alle variabili degli effetti in base al tipo.<br/> La durata di un [**oggetto ID3DX11EffectType**](id3dx11effecttype.md) è uguale alla durata dell'oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.<br/>                          |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)<br/> | Accede a una visualizzazione di accesso non ordinata.<br/>                                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectVariable**](id3dx11effectvariable.md)<br/>                                       | [**L'interfaccia ID3DX11EffectVariable**](id3dx11effectvariable.md) è la classe di base per tutte le variabili di effetto.<br/> La durata di un [**oggetto ID3DX11EffectVariable**](id3dx11effectvariable.md) è uguale alla durata dell'oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.<br/> |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)<br/>                           | Un'interfaccia a variabile di vettore accede a un vettore a quattro componenti.<br/>                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su Effects 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





