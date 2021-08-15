---
description: La maggior parte delle trame, come le bitmap, è una matrice bidimensionale di valori di colore.
ms.assetid: vs|directx_sdk|~\texture_coordinates.htm
title: Coordinate della trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff2c2c86eebac77d910b5dc6c583df380f0bbb2ccb3dca2fc65b9e929e7abb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519823"
---
# <a name="texture-coordinates-direct3d-9"></a>Coordinate della trama (Direct3D 9)

La maggior parte delle trame, come le bitmap, è una matrice bidimensionale di valori di colore. Le trame della mappa dell'ambiente cubico sono un'eccezione. Per informazioni dettagliate, [vedere Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md). I singoli valori di colore sono detti elemento trama o texel. Ogni texel ha un indirizzo univoco nella trama. L'indirizzo può essere pensato come un numero di colonna e di riga, che sono etichettati rispettivamente con v e nella figura seguente.

![illustrazione di un indirizzo texel come numeri di colonna e di riga](images/uvcoordinates.jpg)

Le coordinate della trama sono nello spazio della trama. Ovvero, sono relativi alla posizione (0,0) nella trama. Quando una trama viene applicata a una primitiva nello spazio 3D, i relativi indirizzi texel devono essere mappati in coordinate dell'oggetto. Devono quindi essere tradotti in coordinate dello schermo o posizioni in pixel.

## <a name="mapping-texels-to-screen-space"></a>Mapping di Texel allo spazio dello schermo

Direct3D esegue il mapping dei texel nello spazio della trama direttamente ai pixel nello spazio dello schermo, ignorando il passaggio intermedio per una maggiore efficienza. Questo processo di mapping è in realtà un mapping inverso. Ciò significa che, per ogni pixel nello spazio dello schermo, viene calcolata la posizione del texel corrispondente nello spazio della trama. Viene campionato il colore della trama in corrispondenza o intorno a tale punto. Il processo di campionamento è detto filtro delle trame. Per altre informazioni, vedere [Filtro trame (Direct3D 9).](texture-filtering.md)

Ogni texel in una trama può essere specificato dalla coordinata del texel. Tuttavia, per eseguire il mapping di texel su primitive, Direct3D richiede un intervallo di indirizzi uniforme per tutti i texel in tutte le trame. Viene quindi utilizzato uno schema di indirizzamento generico in cui tutti gli indirizzi texel sono compresi nell'intervallo compreso tra 0,0 e 1,0 inclusi. Le applicazioni Direct3D specificano le coordinate delle trame in termini di valore,v, in modo molto simile alle coordinate cartesiane 2D specificate in termini di coordinate x,y. Tecnicamente, il sistema può effettivamente elaborare le coordinate della trama al di fuori dell'intervallo 0.0 e 1.0 e lo fa usando i parametri impostati per l'indirizzamento della trama. Per altre informazioni, vedere [Modalità di indirizzamento delle trame (Direct3D 9).](texture-addressing-modes.md)

Di conseguenza, gli indirizzi di trama identici possono essere mappati a coordinate texel diverse in trame diverse. Nella figura seguente l'indirizzo della trama è (0.5,1.0). Tuttavia, poiché le trame sono di dimensioni diverse, l'indirizzo della trama esegue il mapping a texel diversi. Texture 1, a sinistra, è 5x5. L'indirizzo della trama (0.5,1.0) esegue il mapping a texel (2,4). Texture 2, a destra, è 7x7. L'indirizzo della trama (0.5,1.0) esegue il mapping a texel (3,6).

![illustrazione del mapping dello stesso indirizzo di trama a texel diversi su trame diverse](images/texadr1.png)

