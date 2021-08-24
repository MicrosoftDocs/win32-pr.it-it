---
description: L'aggiunta di un oggetto a una scena 3D può migliorare il gioco, fornire un ambiente o impostare uno stato d'aria e nascondere artefatti talvolta causati quando viene vista una geometria distante.
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Chiama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f06f9ff25c132feaed4ada291e7f063fcbfb3f4f1129cf934b43795b79b20aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026936"
---
# <a name="fog-direct3d-9"></a>Chiama (Direct3D 9)

L'aggiunta di un oggetto a una scena 3D può migliorare il gioco, fornire un ambiente o impostare uno stato d'aria e nascondere artefatti talvolta causati quando viene vista una geometria distante. Direct3D supporta due modelli di primo livello, pixel vertice e vertice, ognuno con le proprie funzionalità e l'interfaccia di programmazione.

Essenzialmente, l'oggetto viene implementato combinando il colore degli oggetti in una scena con un colore scelto in base alla profondità di un oggetto in una scena o alla distanza dal punto di vista. Quando gli oggetti diventano più distanti, il colore originale si combina sempre di più con il colore bianco scelto, creando l'avariato che l'oggetto viene sempre più nascosto da piccole particelle che fluttuano nella scena. La figura seguente mostra una scena di cui è stato eseguito il rendering senza rendering e una scena simile con il rendering abilitato.

![illustrazione della stessa scena con e senza](images/fogcomp.png)

In questa illustrazione, la scena a sinistra ha un orizzonte chiaro, oltre il quale non è visibile alcun panorama, anche se sarebbe visibile nel mondo reale. La scena a destra nasconde l'orizzonte usando un colore identico al colore di sfondo, in modo che i poligoni appaiano in dissolvenza in distanza. Combinando gli effetti discreti della luna con la progettazione di scene creative, è possibile aggiungere un'animazione e attenuare il colore degli oggetti in una scena.

Direct3D offre due modi per aggiungere un colore a una scena: pixel pixel e vertice, denominati in base alla modalità di applicazione degli effetti della luce. Per informazioni dettagliate, vedere [Pixel Pixel Pixel (Direct3D 9)](pixel-fog.md) e [Vertex Coordinate (Direct3D 9).](vertex-fog.md) In breve, nel driver di dispositivo viene implementata l'implementazione di pixel pixel pixel, detto anche table, e nel motore di illuminazione Direct3D viene implementato vertexrere. Un'applicazione può implementare un'applicazione con un vertex shader e un pixel contemporaneamente, se necessario.

> [!Note]  
> Indipendentemente dal fatto che si usi il pixel o il vertice, l'applicazione deve fornire una matrice di proiezione conforme per garantire che gli effetti della superficie siano applicati correttamente. Questa restrizione si applica anche alle applicazioni che non usano il motore di trasformazione e illuminazione Direct3D. Per altri dettagli su come fornire una matrice appropriata, vedere [Trasformazione proiezione (Direct3D 9).](projection-transform.md)

 

Negli argomenti seguenti vengono presentate alcune informazioni sull'uso di varie funzionalità nelle applicazioni Direct3D.

-   [Formule di Forma (Direct3D 9)](fog-formulas.md)
-   [Parametri Disas (Direct3D 9)](fog-parameters.md)
-   [Blending Di Blending (Direct3D 9)](fog-blending.md)
-   [Colore Bianco (Direct3D 9)](fog-color.md)
-   [VertexBie (Direct3D 9)](vertex-fog.md)
-   [Pixel Pixel Pixel (Direct3D 9)](pixel-fog.md)

La fusione delle sfumature è controllata dagli stati di rendering; non fa parte della pipeline di pixel programmabile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direct3D Rendering](direct3d-rendering.md)
</dt> </dl>

 

 



