---
description: Informazioni sulla fusione alfa. La fusione alfa viene usata per visualizzare un'immagine con pixel trasparenti o semitrasparenti.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Fusione alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081c194b9eae85dca5599f2bf9f779d1cd896c8a37641df5105bb049b4a5bc22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751581"
---
# <a name="alpha-blending-direct3d-9"></a>Fusione alfa (Direct3D 9)

La fusione alfa viene usata per visualizzare un'immagine con pixel trasparenti o semitrasparenti. Oltre a un canale di colori rosso, verde e blu, ogni pixel in una bitmap alfa ha un componente di trasparenza noto come canale alfa. Il canale alfa contiene in genere tutti i bit di un canale di colore. Ad esempio, un canale alfa a 8 bit può rappresentare 256 livelli di trasparenza, da 0 (l'intero pixel è trasparente) a 255 (l'intero pixel è opaco). L'elenco seguente mostra alcuni effetti speciali che è possibile creare usando la fusione alfa.

Il colore può essere definito con o senza valori alfa. Il colore senza alfa è il colore RGB con alfa archiviato come ARGB. I dati sui vertici, i dati sui materiali e i dati di trama possono essere usati per fornire la trasparenza dell'oggetto. Il buffer dei frame può essere usato anche per generare effetti di trasparenza.

-   [Vertice alfa (Direct3D 9)](vertex-alpha.md)
-   [Alfa materiale (Direct3D 9)](material-alpha.md)
-   [Alfa trama (Direct3D 9)](texture-alpha.md)
-   [Frame Buffer Alpha (Direct3D 9)](frame-buffer-alpha.md)
-   [Eseguire il rendering del valore alfa di destinazione (Direct3D 9)](render-target-alpha.md)

Gli esempi che illustrano i caratteri alfa includono:

-   [Confronto (Direct3D 9)](billboarding.md)
-   [Cloud, Smoke e Trails (Direct3D 9)](clouds--smoke--and-vapor-trails.md)
-   [Incendio, flare ed esplosione (Direct3D 9)](fire--flares--and-explosions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direct3D Rendering](direct3d-rendering.md)
</dt> </dl>

 

 



