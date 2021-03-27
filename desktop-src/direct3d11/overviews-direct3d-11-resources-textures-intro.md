---
title: Introduzione alle trame in Direct3D 11
description: Una risorsa di trama è una raccolta strutturata di dati progettati per archiviare Texel.
ms.assetid: d745093e-2d51-4d45-a88a-caa0ca58b2ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fcafdfb9caf53a27e60956c8182ae3ef95008e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856422"
---
# <a name="introduction-to-textures-in-direct3d-11"></a>Introduzione alle trame in Direct3D 11

Una risorsa di trama è una raccolta strutturata di dati progettati per archiviare Texel. Un Texel rappresenta l'unità più piccola di una trama che può essere letta o scritta dalla pipeline. A differenza dei buffer, le trame possono essere filtrate in base ai Sampler di trama Man mano che vengono lette dalle unità dello shader. Il tipo di trama influisca sul modo in cui la trama viene filtrata. Ogni Texel contiene da 1 a 4 componenti, disposti in uno dei formati DXGI definiti dall'enumerazione del \_ formato dxgi.

Le trame vengono create come una risorsa strutturata con una dimensione nota. Tuttavia, ogni trama può essere tipizzata o senza tipo quando la risorsa viene creata purché il tipo venga specificato completamente usando una visualizzazione quando la trama è associata alla pipeline.

## <a name="texture-types"></a>Tipi di trama

Sono disponibili diversi tipi di trame: 1D, 2D, 3D, ciascuna delle quali può essere creata con o senza mipmap. Direct3D 11 supporta anche matrici di trame e trame multicampionate.

