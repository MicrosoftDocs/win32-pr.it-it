---
description: 'Questa sezione contiene informazioni sulle interfacce del sistema di effetti seguenti:'
ms.assetid: ebe0afc7-6261-4c96-a54e-9b491e240c03
title: Interfacce degli effetti (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07e6ecf45f4ef052c7d576849a55d00ef0f877dde7c41fa5dc80b7592761325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303974"
---
# <a name="effect-interfaces-direct3d-10"></a>Interfacce degli effetti (Direct3D 10)

Questa sezione contiene informazioni sulle interfacce del sistema di effetti seguenti:



| Interfacce                                                                                     | Descrizione                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**Interfaccia ID3D10EffectBlendVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)                       | Accede allo stato blend.                                            |
| [**Interfaccia ID3D10EffectConstantBuffer**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Accede a un buffer di trama o a un constant-buffer.                  |
| [**Interfaccia ID3D10EffectDepthStencilVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable)         | Accede allo stato depth-stencil.                                    |
| [**Interfaccia ID3D10EffectDepthStencilViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Accede a una visualizzazione stencil di profondità.                                   |
| [**Interfaccia ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                                                 | Incapsula lo stato della pipeline in una o più tecniche di rendering. |
| [**Interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                                               | Metodi implementati dall'utente per la lettura dei file di inclusione.              |
| [**Interfaccia ID3D10EffectMatrixVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable)                     | Accede a una matrice.                                               |
| [**Interfaccia ID3D10EffectPass**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)                                         | Incapsula lo stato dell'effetto in un passaggio.                             |
| [**Interfaccia ID3D10EffectPool**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)                                         | Identifica le variabili di effetto condiviso.                              |
| [**Interfaccia ID3D10EffectRasterizerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)             | Accede allo stato di rasterizzazione.                                       |
| [**Interfaccia ID3D10EffectRenderTargetViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Accede a una destinazione di rendering.                                        |
| [**Interfaccia ID3D10EffectSamplerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)                   | Accede allo stato del campionatore.                                          |
| [**Interfaccia ID3D10EffectScalarVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable)                     | Accede a una variabile scalare.                                      |
| [**Interfaccia ID3D10EffectShaderResourceVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Accede a una risorsa shader.                                      |
| [**Interfaccia ID3D10EffectShaderVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable)                     | Accede a una variabile shader.                                      |
| [**Interfaccia ID3D10EffectStringVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable)                     | Accede a una stringa.                                               |
| [**Interfaccia ID3D10EffectTechnique**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique)                               | Incapsula uno o più passaggi.                                 |
| [**Interfaccia ID3D10EffectType**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                                         | Implementa metodi per l'accesso alle variabili di effetto.               |
| [**Interfaccia ID3D10EffectVectorVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable)                     | Accede a un vettore.                                               |



 

Esistono due tipi di interfacce nel framework degli effetti: interfacce di rendering per il rendering di un effetto e interfacce di reflection per ottenere e impostare le variabili di effetto con l'API. Tutte le interfacce di reflection derivano [**dall'interfaccia ID3D10EffectVariable.**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sull'effetto](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 
