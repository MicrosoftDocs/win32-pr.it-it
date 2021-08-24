---
description: Le mappe di ambiente sferiche, o mappe a sfera, sono trame speciali che contengono un'immagine della scena che circonda un oggetto o gli effetti di illuminazione intorno all'oggetto.
ms.assetid: b4a8defc-876f-4a23-a12e-e7423a1e8f89
title: Mapping dell'ambiente sferico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be4347b71a041aaa8d7057ac2bb7523bfa235fe59f84fe1ba54c54283cd2159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746391"
---
# <a name="spherical-environment-mapping-direct3d-9"></a>Mapping dell'ambiente sferico (Direct3D 9)

Le mappe di ambiente sferiche, o mappe a sfera, sono trame speciali che contengono un'immagine della scena che circonda un oggetto o gli effetti di illuminazione intorno all'oggetto. A differenza delle mappe di ambiente cubiche, le mappe a sfera non rappresentano direttamente l'ambiente circostante di un oggetto. L'immagine della teiera nell'argomento [Environment Mapping (Direct3D 9)](environment-mapping.md) (Mapping dell'ambiente - Direct3D 9) illustra gli effetti di reflection che è possibile ottenere con il mapping della sfera. Una mappa a sfera è una rappresentazione 2D della vista completa a 360 gradi della scena che circonda un oggetto, come se fosse presa attraverso una lente a occhio dipersi, come illustrato nella figura seguente.

![illustrazione di una mappa a sfera dell'interno di un edificio](images/spheremap.png)

## <a name="texture-coordinates-for-spherical-environment-maps"></a>Coordinate di trama per l'ambiente sferico Mappe

Le coordinate di trama specificate per ogni vertice che riceve un mapping dell'ambiente devono essere indirizzate alla trama come funzione della distorsione riflettente creata dalla curvatura della superficie. Le applicazioni devono calcolare queste coordinate di trama per ogni vertice per ottenere l'effetto desiderato. Un modo semplice ed efficace per generare le coordinate della trama usa la normale del vertice come input. Anche se esistono diversi metodi, l'equazione seguente è comune tra le applicazioni che eseguono il mapping dell'ambiente con le mappe di sfera.

![equazione di calcolo delle coordinate di trama per una mappa sphere](images/spheremap-formula.png)

In queste formule, tu e v sono le coordinate della trama che vengono calcolate e N<sub>X</sub> e N<sub>Y</sub> sono i componenti x e y del vertice normale dello spazio della fotocamera. La formula è semplice ma efficace. Se la normale ha un componente x positivo, la normale punta a destra e la coordinata u viene regolata per fare riferimento alla trama in modo appropriato. Analogamente alla coordinata v: y positivo indica che la normale punta verso l'alto. Il contrario è vero per i valori negativi in ogni componente.

Se il normale punta direttamente alla fotocamera, le coordinate risultanti non devono ricevere distorsioni. La distorsione +0,5 per entrambe le coordinate posiziona il punto di distorsione zero al centro della mappa sphere e una normale vertice di (0, 0, z) punta a questo punto. Questa formula non rappresenta il componente z della normale, ma le applicazioni che usano la formula possono ottimizzare i calcoli ignorando i vertici con una normale con un elemento z positivo. Questa operazione funziona per gli oggetti con ombreggiatura piatta perché, nello spazio della fotocamera, se la normale punta all'esterno della fotocamera (z positiva), il vertice viene sottoposto a culled quando viene eseguito il rendering dell'oggetto. Per gli oggetti ombreggiati da Gouraud, una normale può puntare lontano dalla fotocamera (x positiva) e il triangolo contenente il vertice può comunque essere visibile. Se non si calcola l'utente e v per questo vertice, il viso potrebbe comunque essere usato, determinando un comportamento imprevisto.

## <a name="applying-spherical-environment-maps"></a>Applicazione di Spherical Environment Mappe

Si applica una mappa dell'ambiente agli oggetti nello stesso modo di qualsiasi altra trama, impostando la trama sulla fase di trama appropriata con il metodo [**IDirect3DDevice9::SetTexture.**](/windows/desktop/api) Impostare il primo parametro sull'indice per la fase di trama desiderata e impostare il secondo parametro sull'indirizzo [**dell'interfaccia IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) restituita quando è stata creata la trama per la mappa dell'ambiente. È possibile impostare il colore e le operazioni di fusione alfa e gli argomenti in base alle esigenze per ottenere gli effetti di fusione della trama desiderati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping dell'ambiente](environment-mapping.md)
</dt> </dl>

 

 
