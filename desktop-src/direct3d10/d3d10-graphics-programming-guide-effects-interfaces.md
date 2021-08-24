---
description: "Il sistema di effetti definisce diverse interfacce per la gestione dello stato dell'effetto. Esistono due tipi di interfacce: quelle usate dal runtime per eseguire il rendering di un effetto e le interfacce di reflection per ottenere e impostare le variabili di effetto."
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Interfacce di sistema degli effetti (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5d640b31d0d1db9ac9b58ed166b45acff762b30edc0e71f1d7138b5818b3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128393"
---
# <a name="effect-system-interfaces-direct3d-10"></a>Interfacce di sistema degli effetti (Direct3D 10)

Il sistema di effetti definisce diverse interfacce per la gestione dello stato dell'effetto. Esistono due tipi di interfacce: quelle usate dal runtime per eseguire il rendering di un effetto e le interfacce di reflection per ottenere e impostare le variabili di effetto.

-   [Interfacce di runtime degli effetti](#effect-runtime-interfaces)
-   [Interfacce di reflection degli effetti](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Interfacce di runtime degli effetti

Usare le interfacce di runtime per eseguire il rendering di un effetto.



| Interfacce di runtime                                               | Descrizione                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [**Interfaccia ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | Raccolta di una o più tecniche per il rendering.                  |
| [**Interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                 | Interfaccia per l'aggiunta di comportamenti personalizzati durante la lettura dei file di inclusione. |
| [**Interfaccia ID3D10EffectPass**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | Raccolta di assegnazioni di stato.                                   |
| [**Interfaccia ID3D10EffectPool**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | Creare un percorso di memoria per le variabili da condividere tra gli effetti. |
| [**Interfaccia ID3D10EffectTechnique**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | Raccolta di uno o più passaggi.                                  |



 

## <a name="effect-reflection-interfaces"></a>Interfacce di reflection degli effetti

La reflection viene implementata nel sistema degli effetti per supportare lo stato dell'effetto di lettura e scrittura. Esistono diversi modi per accedere alle variabili degli effetti.

### <a name="setting-groups-of-effect-state"></a>Impostazione di gruppi di stato dell'effetto

Usare queste interfacce per ottenere e impostare un gruppo di stato.



| Interfacce di reflection                                                                  | Descrizione                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [**Interfaccia ID3D10EffectBlendVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | Ottiene e imposta lo stato di fusione.         |
| [**Interfaccia ID3D10EffectDepthStencilVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | Ottiene e imposta lo stato depth-stencil. |
| [**Interfaccia ID3D10EffectRasterizerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | Ottenere e impostare lo stato del rasterizzatore.    |
| [**Interfaccia ID3D10EffectSamplerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | Ottenere e impostare lo stato del campionatore.       |



 

### <a name="setting-effect-resources"></a>Impostazione delle risorse degli effetti

Usare queste interfacce per ottenere e impostare le risorse.



| Interfacce di reflection                                                                          | Descrizione                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**Interfaccia ID3D10EffectConstantBuffer**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Accedere ai dati in un buffer di trama o in un buffer costante. |
| [**Interfaccia ID3D10EffectDepthStencilViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Accedere ai dati in una risorsa depth-stencil.            |
| [**Interfaccia ID3D10EffectRenderTargetViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Accedere ai dati in una destinazione di rendering.                     |
| [**Interfaccia ID3D10EffectShaderResourceVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Accedere ai dati in una risorsa shader.                   |



 

### <a name="setting-other-effect-variables"></a>Impostazione di altre variabili degli effetti

Usare queste interfacce per ottenere e impostare lo stato in base al tipo di variabile.



| Interfacce di reflection                                                      | Descrizione                    |
|----------------------------------------------------------------------------|--------------------------------|
| [**Interfaccia ID3D10EffectMatrixVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | Ottenere e impostare una matrice.          |
| [**Interfaccia ID3D10EffectScalarVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | Ottenere e impostare un valore scalare.          |
| [**Interfaccia ID3D10EffectShaderVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | Ottenere e impostare una variabile shader. |
| [**Interfaccia ID3D10EffectStringVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | Ottenere e impostare una stringa.          |
| [**Interfaccia ID3D10EffectType**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | Ottiene un tipo di variabile.           |
| [**Interfaccia ID3D10EffectVectorVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | Ottenere e impostare un vettore.          |



 

Tutte le interfacce di reflection derivano da [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[Guida per programmatori per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
