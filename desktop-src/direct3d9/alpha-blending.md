---
description: La fusione alfa viene utilizzata per visualizzare un'immagine con pixel trasparenti o semitrasparenti.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Fusione alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f4ae2883c7a9a92ba1b62306dc26bf09d0d9947
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127239"
---
# <a name="alpha-blending-direct3d-9"></a>Fusione alfa (Direct3D 9)

La fusione alfa viene utilizzata per visualizzare un'immagine con pixel trasparenti o semitrasparenti. Oltre a un canale di colore rosso, verde e blu, ogni pixel in una bitmap alfa presenta un componente di trasparenza noto come canale alfa. Il canale alfa contiene in genere tutti i bit di un canale colori. Un canale alfa a 8 bit, ad esempio, può rappresentare 256 livelli di trasparenza, da 0 (l'intero pixel è trasparente) a 255 (l'intero pixel è opaco). L'elenco seguente illustra alcuni effetti speciali che è possibile creare usando la fusione alfa.

Il colore può essere definito con o senza valori alfa. Il colore senza alfa è il colore RGB con alfa viene archiviato come ARGB. I dati dei vertici, i dati del materiale e i dati di trama possono essere utilizzati per garantire la trasparenza dell'oggetto. Il buffer del frame può essere usato anche per generare effetti di trasparenza.

-   [Alfa vertice (Direct3D 9)](vertex-alpha.md)
-   [Materiale Alfa (Direct3D 9)](material-alpha.md)
-   [Trama alfa (Direct3D 9)](texture-alpha.md)
-   [Buffer frame alfa (Direct3D 9)](frame-buffer-alpha.md)
-   [Alfa destinazione rendering (Direct3D 9)](render-target-alpha.md)

Gli esempi che dimostrano Alpha includono:

-   [Billboard (Direct3D 9)](billboarding.md)
-   [Percorsi cloud, fumo e Vapor (Direct3D 9)](clouds--smoke--and-vapor-trails.md)
-   [Incendi, flare ed esplosioni (Direct3D 9)](fire--flares--and-explosions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



