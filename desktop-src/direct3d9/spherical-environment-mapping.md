---
description: Le mappe dell'ambiente sferico, o mappe Sphere, sono trame speciali che contengono un'immagine della scena che circonda un oggetto o gli effetti di illuminazione intorno all'oggetto.
ms.assetid: b4a8defc-876f-4a23-a12e-e7423a1e8f89
title: Mapping di ambienti sferici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b0e7aaa123478ecc7cc327dca0b13a8aae3d0c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304062"
---
# <a name="spherical-environment-mapping-direct3d-9"></a>Mapping di ambienti sferici (Direct3D 9)

Le mappe dell'ambiente sferico, o mappe Sphere, sono trame speciali che contengono un'immagine della scena che circonda un oggetto o gli effetti di illuminazione intorno all'oggetto. Diversamente dalle mappe di ambiente cubi, le mappe Sphere non rappresentano direttamente i dintorni di un oggetto. L'immagine della teiera nell'argomento [mapping dell'ambiente (Direct3D 9)](environment-mapping.md) Mostra gli effetti della reflection che è possibile ottenere con il mapping di Sphere. Una mappa Sphere è una rappresentazione 2D della visualizzazione completa di 360 gradi della scena che circonda un oggetto, come se venisse eseguita tramite una lente di pesce, come illustrato nella figura seguente.

![illustrazione di una mappa Sphere della parte interna di una compilazione](images/spheremap.png)

## <a name="texture-coordinates-for-spherical-environment-maps"></a>Coordinate di trama per le mappe di ambienti sferici

Le coordinate di trama specificate per ogni vertice che riceve un mapping dell'ambiente devono indirizzare la trama come funzione della distorsione riflessiva creata dalla curvatura della superficie. Le applicazioni devono calcolare queste coordinate di trama per ogni vertice per ottenere l'effetto desiderato. Un modo semplice ed efficace per generare le coordinate di trama usa il vertice normale come input. Sebbene esistano diversi metodi, l'equazione seguente è comune tra le applicazioni che eseguono il mapping dell'ambiente con le mappe Sphere.

![equazione di calcolo delle coordinate di trama per una mappa Sphere](images/spheremap-formula.png)

In queste formule, l'utente e la v sono le coordinate di trama calcolate e N<sub>x</sub> e n<sub>Y</sub> sono i componenti x e Y della normale vertice spazio fotocamera. La formula è semplice ma efficace. Se il normale ha un componente x positivo, il normale punta a destra e la coordinata u viene regolata in modo da indirizzare la trama in modo appropriato. Analogamente, per la coordinata v: y positivo indica che il normale punta verso l'alto. Il contrario è true per i valori negativi in ogni componente.

Se il normale punta direttamente alla fotocamera, le coordinate risultanti non devono ricevere alcuna distorsione. La distorsione + 0,5 a entrambe le coordinate posiziona il punto di distorsione zero al centro della mappa della sfera e una normale del vertice di (0, 0, z) si rivolge a questo punto. Questa formula non tiene conto del componente z del normale, ma le applicazioni che usano la formula possono ottimizzare i calcoli ignorando i vertici con una normale con un elemento z positivo. Questa operazione può essere eseguita per gli oggetti con ombreggiatura piatta perché, nello spazio della fotocamera, se il normale fa riferimento alla fotocamera (positivo z), il vertice viene raccolto quando viene eseguito il rendering dell'oggetto. Per gli oggetti ombreggiati con Gouraud, un normale può puntare fuori dalla fotocamera (x positivo) e il triangolo che contiene il vertice può essere ancora visibile. Se non si calcolano l'utente e il v per questo vertice, è possibile che venga ancora usato il volto, causando un comportamento imprevisto.

## <a name="applying-spherical-environment-maps"></a>Applicazione di mappe di ambienti sferici

Applicare un mapping dell'ambiente agli oggetti in modo analogo a qualsiasi altra trama, impostando la trama sulla fase di trama appropriata con il metodo [**IDirect3DDevice9:: setexture**](/windows/desktop/api) . Impostare il primo parametro sull'indice per la fase di trama desiderata e impostare il secondo parametro sull'indirizzo dell'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) restituita quando è stata creata la trama per la mappa dell'ambiente. È possibile impostare le operazioni e gli argomenti del colore e della fusione alfa in base alle esigenze per ottenere gli effetti desiderati per la fusione della trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping dell'ambiente](environment-mapping.md)
</dt> </dl>

 

 
