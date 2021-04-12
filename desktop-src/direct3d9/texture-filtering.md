---
description: Quando Direct3D esegue il rendering di una primitiva, esegue il mapping della primitiva 3D su una schermata 2D.
ms.assetid: vs|directx_sdk|~\texture_filtering.htm
title: Filtraggio delle trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faeeb83e1a3bc7fc03534771b15b6076aeb48f8c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482037"
---
# <a name="texture-filtering-direct3d-9"></a>Filtraggio delle trame (Direct3D 9)

Quando Direct3D esegue il rendering di una primitiva, esegue il mapping della primitiva 3D su una schermata 2D. Se la primitiva ha una trama, Direct3D deve usare tale trama per produrre un colore per ogni pixel nell'immagine di rendering 2D della primitiva. Per ogni pixel nell'immagine su schermo della primitiva, deve ottenere un valore di colore dalla trama. Questo processo è denominato filtraggio della trama.

Quando viene eseguita un'operazione di filtro di trama, viene in genere ingrandita anche la trama utilizzata in minimizzati. In altre parole, viene eseguito il mapping in un'immagine primitiva di dimensioni maggiori o minori di se stessa. L'ingrandimento di una trama può causare il mapping di molti pixel a un Texel. Il risultato può essere un aspetto robusto. Minification di una trama spesso significa che viene eseguito il mapping di un singolo pixel a molti Texel. L'immagine risultante può essere sfocata o con alias. Per risolvere questi problemi, è necessario eseguire alcune fusioni dei colori Texel per arrivare a un colore per il pixel.

Direct3D semplifica il processo complesso di filtraggio delle trame. Sono disponibili tre tipi di filtro di trama: filtro lineare, filtro anisotropico e filtro mipmap. Se non si seleziona alcun filtro di trama, Direct3D usa una tecnica denominata campionamento del punto più vicino.

Ogni tipo di filtro di trama presenta vantaggi e svantaggi. Ad esempio, l'applicazione di filtri di trama lineare può produrre spigoli irregolari o un aspetto robusto nell'immagine finale. Tuttavia, si tratta di un metodo con sovraccarico computazionale per il filtraggio delle trame. L'applicazione di filtri con mipmap in genere produce i risultati migliori, specialmente in combinazione con il filtro anisotropico. Tuttavia, richiede la maggior parte della memoria delle tecniche supportate da Direct3D.

Le applicazioni che usano puntatori a interfaccia di trama devono impostare il metodo di filtro della trama corrente chiamando il metodo [**IDirect3DDevice9:: SetSamplerState**](/windows/desktop/api) . Impostare il valore del primo parametro sul numero di indice Integer (0-7) della trama per cui si seleziona un metodo di filtro della trama. Passare D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER o D3DSAMP \_ MIPFILTER per il secondo parametro per impostare il filtro di ingrandimento, minification o mapping MIP. Passare un membro del tipo enumerato [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) come valore nel terzo parametro.

In questa sezione vengono illustrati i metodi di filtro della trama supportati da Direct3D. Sono organizzati negli argomenti seguenti.

-   [Campionamento del punto più vicino (Direct3D 9)](nearest-point-sampling.md)
-   [Filtro di trama lineare (Direct3D 9)](linear-texture-filtering.md)
-   [Filtraggio bilineare della trama (Direct3D 9)](bilinear-texture-filtering.md)
-   [Filtro di trama anisotropico (Direct3D 9)](anisotropic-texture-filtering.md)
-   [Filtraggio delle trame con mipmap (Direct3D 9)](texture-filtering-with-mipmaps.md)

> [!Note]  
> Sebbene gli Stati di rendering del filtro della trama presenti nel tipo enumerato [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) siano sostituiti da Stati della fase trama, [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate), invece della versione IDirect3DDevice2, non ha esito negativo se si tenta di usarli. Al contrario, il sistema esegue il mapping degli effetti di questi stati di rendering alla prima fase in Cascade multitexture, fase 0. Le applicazioni non devono combinare gli Stati di rendering legacy con gli Stati della fase di trama corrispondenti, perché possono verificarsi risultati imprevedibili.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
