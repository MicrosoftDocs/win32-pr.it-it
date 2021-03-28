---
title: Trame
description: Questa sezione descrive le trame usate in Direct3D 11 e i collegamenti alla documentazione basata su attività per gli scenari comuni.
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc3909f354b0709e82ffd2bdffafe6cdb35516
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221746"
---
# <a name="textures"></a>Trame

Una trama archivia le informazioni di Texel. Questa sezione descrive le trame usate in Direct3D 11 e i collegamenti alla documentazione basata su attività per gli scenari comuni.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introduzione alle trame in Direct3D 11](overviews-direct3d-11-resources-textures-intro.md)<br/> | Una risorsa di trama è una raccolta strutturata di dati progettati per archiviare Texel. Un Texel rappresenta l'unità più piccola di una trama che può essere letta o scritta dalla pipeline. A differenza dei buffer, le trame possono essere filtrate in base ai Sampler di trama Man mano che vengono lette dalle unità dello shader. Il tipo di trama influisca sul modo in cui la trama viene filtrata. Ogni Texel contiene da 1 a 4 componenti, disposti in uno dei formati DXGI definiti dall'enumerazione del \_ formato dxgi.<br/> |
| [Compressione dei blocchi di trama in Direct3D 11](texture-block-compression-in-direct3d-11.md)<br/>      | Il supporto per la compressione dei blocchi (BC) per le trame è stato esteso in Direct3D 11 per includere gli algoritmi BC6H e BC7. BC6H supporta i dati di origine dei colori con intervallo dinamico elevato e BC7 offre una compressione di qualità migliore rispetto alla media con meno elementi per i dati di origine RGB standard.<br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedura: creare una trama](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[Procedura: inizializzare una trama a livello di codice](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[Procedura: inizializzare una trama da un file](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[Risorse](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





