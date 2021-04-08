---
description: 'Questa sezione contiene informazioni sulle seguenti interfacce del sistema di effetti:'
ms.assetid: ebe0afc7-6261-4c96-a54e-9b491e240c03
title: Interfacce degli effetti (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1946e7b9e3711bf2d79c0876efca1c533e0ff4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748015"
---
# <a name="effect-interfaces-direct3d-10"></a>Interfacce degli effetti (Direct3D 10)

Questa sezione contiene informazioni sulle seguenti interfacce del sistema di effetti:



| Interfacce                                                                                     | Descrizione                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**Interfaccia ID3D10EffectBlendVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)                       | Accede allo stato di Blend.                                            |
| [**Interfaccia ID3D10EffectConstantBuffer**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Accede a un buffer di trama o a un buffer di costanti.                  |
| [**Interfaccia ID3D10EffectDepthStencilVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable)         | Accede allo stato dello stencil di profondità.                                    |
| [**Interfaccia ID3D10EffectDepthStencilViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Accede a una visualizzazione stencil profondità.                                   |
| [**Interfaccia ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                                                 | Incapsula lo stato della pipeline in una o più tecniche di rendering. |
| [**Interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                                               | Metodi implementati dall'utente per la lettura dei file di inclusione.              |
| [**Interfaccia ID3D10EffectMatrixVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable)                     | Accede a una matrice.                                               |
| [**Interfaccia ID3D10EffectPass**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)                                         | Incapsula lo stato dell'effetto in un passaggio.                             |
| [**Interfaccia ID3D10EffectPool**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)                                         | Identifica le variabili con effetto condiviso.                              |
| [**Interfaccia ID3D10EffectRasterizerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)             | Accede allo stato di rasterizzazione.                                       |
| [**Interfaccia ID3D10EffectRenderTargetViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Accede a una destinazione di rendering.                                        |
| [**Interfaccia ID3D10EffectSamplerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)                   | Accede allo stato del campionatore.                                          |
| [**Interfaccia ID3D10EffectScalarVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable)                     | Accede a una variabile scalare.                                      |
| [**Interfaccia ID3D10EffectShaderResourceVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Accede a una risorsa dello shader.                                      |
| [**Interfaccia ID3D10EffectShaderVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable)                     | Accede a una variabile shader.                                      |
| [**Interfaccia ID3D10EffectStringVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable)                     | Accede a una stringa.                                               |
| [**Interfaccia ID3D10EffectTechnique**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique)                               | Incapsula uno o più passaggi.                                 |
| [**Interfaccia ID3D10EffectType**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                                         | Implementa i metodi per l'accesso alle variabili di effetto.               |
| [**Interfaccia ID3D10EffectVectorVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable)                     | Accede a un vettore.                                               |



 

Nel Framework degli effetti sono disponibili due tipi di interfacce: il rendering delle interfacce per il rendering di un effetto e delle interfacce di reflection per ottenere e impostare le variabili di effetto con l'API. Tutte le interfacce di Reflection derivano dall' [**interfaccia ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento a effetti](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 
