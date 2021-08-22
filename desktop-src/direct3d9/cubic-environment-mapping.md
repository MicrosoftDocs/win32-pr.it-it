---
description: Le mappe dell'ambiente cubico, a volte definite mappe di cubi, sono trame che contengono dati immagine che rappresentano la scena che circonda un oggetto, come se l'oggetto fosse al centro di un cubo.
ms.assetid: 4879d59b-e6d3-4811-ab2c-bcce8f214e1c
title: Mapping dell'ambiente cubico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b02f86528c52c2e8e9376eb92e4452735c2613cc9b7dda08a8a07e8473193ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565340"
---
# <a name="cubic-environment-mapping-direct3d-9"></a>Mapping dell'ambiente cubico (Direct3D 9)

Le mappe dell'ambiente cubico, a volte definite mappe di cubi, sono trame che contengono dati immagine che rappresentano la scena che circonda un oggetto, come se l'oggetto fosse al centro di un cubo. Ogni viso della mappa dell'ambiente cubico copre un campo di visualizzazione a 90 gradi in orizzontale e verticale e sono presenti sei visi per ogni mappa cubo. L'orientamento dei visi è illustrato nella figura seguente.

![Illustrazione di un cubo con assi di coordinate centrali perpendicolari ai visi del cubo](images/cubemap-cube.png)

Ogni faccia del cubo è orientata perpendicolare al piano x/y, y/z o x/z, nello spazio mondiale. La figura seguente mostra come ogni piano corrisponde a un viso.

![Illustrazione di visi del cubo con proiezioni di coordinate dai piani](images/cube-faces.png)

Le mappe dell'ambiente cubico vengono implementate come una serie di oggetti trama. Le applicazioni possono usare immagini statiche per il mapping dell'ambiente cubico oppure possono eseguire il rendering nei visi della mappa del cubo per eseguire il mapping dinamico dell'ambiente. Questa tecnica richiede che le superfici della mappa cubo siano superfici di destinazione di rendering valide, create con il flag D3DUSAGE \_ RENDERTARGET impostato.

I visi di una mappa cubo non devono contenere rendering estremamente dettagliati della scena circostante. Nella maggior parte dei casi, le mappe di ambiente vengono applicate alle superfici curve. Data la quantità di curvatura usata dalla maggior parte delle applicazioni, la distorsione riflettente risultante rende i dettagli estremi della mappa dell'ambiente sprecati in termini di memoria e sovraccarico di rendering.

## <a name="mipmapped-cubic-environment-maps"></a>Ambiente cubico mipmapped Mappe

Le mappe dei cubi possono essere mipmapped. Per creare una mappa del cubo mipmapped, impostare il parametro Levels del [**metodo CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) sul numero di livelli desiderato. È possibile immaginare la topografia di queste superfici, come illustrato nel diagramma seguente.

![Diagramma di una mappa cubo mipmapped con n livelli mip](images/cubemap-mipped.png)

Le applicazioni che creano mappe dell'ambiente cubico con mipmapped possono accedere a ogni viso chiamando il [**metodo GetCubeMapSurface.**](/windows/desktop/api) Iniziare impostando il valore appropriato dal tipo [**enumerato D3DCUBEMAP \_ FACES,**](./d3dcubemap-faces.md) come descritto in Creazione di superfici mappa dell'ambiente [cubico (Direct3D 9).](creating-cubic-environment-map-surfaces.md) Selezionare quindi il livello da recuperare impostando il parametro del livello **GetCubeMapSurface** sul livello mipmap desiderato. Tenere presente che 0 corrisponde all'immagine di primo livello.

## <a name="texture-coordinates-for-cubic-environment-maps"></a>Coordinate di trama per l'ambiente cubico Mappe

Le coordinate di trama che indicizzano una mappa dell'ambiente cubico non sono semplici coordinate di stile u, v, come usato quando vengono applicate trame standard. In realtà, le mappe dell'ambiente cubico non usano affatto le coordinate di trama. Al posto di un set di coordinate di trama, le mappe dell'ambiente cubico richiedono un vettore 3D. È necessario specificare un formato di vertice appropriato. Oltre a specificare al sistema il numero di set di coordinate trame utilizzate dall'applicazione, è necessario fornire informazioni sul numero di elementi presenti in ogni set. Direct3D offre il set di macro [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) a questo scopo. Queste macro accettano un singolo parametro, identificando l'indice del set di coordinate di trama per cui vengono descritte le dimensioni. Nel caso di un vettore 3D, includere il modello di bit creato dalla macro D3DFVF \_ TEXCOORDSIZE3. Nell'esempio di codice seguente viene illustrato l'utilizzo di questa macro.