-   [Trame 1D](#1d-textures)
-   [Matrici di trama 1D](#1d-texture-arrays)
-   [Trame 2D e matrici di trame 2D](#2d-textures-and-2d-texture-arrays)
-   [Trame 3D](#3d-textures)

### <a name="1d-textures"></a>Trame 1D

Una trama 1D nella sua forma più semplice contiene dati di trama che possono essere risolti con una singola coordinata di trama; può essere visualizzato come matrice di Texel, come illustrato nella figura seguente. le trame 1D sono rappresentate dall'interfaccia [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) .

![illustrazione di una trama 1D](images/d3d10-1d-texture.png)

Ogni Texel contiene diversi componenti colore a seconda del formato dei dati archiviati. Aggiungendo maggiore complessità, è possibile creare una trama 1D con livelli mipmap, come illustrato nella figura seguente.

![illustrazione di una trama 1D con livelli mipmap](images/d3d10-resource-texture1d.png)

Un livello mipmap è una trama che è una potenza di due dimensioni inferiori al livello superiore. Il livello superiore contiene il maggior numero di dettagli, ogni livello successivo è inferiore. Per un mipmap 1D, il livello più piccolo contiene un Texel. Inoltre, i livelli MIP riducono sempre fino a 1:1. Quando vengono generati mipmap per una trama di dimensioni dispari, il livello inferiore successivo è sempre pari alla dimensione (tranne quando il livello più basso raggiunge 1). Il diagramma illustra ad esempio una trama 5x1 il cui livello più basso successivo è una trama 2x1, il cui livello successivo (e ultimo) MIP è una trama di dimensioni 1x1. I livelli sono identificati da un indice denominato LOD (livello di dettaglio) che viene usato per accedere alla trama più piccola durante il rendering della geometria che non si avvicina alla fotocamera.

### <a name="1d-texture-arrays"></a>Matrici di trama 1D

Direct3D 11 supporta inoltre matrici di trame. Una matrice di trama 1D è inoltre rappresentata dall'interfaccia [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) . Una matrice di trame 1D sembra concettualmente simile alla figura seguente.

![illustrazione di una matrice di trame 1D](images/d3d10-resource-texture1darray.png)

Questa matrice di trame contiene tre trame. Ognuna delle tre trame ha una larghezza di trama pari a 5, ovvero il numero di elementi nel primo livello. Ogni trama contiene anche un mipmap a 3 livelli.

Tutte le matrici di trama in Direct3D sono una matrice omogenea di trame; Ciò significa che ogni trama in una matrice di trame deve avere lo stesso formato e la stessa dimensione dei dati (inclusa la larghezza della trama e il numero di livelli di mipmap). È possibile creare matrici di trama di dimensioni diverse, purché tutte le trame in ogni matrice corrispondano alle dimensioni.

### <a name="2d-textures-and-2d-texture-arrays"></a>Trame 2D e matrici di trame 2D

Una risorsa Texture2D contiene una griglia 2D di Texel. Ogni Texel è indirizzabile da un vettore u, v. Poiché si tratta di una risorsa di trama, può contenere livelli mipmap e sottorisorse. le trame 2D sono rappresentate dall'interfaccia [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) . Una risorsa di trama 2D completamente popolata ha un aspetto simile a quello illustrato nella figura seguente.

![illustrazione di una risorsa di trama 2D](images/d3d10-resource-texture2d.png)

Questa risorsa trama contiene una singola trama 3x5 con tre livelli di mipmap.

Una risorsa di matrice di trama 2D è una matrice omogenea di trame 2D. ovvero ogni trama presenta lo stesso formato di dati e le stesse dimensioni (inclusi i livelli mipmap). Una matrice di trame 2D è inoltre rappresentata dall'interfaccia [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) . Ha un layout simile a quello della matrice di trama 1D, ad eccezione del fatto che le trame ora contengono dati 2D, come illustrato nella figura seguente.

![illustrazione di una matrice di trame 2D](images/d3d10-resource-texture2darray.png)

Questa matrice di trame contiene tre trame; ogni trama è 3x5 con due livelli di mipmap.

### <a name="using-a-2d-texture-array-as-a-texture-cube"></a>Uso di una matrice di trame 2D come cubo di trama

Un cubo di trama è una matrice di trame 2D che contiene 6 trame, una per ogni faccia del cubo. Un cubo di trama completamente popolato ha un aspetto simile a quello illustrato nella figura seguente.

![illustrazione di una matrice di trame 2D che rappresentano un cubo di trama](images/d3d10-resource-texturecube.png)

Una matrice di trame 2D che contiene 6 trame può essere letta dall'interno degli shader con le funzioni intrinseche della mappa del cubo, dopo che sono state associate alla pipeline con una visualizzazione di trama del cubo. I cubi di trama sono indirizzati dallo shader con un vettore 3D che punta al centro del cubo di trama.

> [!Note]  
> I dispositivi creati con un [**\_ livello di funzionalità di 10 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) e versioni successive sono in grado di supportare matrici di cubi di trama in cui il numero di trame è uguale al numero di cubi di trama in una matrice per sei. I dispositivi creati con un [**\_ livello di funzionalità di 10 0**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) supportano solo un singolo cubo di trama di sei visi. Inoltre, Direct3D 11 non supporta CubeMaps parziali.

 

### <a name="3d-textures"></a>Trame 3D

Una risorsa di trama 3D, nota anche come trama del volume, contiene un volume 3D di Texel. Poiché si tratta di una risorsa di trama, può contenere livelli mipmap. le trame 3D sono rappresentate dall'interfaccia [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) . Una trama 3D completamente popolata ha un aspetto simile a quello illustrato nella figura seguente.

![illustrazione di una risorsa di trama 3D](images/d3d10-resource-texture3d.png)

Quando una sezione mipmap trama 3D viene associata come output della destinazione di rendering (con una visualizzazione di destinazione del rendering), la trama 3D si comporta in modo identico a una matrice di trama 2D con n sezioni. La sezione di rendering specifica viene scelta dalla fase geometry-shader, dichiarando un componente scalare dei dati di output come \_ valore di sistema RENDERTARGETARRAYINDEX SV.

Non esiste alcun concetto di matrice di trama 3D; una sottorisorsa di trama 3D è quindi un singolo livello di mipmap.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




