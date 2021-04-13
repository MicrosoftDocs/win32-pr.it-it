---
description: La maggior parte delle trame, come le bitmap, è una matrice bidimensionale di valori dei colori.
ms.assetid: vs|directx_sdk|~\texture_coordinates.htm
title: Coordinate di trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dcf4c886c187aaa2218508a180e23644a544739
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482692"
---
# <a name="texture-coordinates-direct3d-9"></a>Coordinate di trama (Direct3D 9)

La maggior parte delle trame, come le bitmap, è una matrice bidimensionale di valori dei colori. Le trame della mappa dell'ambiente cubico sono un'eccezione. Per informazioni dettagliate, vedere [mapping di ambienti cubici (Direct3D 9)](cubic-environment-mapping.md). I singoli valori di colore sono detti elemento texture o Texel. Ogni Texel ha un indirizzo univoco nella trama. L'indirizzo può essere considerato come un numero di colonna e di riga, che vengono etichettati rispettivamente e v nella figura seguente.

![illustrazione di un indirizzo Texel come numeri di colonna e di riga](images/uvcoordinates.jpg)

Le coordinate di trama si trovano nello spazio di trama. Ovvero sono relativi alla posizione (0, 0) nella trama. Quando si applica una trama a una primitiva nello spazio 3D, è necessario eseguire il mapping degli indirizzi Texel nelle coordinate dell'oggetto. Devono quindi essere convertite in coordinate dello schermo o posizioni dei pixel.

## <a name="mapping-texels-to-screen-space"></a>Mapping di Texel allo spazio dello schermo

Direct3D esegue il mapping dei Texel nello spazio di trama direttamente ai pixel nello spazio dello schermo, ignorando il passaggio intermedio per una maggiore efficienza. Questo processo di mapping è in realtà un mapping inverso. Ovvero per ogni pixel nello spazio dello schermo, viene calcolata la posizione di Texel corrispondente nello spazio di trama. Viene campionato il colore della trama in corrispondenza o intorno a tale punto. Il processo di campionamento è denominato filtro della trama. Per altre informazioni, vedere [filtro delle trame (Direct3D 9)](texture-filtering.md).

Ogni Texel in una trama può essere specificato dalla relativa coordinata Texel. Tuttavia, per eseguire il mapping dei Texel in primitive, Direct3D richiede un intervallo di indirizzi uniformi per tutti i Texel in tutte le trame. Quindi, usa uno schema di indirizzamento generico in cui tutti gli indirizzi Texel sono compresi nell'intervallo tra 0,0 e 1,0 inclusi. Le applicazioni Direct3D specificano le coordinate di trama in termini di valori v, in modo analogo alle coordinate cartesiane 2D, in termini di coordinate x, y. Tecnicamente, il sistema è in grado di elaborare le coordinate di trama non comprese nell'intervallo 0,0 e 1,0, usando i parametri impostati per l'indirizzamento della trama. Per altre informazioni, vedere [modalità di indirizzamento delle trame (Direct3D 9)](texture-addressing-modes.md).

Il risultato è che gli indirizzi di trama identici possono eseguire il mapping a coordinate di Texel diverse in trame diverse. Nell'illustrazione seguente l'indirizzo di trama è (0.5, 1.0). Tuttavia, poiché le trame sono di dimensioni diverse, l'indirizzo della trama viene mappato a Texel diversi. La trama 1, a sinistra, è 5x5. L'indirizzo della trama (0,5, 1.0) viene mappato a Texel (2,4). La trama 2, a destra, è 7x7. L'indirizzo della trama (0.5, 1.0) viene mappato a Texel (3, 6).

![illustrazione dello stesso mapping degli indirizzi di trama a Texel diversi su trame diverse](images/texadr1.png)

Nella figura seguente è illustrata una versione semplificata del processo di mapping di Texel. Questo esempio è estremamente semplice. Per informazioni più dettagliate, vedere [mapping diretto dei Texel ai pixel (Direct3D 9)](directly-mapping-texels-to-pixels.md).

![illustrazione di pixel (un quadrato di colore) mappato nello spazio oggetto](images/texadr2.png)