```
// Create a flexible vertex format descriptor for a vertex that contains
//   a position, normal, and one set of 3D texture coordinates.

DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 | D3DFVF_TEXCOORDSIZE3(0); 
```



In alcuni casi, ad esempio il mapping della luce diffusa, si usa la normale del vertice spazio-fotocamera per il vettore. In altri casi, come il mapping dell'ambiente speculare, si usa un vettore di reflection. Poiché le normali dei vertici trasformate sono ampiamente comprese, le informazioni qui si concentrano sul calcolo di un vettore di reflection.

Il calcolo di un vettore di reflection da solo richiede la comprensione della posizione di ogni vertice e di un vettore dal punto di vista a tale vertice. Direct3D può calcolare automaticamente i vettori di reflection per la geometria. L'uso di questa funzionalità consente di risparmiare memoria perché non è necessario includere le coordinate di trama per la mappa dell'ambiente. Riduce anche la larghezza di banda e, nel caso di un dispositivo HAL T&L, può essere notevolmente più veloce dei calcoli che l'applicazione può eseguire da solo. Per usare questa funzionalità, nella fase della trama che contiene la mappa dell'ambiente cubico impostare lo stato della fase della trama D3DTSS TEXCOORDINDEX su una combinazione del membro \_ D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR [**di D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) e dell'indice di un set di coordinate di trama. In alcune situazioni, ad esempio il mapping della luce diffusa, è possibile usare il membro D3DTSS \_ TCI \_ CAMERASPACENORMAL di **D3DTEXTURESTAGESTATETYPE**, che fa sì che il sistema usi la normale dei vertici trasformata, spazio-fotocamera e vertice come vettore di indirizzamento per la trama. L'indice viene usato solo dal sistema per determinare la modalità di ritorno a capo per la trama.

Nell'esempio di codice seguente viene illustrato come viene usato questo valore.


```
// The m_d3dDevice variable is a valid pointer
// to an IDirect3DDevice9 interface.

// Automatically generate texture coordinates for stage 2.
// This assumes that stage 2 is assigned a cube map.
// Use the wrap mode from the texture coordinate set at index 1.

m_d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX,
                                   D3DTSS_TCI_CAMERASPACEREFLECTIONVECTOR | 1); 
```



Quando si abilita la generazione automatica delle coordinate di trama, il sistema usa una delle due formule per calcolare il vettore di reflection per ogni vertice. Quando lo stato di rendering D3DRS \_ LOCALVIEWER è impostato su **TRUE,** viene usata la formula seguente.

![formula del vettore di reflection (r = 2(exn)n-e)](images/reflection-vector-local.png)

Nella formula precedente R è il vettore di reflection calcolato, E è il vettore posizione-occhio normalizzato e N è la normale del vertice dello spazio della fotocamera.

Quando lo stato di rendering D3DRS \_ LOCALVIEWER è impostato su **FALSE,** il sistema usa la formula seguente.

![formula del vettore di reflection (r = 2nzn-i)](images/reflection-vector-nonlocal.png)

Gli elementi R e N in questa formula sono identici alla formula precedente. <sub>L'elemento</sub> N Z è lo spazio mondo z della normale vertice e I è il vettore (0,0,1) di un punto di vista infinitamente distante. Il sistema usa il vettore di reflection di una delle due formule per selezionare e risolvere il viso appropriato della mappa del cubo.

> [!Note]  
> Nella maggior parte dei casi, le applicazioni devono abilitare la normalizzazione automatica delle normali dei vertici. A tale scopo, impostare D3DRS \_ NORMALIZENORMALS su **TRUE.** Se non si abilita questo stato di rendering, l'aspetto della mappa dell'ambiente sarà drasticamente diverso da quello previsto.

 

Altre informazioni sono contenute nell'argomento seguente.

-   [Creazione di superfici mappa dell'ambiente cubico (Direct3D 9)](creating-cubic-environment-map-surfaces.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping dell'ambiente](environment-mapping.md)
</dt> </dl>

 

 
