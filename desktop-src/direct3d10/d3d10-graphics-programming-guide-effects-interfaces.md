---
description: "Il sistema degli effetti definisce diverse interfacce per la gestione dello stato dell'effetto. Esistono due tipi di interfacce: quelle usate dal runtime per eseguire il rendering di un effetto e delle interfacce di reflection per ottenere e impostare le variabili di effetto."
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Interfacce di sistema effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40b21d98bedaec65550343260e7c52e2df1c302
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126324"
---
# <a name="effect-system-interfaces-direct3d-10"></a>Interfacce di sistema effetto (Direct3D 10)

Il sistema degli effetti definisce diverse interfacce per la gestione dello stato dell'effetto. Esistono due tipi di interfacce: quelle usate dal runtime per eseguire il rendering di un effetto e delle interfacce di reflection per ottenere e impostare le variabili di effetto.

-   [Interfacce di runtime degli effetti](#effect-runtime-interfaces)
-   [Interfacce di Reflection effetto](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Interfacce di runtime degli effetti

Usare le interfacce di runtime per eseguire il rendering di un effetto.



| Interfacce di runtime                                               | Descrizione                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [**Interfaccia ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | Raccolta di una o più tecniche per il rendering.                  |
| [**Interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                 | Interfaccia per l'aggiunta di comportamenti personalizzati durante la lettura dei file di inclusione. |
| [**Interfaccia ID3D10EffectPass**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | Raccolta di assegnazioni di stato.                                   |
| [**Interfaccia ID3D10EffectPool**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | Creare una posizione di memoria per le variabili da condividere tra gli effetti. |
| [**Interfaccia ID3D10EffectTechnique**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | Raccolta di uno o più passaggi.                                  |



 

## <a name="effect-reflection-interfaces"></a>Interfacce di Reflection effetto

La reflection è implementata nel sistema di effetti per supportare la lettura e la scrittura dello stato dell'effetto. Sono disponibili diversi modi per accedere alle variabili di effetto.

### <a name="setting-groups-of-effect-state"></a>Impostazione dei gruppi di stato effetto

Usare queste interfacce per ottenere e impostare un gruppo di stato.



| Interfacce di Reflection                                                                  | Descrizione                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [**Interfaccia ID3D10EffectBlendVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | Ottenere e impostare lo stato di Blend.         |
| [**Interfaccia ID3D10EffectDepthStencilVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | Ottenere e impostare lo stato di stencil Depth. |
| [**Interfaccia ID3D10EffectRasterizerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | Ottiene e imposta lo stato di rasterizzazione.    |
| [**Interfaccia ID3D10EffectSamplerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | Ottiene e imposta lo stato del campionatore.       |



 

### <a name="setting-effect-resources"></a>Impostazione delle risorse degli effetti

Usare queste interfacce per ottenere e impostare le risorse.



| Interfacce di Reflection                                                                          | Descrizione                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**Interfaccia ID3D10EffectConstantBuffer**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Accedere ai dati in un buffer di trama o in un buffer costante. |
| [**Interfaccia ID3D10EffectDepthStencilViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Accedere ai dati in una risorsa di stencil di profondità.            |
| [**Interfaccia ID3D10EffectRenderTargetViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Accedere ai dati in una destinazione di rendering.                     |
| [**Interfaccia ID3D10EffectShaderResourceVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Accedere ai dati in una risorsa shader.                   |



 

### <a name="setting-other-effect-variables"></a>Impostazione di altre variabili di effetto

Usare queste interfacce per ottenere e impostare lo stato in base al tipo di variabile.



| Interfacce di Reflection                                                      | Descrizione                    |
|----------------------------------------------------------------------------|--------------------------------|
| [**Interfaccia ID3D10EffectMatrixVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | Ottenere e impostare una matrice.          |
| [**Interfaccia ID3D10EffectScalarVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | Ottenere e impostare un valore scalare.          |
| [**Interfaccia ID3D10EffectShaderVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | Ottenere e impostare una variabile shader. |
| [**Interfaccia ID3D10EffectStringVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | Ottenere e impostare una stringa.          |
| [**Interfaccia ID3D10EffectType**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | Ottiene un tipo di variabile.           |
| [**Interfaccia ID3D10EffectVectorVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | Ottenere e impostare un vettore.          |



 

Tutte le interfacce di Reflection derivano dall' [**interfaccia ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[Guida di programmazione per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