Per questo esempio, un pixel, illustrato a sinistra dell'illustrazione, è idealizzato in un quadrato di colore. Gli indirizzi dei quattro angoli del pixel vengono mappati nella primitiva 3D nello spazio degli oggetti. La forma del pixel viene spesso distorta a causa della forma della primitiva nello spazio 3D e a causa dell'angolo di visualizzazione. Gli angoli della superficie di attacco della primitiva che corrispondono agli angoli del pixel vengono quindi mappati nello spazio di trama. Il processo di mapping consente di ritorcere la forma del pixel, che è comune. Il valore di colore finale del pixel viene calcolato dai Texel nell'area in cui viene eseguito il mapping del pixel. Si determina il metodo utilizzato da Direct3D per arrivare al colore del pixel quando si imposta il metodo di filtro della trama. Per altre informazioni, vedere [filtro delle trame (Direct3D 9)](texture-filtering.md).

L'applicazione può assegnare coordinate di trama direttamente ai vertici. Questa funzionalità consente di controllare la parte di una trama mappata in una primitiva. Si supponga, ad esempio, di creare una primitiva rettangolare che abbia esattamente le stesse dimensioni della trama nella figura seguente. In questo esempio si vuole che l'applicazione Esegui il mapping dell'intera trama sull'intera parete. Le coordinate di trama assegnate dall'applicazione ai vertici della primitiva sono (0,0, 0,0), (1.0, 0,0), (1.0, 1.0) e (0,0, 1.0).

![illustrazione di una parete mappata alla trama](images/texadr3.png)

Se si decide di ridurre l'altezza della parete di una metà, è possibile distorcere la trama per adattarla alla parete più piccola, oppure è possibile assegnare coordinate di trama che fanno sì che Direct3D usi la metà inferiore della trama.

Se si decide di distorcere o ridimensionare la trama per adattarla alla parete più piccola, il metodo di filtro della trama utilizzato influenzerà la qualità dell'immagine. Per altre informazioni, vedere [filtro delle trame (Direct3D 9)](texture-filtering.md).

Se invece si decide di assegnare coordinate di trama per fare in modo che Direct3D usi la metà inferiore della trama per la parete più piccola, le coordinate di trama assegnate all'applicazione ai vertici della primitiva in questo esempio sono (0.0, 0.5), (1.0, 0.5), (1.0, 1.0) e (0.0, 1.0). Direct3D applica la metà inferiore della trama alla parete.

È possibile che le coordinate di trama di un vertice siano maggiori di 1,0. Quando si assegnano coordinate di trama a un vertice che non si trova nell'intervallo compreso tra 0,0 e 1,0, è necessario impostare anche la modalità di indirizzamento della trama. Per altre informazioni, vedere [modalità di indirizzamento delle trame (Direct3D 9)](texture-addressing-modes.md).

## <a name="texture-coordinates-and-texture-stages"></a>Coordinate di trama e fasi della trama

Le coordinate di trama sono associate a trame per mezzo di fasi di trama. Le trame vengono assegnate a fasi di trama con la trama (stageIndex, pTexture). Vedere [**IDirect3DDevice9:: setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).

Un codice FVF (Flexible Vertex Format) può definire fino a otto set di coordinate di trama. I dati delle coordinate di trama sono arredati dall'utente nei dati dei vertici. Ai dati viene fatto riferimento con un indice in base zero: 0-7. Esistono fino a otto fasi di combinazione di trame. Una trama è associata a una particolare fase usando la classe setrame (stageIndex, pTexture).

Al termine di questa operazione, qualsiasi set di coordinate di trama può essere usato da qualsiasi fase. Ogni set di coordinate è associato a una fase mediante SetTextureStageState (stageIndex, D3DTSS \_ TEXCOORDINDEX, textureCoordinateIndex). Vedere [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate). In questo modo, è possibile configurare le fasi di fusione per usare qualsiasi trama e qualsiasi coordinate di trama. Più di una fase può utilizzare le stesse trame o le stesse coordinate di trama.

Informazioni aggiuntive sono contenute negli argomenti seguenti.

-   [Formati di coordinate di trama (Direct3D 9)](texture-coordinate-formats.md)
-   [Elaborazione delle coordinate di trama (Direct3D 9)](texture-coordinate-processing.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
