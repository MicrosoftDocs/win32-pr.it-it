---
title: Introduzione alle trame in Direct3D 11
description: Una risorsa trama è una raccolta strutturata di dati progettati per archiviare texel.
ms.assetid: d745093e-2d51-4d45-a88a-caa0ca58b2ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3bfd19f018ff3f3d9fc8eb1608212a93b4364de2cc24b6213763dfcda4ffe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027901"
---
# <a name="introduction-to-textures-in-direct3d-11"></a>Introduzione alle trame in Direct3D 11

Una risorsa trama è una raccolta strutturata di dati progettati per archiviare texel. Un texel rappresenta l'unità più piccola di una trama che può essere letta o scritta dalla pipeline. A differenza dei buffer, le trame possono essere filtrate in base ai campionatori di trama mentre vengono lette dalle unità shader. Il tipo di trama influisce sul modo in cui viene filtrata la trama. Ogni texel contiene da 1 a 4 componenti, disposti in uno dei formati DXGI definiti dall'enumerazione DXGI \_ FORMAT.

Le trame vengono create come risorsa strutturata con dimensioni note. Tuttavia, ogni trama può essere tipica o senza tipo quando la risorsa viene creata, purché il tipo sia completamente specificato usando una vista quando la trama è associata alla pipeline.

## <a name="texture-types"></a>Tipi di trama

Esistono diversi tipi di trame: 1D, 2D, 3D, ognuna delle quali può essere creata con o senza mipmap. Direct3D 11 supporta anche matrici di trame e trame multicampionato.

