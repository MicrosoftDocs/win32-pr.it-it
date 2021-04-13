---
description: Mappe per l'ambiente cubico, a volte denominate mappe cubo, sono trame che contengono dati di immagine che rappresentano la scena che circonda un oggetto, come se l'oggetto fosse al centro di un cubo.
ms.assetid: 4879d59b-e6d3-4811-ab2c-bcce8f214e1c
title: Mapping dell'ambiente cubico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecac83db067224195883485bcbd282aa82ae4b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401504"
---
# <a name="cubic-environment-mapping-direct3d-9"></a>Mapping dell'ambiente cubico (Direct3D 9)

Mappe per l'ambiente cubico, a volte denominate mappe cubo, sono trame che contengono dati di immagine che rappresentano la scena che circonda un oggetto, come se l'oggetto fosse al centro di un cubo. Ogni faccia della mappa dell'ambiente cubica copre un campo di visualizzazione di 90 gradi in orizzontale e verticale e sono presenti sei visi per ogni mappa del cubo. L'orientamento dei visi è illustrato nella figura seguente.

![illustrazione di un cubo con assi di coordinate centrali perpendicolari ai visi dei cubi](images/cubemap-cube.png)

Ogni faccia del cubo è orientata perpendicolarmente al piano x/y, y/z o x/z, nello spazio globale. Nella figura seguente viene illustrato il modo in cui ogni piano corrisponde a una faccia.

![illustrazione dei volti dei cubi con proiezioni di coordinate da piani](images/cube-faces.png)

Le mappe dell'ambiente cubico sono implementate come una serie di oggetti texture. Le applicazioni possono usare immagini statiche per il mapping di ambienti cubici o eseguire il rendering nei visi della mappa del cubo per eseguire il mapping dell'ambiente dinamico. Questa tecnica richiede che le superfici della mappa del cubo siano superfici di destinazione di rendering valide, create con il \_ flag D3DUSAGE RENDERTARGET impostato.

I visi di una mappa cubo non devono contenere rendering estremamente dettagliati della scena circostante. Nella maggior parte dei casi, le mappe dell'ambiente vengono applicate alle superfici curve. Dato il livello di curvatura usato dalla maggior parte delle applicazioni, la distorsione riflessiva risultante rende estremamente dettagliati gli sprechi della mappa dell'ambiente in termini di memoria e sovraccarico di rendering.

## <a name="mipmapped-cubic-environment-maps"></a>Mappe dell'ambiente cubico mipmap

Le mappe del cubo possono essere mipmap. Per creare una mappa del cubo mipmap, impostare il parametro Levels del metodo [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) sul numero di livelli desiderato. È possibile prevedere la topografia di queste superfici, come illustrato nella figura seguente.

![diagramma di una mappa del cubo mipmap con n livelli MIP](images/cubemap-mipped.png)

Le applicazioni che creano mappe dell'ambiente cubico mipmap possono accedere a ogni volto chiamando il metodo [**GetCubeMapSurface**](/windows/desktop/api) . Iniziare impostando il valore appropriato dal tipo enumerato [**D3DCUBEMAP \_ Faces**](./d3dcubemap-faces.md) , come descritto in [creazione di superfici della mappa dell'ambiente cubico (Direct3D 9)](creating-cubic-environment-map-surfaces.md). Selezionare quindi il livello da recuperare impostando il parametro **GetCubeMapSurface** Level sul livello mipmap desiderato. Tenere presente che 0 corrisponde all'immagine di primo livello.

## <a name="texture-coordinates-for-cubic-environment-maps"></a>Coordinate di trama per le mappe dell'ambiente cubico

Le coordinate di trama che indicizzano una mappa dell'ambiente cubi non sono semplici coordinate di stile u, v, come usate quando si applicano trame standard. Di fatto, le mappe dell'ambiente cubico non usano affatto le coordinate di trama. Al posto di un set di coordinate di trama, le mappe dell'ambiente cubico richiedono un vettore 3D. È necessario prestare attenzione a specificare un formato di vertice appropriato. Oltre a comunicare al sistema il numero di set di coordinate di trama utilizzate dall'applicazione, è necessario fornire informazioni sul numero di elementi in ogni set. Direct3D offre il set di macro [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) per questo scopo. Queste macro accettano un solo parametro, identificando l'indice del set di coordinate di trama per il quale viene descritta la dimensione. Nel caso di un vettore 3D, è necessario includere lo schema di bit creato dalla \_ macro TEXCOORDSIZE3 di D3DFVF. Nell'esempio di codice seguente viene illustrata la modalità di utilizzo di questa macro.