Nella figura seguente è illustrata una versione semplificata del processo di mapping dei texel. Questo esempio è estremamente semplice. Per informazioni più dettagliate, vedere [Directly Mapping Texels to Pixels (Direct3D 9) (Mapping diretto di Texel ai pixel (Direct3D 9).](directly-mapping-texels-to-pixels.md)

![illustrazione di pixel (quadrato di colore) mappato nello spazio degli oggetti](images/texadr2.png)

Per questo esempio, un pixel, mostrato a sinistra dell'illustrazione, viene idealizzato in un quadrato di colore. Gli indirizzi dei quattro angoli del pixel vengono mappati alla primitiva 3D nello spazio oggetti. La forma del pixel è spesso distorta a causa della forma della primitiva nello spazio 3D e dell'angolo di visualizzazione. Gli angoli della superficie di attacco sulla primitiva che corrispondono agli angoli del pixel vengono quindi mappati nello spazio della trama. Il processo di mapping distorce nuovamente la forma del pixel, operazione comune. Il valore del colore finale del pixel viene calcolato dai texel nell'area a cui viene mappato il pixel. È possibile determinare il metodo utilizzato da Direct3D per ottenere il colore in pixel quando si imposta il metodo di filtro della trama. Per altre informazioni, vedere [Filtro trame (Direct3D 9).](texture-filtering.md)

L'applicazione può assegnare le coordinate di trama direttamente ai vertici. Questa funzionalità consente di controllare quale parte di una trama viene mappata in una primitiva. Si supponga, ad esempio, di creare una primitiva rettangolare che abbia esattamente le stesse dimensioni della trama nella figura seguente. In questo esempio si vuole che l'applicazione esemplime l'intera trama sull'intera superficie. Le coordinate della trama assegnate dall'applicazione ai vertici della primitiva sono (0.0,0.0), (1.0,0.0), (1.0,1.0) e (0.0,1.0).

![illustrazione di una superficie mappata a trama](images/texadr3.png)

Se si decide di ridurre di metà l'altezza della superficie, è possibile distorcere la trama per adattarla alla superficie più piccola oppure assegnare coordinate di trama che determinano l'uso della metà inferiore della trama da parte di Direct3D.

Se si decide di distorcere o ridimensionare la trama per adattarla alla superficie più piccola, il metodo di filtro della trama che si usa influirà sulla qualità dell'immagine. Per altre informazioni, vedere [Filtro trame (Direct3D 9).](texture-filtering.md)

Se invece si decide di assegnare coordinate di trama per fare in modo che Direct3D usi la metà inferiore della trama per la superficie più piccola, la trama coordina l'applicazione assegna ai vertici della primitiva in questo esempio sono (0.0,0.5), (1.0,0.5), (1.0,1.0) e (0.0,1.0). Direct3D applica la metà inferiore della trama alla superficie.

È possibile che le coordinate di trama di un vertice siano maggiori di 1,0. Quando si assegnano coordinate di trama a un vertice non compreso nell'intervallo compreso tra 0,0 e 1,0 inclusi, è necessario impostare anche la modalità di indirizzamento della trama. Per altre informazioni, vedere [Modalità di indirizzamento delle trame (Direct3D 9).](texture-addressing-modes.md)

## <a name="texture-coordinates-and-texture-stages"></a>Coordinate di trama e fasi della trama

Le coordinate della trama sono associate alle trame tramite le fasi della trama. Le trame vengono assegnate alle fasi della trama con SetTexture(stageIndex, pTexture). Vedere [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).

Un codice FVF (Flexible Vertex Format) può definire fino a otto set di coordinate di trama. I dati delle coordinate della trama vengono forniti dall'utente nei dati dei vertici. Ai dati viene fatto riferimento con un indice in base zero: da 0 a 7. Sono presenti fino a otto fasi di fusione delle trame. Una trama è associata a una determinata fase usando SetTexture( stageIndex, pTexture).

Al termine, qualsiasi set di coordinate di trama può essere usato da qualsiasi fase. Ogni set di coordinate è associato a una fase usando SetTextureStageState( stageIndex, D3DTSS \_ TEXCOORDINDEX, textureCoordinateIndex ). Vedere [**IDirect3DDevice9::SetTextureStageState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) In questo modo, le fasi di fusione possono essere impostate in modo da usare qualsiasi trama e qualsiasi coordinata di trama. Più fasi possono usare le stesse trame o le stesse coordinate di trama.

Informazioni aggiuntive sono contenute negli argomenti seguenti.

-   [Formati delle coordinate della trama (Direct3D 9)](texture-coordinate-formats.md)
-   [Elaborazione delle coordinate della trama (Direct3D 9)](texture-coordinate-processing.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