-   [Trame 1D](#1d-textures)
-   [Matrici di trame 1D](#1d-texture-arrays)
-   [Trame 2D e matrici di trame 2D](#2d-textures-and-2d-texture-arrays)
-   [Trame 3D](#3d-textures)

### <a name="1d-textures"></a>Trame 1D

Una trama 1D nella forma più semplice contiene dati di trama che possono essere indirizzati con una singola coordinata di trama; può essere visualizzato come matrice di texel, come illustrato nella figura seguente. Le trame 1D sono rappresentate [**dall'interfaccia ID3D11Texture1D.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)

![Illustrazione di una trama 1d](images/d3d10-1d-texture.png)

Ogni texel contiene una serie di componenti di colore a seconda del formato dei dati archiviati. Aggiungendo maggiore complessità, è possibile creare una trama 1D con livelli mipmap, come illustrato nella figura seguente.

![Illustrazione di una trama 1d con livelli mipmap](images/d3d10-resource-texture1d.png)

Un livello mipmap è una trama che è una potenza di due più piccola del livello superiore. Il livello più alto contiene il maggior numero di dettagli, ogni livello successivo è più piccolo. Per un mipmap 1D, il livello più piccolo contiene un texel. Inoltre, i livelli MIP riducono sempre fino a 1:1. Quando vengono generate mipmap per una trama di dimensioni dispari, il livello inferiore successivo è sempre di dimensioni pari (tranne quando il livello più basso raggiunge 1). Ad esempio, il diagramma illustra una trama 5x1 il cui livello più basso successivo è una trama 2x1, il cui livello mip successivo (e ultimo) è una trama di dimensioni 1x1. I livelli sono identificati da un indice denominato LOD (livello di dettaglio) usato per accedere alla trama più piccola durante il rendering di una geometria non così vicina alla fotocamera.

### <a name="1d-texture-arrays"></a>Matrici di trame 1D

Direct3D 11 supporta anche matrici di trame. Una matrice di trame 1D è rappresentata anche [**dall'interfaccia ID3D11Texture1D.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) Una matrice di trame 1D è concettualmente simile alla figura seguente.

![Illustrazione di una matrice di trame 1d](images/d3d10-resource-texture1darray.png)

Questa matrice di trame contiene tre trame. Ognuna delle tre trame ha una larghezza di trama di 5 (ovvero il numero di elementi nel primo livello). Ogni trama contiene anche un mipmap a 3 livelli.

Tutte le matrici di trame in Direct3D sono una matrice omogenea di trame; Ciò significa che ogni trama in una matrice di trame deve avere lo stesso formato e le stesse dimensioni dei dati (inclusi la larghezza della trama e il numero di livelli di mipmap). È possibile creare matrici di trame di dimensioni diverse, purché tutte le trame in ogni matrice corrispondano alle dimensioni.

### <a name="2d-textures-and-2d-texture-arrays"></a>Trame 2D e matrici di trame 2D

Una risorsa Texture2D contiene una griglia 2D di texel. Ogni texel è indirizzabile da un vettore u, v. Poiché si tratta di una risorsa trama, può contenere livelli mipmap e sottorisorse. Le trame 2D sono rappresentate [**dall'interfaccia ID3D11Texture2D.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) Una risorsa di trama 2D completamente popolata è simile alla figura seguente.

![Illustrazione di una risorsa trama 2d](images/d3d10-resource-texture2d.png)

Questa risorsa di trama contiene una singola trama 3x5 con tre livelli mipmap.

Una risorsa matrice di trame 2D è una matrice omogenea di trame 2D. ovvero ogni trama ha lo stesso formato e dimensioni dei dati (inclusi i livelli mipmap). Una matrice di trame 2D è rappresentata anche [**dall'interfaccia ID3D11Texture2D.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) Ha un layout simile a quello della matrice di trame 1D, ad eccezione del fatto che le trame contengono ora dati 2D, come illustrato nella figura seguente.

![Illustrazione di una matrice di trame 2d](images/d3d10-resource-texture2darray.png)

Questa matrice di trame contiene tre trame; ogni trama è 3x5 con due livelli mipmap.

### <a name="using-a-2d-texture-array-as-a-texture-cube"></a>Uso di una matrice di trame 2D come cubo di trama

Un cubo trama è una matrice di trame 2D che contiene 6 trame, una per ogni viso del cubo. Un cubo di trama completamente popolato è simile alla figura seguente.

![Illustrazione di una matrice di trame 2d che rappresentano un cubo di trame](images/d3d10-resource-texturecube.png)

Una matrice di trame 2D che contiene 6 trame può essere letta dall'interno degli shader con le funzioni intrinseche della mappa del cubo, dopo essere stata associata alla pipeline con una vista trame cubo. I cubi di trama vengono indirizzati dallo shader con un vettore 3D che punta dal centro del cubo di trama.

> [!Note]  
> I dispositivi creati con [**10 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) livello di funzionalità e superiore possono supportare matrici di cubi di trama in cui il numero di trame è uguale al numero di cubi di trama in una matrice per sei volte. I dispositivi creati con livello di funzionalità [**\_ 10 0**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) supportano solo un singolo cubo di trama di sei visi. Direct3D 11 non supporta inoltre mappe di cubi parziali.

 

### <a name="3d-textures"></a>Trame 3D

Una risorsa trama 3D (nota anche come trama di volume) contiene un volume 3D di texel. Poiché si tratta di una risorsa trama, può contenere livelli mipmap. Le trame 3D sono rappresentate [**dall'interfaccia ID3D11Texture3D.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) Una trama 3D completamente popolata è simile alla figura seguente.

![Illustrazione di una risorsa trama 3D](images/d3d10-resource-texture3d.png)

Quando una sezione mipmap di trama 3D viene associata come output di destinazione di rendering (con una visualizzazione di destinazione di rendering), la trama 3D si comporta in modo identico a una matrice di trame 2D con n sezioni. La sezione di rendering specifica viene scelta dalla fase geometry-shader, dichiarando un componente scalare dei dati di output come valore di sistema \_ RenderTargetArrayIndex SV.

Non esiste alcun concetto di matrice di trame 3D. pertanto una sottorisorsa di trama 3D è un singolo livello mipmap.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