```
// Create a flexible vertex format descriptor for a vertex that contains
//   a position, normal, and one set of 3D texture coordinates.

DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 | D3DFVF_TEXCOORDSIZE3(0); 
```



In alcuni casi, ad esempio il mapping della luce diffusa, si usa la normalità dei vertici dello spazio della fotocamera per il vettore. In altri casi, come il mapping dell'ambiente speculare, si usa un vettore di Reflection. Poiché le normali Vertex trasformate sono ampiamente comprese, le informazioni in questo argomento si concentrano sul calcolo di un vettore di Reflection.

Per il calcolo di un vettore di Reflection è necessario conoscere la posizione di ogni vertice e di un vettore dal punto di vista a tale vertice. Direct3D può calcolare automaticamente i vettori di reflection per la geometria. L'uso di questa funzionalità consente di risparmiare memoria perché non è necessario includere coordinate di trama per la mappa dell'ambiente. Consente inoltre di ridurre la larghezza di banda e, nel caso di un dispositivo HAL T&L, può essere notevolmente più veloce rispetto ai calcoli che l'applicazione può creare autonomamente. Per usare questa funzionalità, nella fase della trama che contiene la mappa dell'ambiente cubica impostare lo \_ stato della fase della trama D3DTSS TEXCOORDINDEX su una combinazione del \_ membro D3DTSS TCI \_ CAMERASPACEREFLECTIONVECTOR di [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) e dell'indice di un set di coordinate di trama. In alcune situazioni, ad esempio il mapping della luce diffusa, è possibile usare \_ il \_ membro D3DTSS TCI CAMERASPACENORMAL di **D3DTEXTURESTAGESTATETYPE**, che fa in modo che il sistema usi il vettore di indirizzamento, ovvero lo spazio della fotocamera, la normalità dei vertici per la trama. L'indice viene usato solo dal sistema per determinare la modalità di wrapping per la trama.

Nell'esempio di codice riportato di seguito viene illustrato il modo in cui viene utilizzato questo valore.


```
// The m_d3dDevice variable is a valid pointer
// to an IDirect3DDevice9 interface.

// Automatically generate texture coordinates for stage 2.
// This assumes that stage 2 is assigned a cube map.
// Use the wrap mode from the texture coordinate set at index 1.

m_d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX,
                                   D3DTSS_TCI_CAMERASPACEREFLECTIONVECTOR | 1); 
```



Quando si Abilita la generazione automatica delle coordinate di trama, il sistema usa una delle due formule per calcolare il vettore di reflection per ogni vertice. Quando lo \_ stato di rendering LOCALVIEWER di D3DRS è impostato su **true**, viene utilizzata la formula seguente.

![formula del vettore di Reflection (r = 2 (exn) n-e)](images/reflection-vector-local.png)

Nella formula precedente R è il vettore di reflection in fase di calcolo, E è il vettore di posizione normalizzato e N è la normalità del vertice dello spazio della fotocamera.

Quando lo \_ stato di rendering LOCALVIEWER di D3DRS è impostato su **false**, il sistema utilizza la formula seguente.

![formula del vettore di Reflection (r = 2nzn-i)](images/reflection-vector-nonlocal.png)

Gli elementi R e N in questa formula sono identici a quelli della formula precedente. L'elemento N<sub>z</sub> è la Z dello spazio globale del vertice normale ed è il vettore (0, 0, 1) di un punto di vista a distanza infinita. Il sistema utilizza il vettore di reflection di una delle due formule per selezionare e indirizzare il volto appropriato della mappa del cubo.

> [!Note]  
> Nella maggior parte dei casi, le applicazioni devono abilitare la normalizzazione automatica delle normali dei vertici. A tale scopo, impostare D3DRS \_ NORMALIZENORMALS su **true**. Se non si Abilita questo stato di rendering, l'aspetto della mappa dell'ambiente sarà notevolmente diverso da quanto previsto.

 

Informazioni aggiuntive sono contenute nell'argomento seguente.

-   [Creazione di superfici della mappa dell'ambiente cubico (Direct3D 9)](creating-cubic-environment-map-surfaces.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping dell'ambiente](environment-mapping.md)
</dt> </dl>

 

 
