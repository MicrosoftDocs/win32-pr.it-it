---
description: Quando Direct3D esegue il rendering di una primitiva, esegue il mapping della primitiva 3D a uno schermo 2D.
ms.assetid: vs|directx_sdk|~\texture_filtering.htm
title: Filtro trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758ee51df65ffa4dddf793db83fe618107886cd4c20497f0e8090373a1415beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291176"
---
# <a name="texture-filtering-direct3d-9"></a>Filtro trame (Direct3D 9)

Quando Direct3D esegue il rendering di una primitiva, esegue il mapping della primitiva 3D a uno schermo 2D. Se la primitiva ha una trama, Direct3D deve usare tale trama per produrre un colore per ogni pixel nell'immagine sottoposta a rendering 2D della primitiva. Per ogni pixel nell'immagine sullo schermo della primitiva, deve ottenere un valore di colore dalla trama. Questo processo è detto filtro delle trame.

Quando viene eseguita un'operazione di filtro della trama, anche la trama usata viene in genere ingrandita o minimiizzata. In altre parole, viene eseguito il mapping a un'immagine primitiva più grande o più piccola di se stessa. L'ingrandimento di una trama può comportare il mapping di molti pixel a un texel. Il risultato può essere un aspetto a blocchi. La minimicazione di una trama spesso significa che un singolo pixel viene mappato a molti texel. L'immagine risultante può essere sfocata o con alias. Per risolvere questi problemi, è necessario eseguire una fusione dei colori texel per ottenere un colore per il pixel.

Direct3D semplifica il processo complesso di filtro delle trame. Offre tre tipi di filtro trame: filtro lineare, filtro anisotropo e filtro mipmap. Se non si seleziona alcun filtro di trama, Direct3D usa una tecnica denominata campionamento del punto più vicino.

Ogni tipo di filtro delle trame presenta vantaggi e svantaggi. Ad esempio, il filtraggio lineare delle trame può produrre bordi irregolari o un aspetto a blocchi nell'immagine finale. Tuttavia, si tratta di un metodo a sovraccarico ridotto dal punto di vista computazionale per il filtraggio delle trame. L'applicazione di filtri con mipmap produce in genere i risultati migliori, soprattutto in combinazione con il filtro anisotropo. Tuttavia, richiede la maggior parte della memoria delle tecniche supportate da Direct3D.

Le applicazioni che usano puntatori a interfaccia di trama devono impostare il metodo di filtro della trama corrente chiamando il [**metodo IDirect3DDevice9::SetSamplerState.**](/windows/desktop/api) Impostare il valore del primo parametro sul numero di indice intero (0-7) della trama per cui si seleziona un metodo di filtro della trama. Passare D3DSAMP \_ MAGFILTER, D3DSAMP MINFILTER o D3DSAMP MIPFILTER per il secondo parametro per impostare il filtro di ingrandimento, minimizzazione o \_ \_ mipmapping. Passare un membro del [**tipo enumerato D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) come valore nel terzo parametro.

Questa sezione presenta i metodi di filtro delle trame supportati da Direct3D. È organizzato negli argomenti seguenti.

-   [Campionamento del punto più vicino (Direct3D 9)](nearest-point-sampling.md)
-   [Filtro trame lineare (Direct3D 9)](linear-texture-filtering.md)
-   [Filtro trame bilineare (Direct3D 9)](bilinear-texture-filtering.md)
-   [Anisotrop Texture Filtering (Direct3D 9)](anisotropic-texture-filtering.md)
-   [Filtro delle trame con mipmap (Direct3D 9)](texture-filtering-with-mipmaps.md)

> [!Note]  
> Anche se gli stati di rendering del filtro delle trame presenti nel tipo enumerato [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) vengono sostituiti dagli stati della fase di trama, [**IDirect3DDevice9::SetRenderState,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)a differenza della versione IDirect3DDevice2, non ha esito negativo se si tenta di usarli. Il sistema esegue invece il mapping degli effetti di questi stati di rendering alla prima fase della cascata multitesto, fase 0. Le applicazioni non devono combinare gli stati di rendering legacy con gli stati della fase di trama corrispondenti, perché possono verificarsi risultati imprevedibili.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
