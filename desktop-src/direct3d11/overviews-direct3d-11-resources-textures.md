---
title: Trame
description: Questa sezione descrive le trame usate in Direct3D 11 e i collegamenti alla documentazione basata su attività per scenari comuni.
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e02fbc59922710aaf764dafd363429a68c734d365335f5bdb4355bec8570971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027841"
---
# <a name="textures"></a>Trame

Una trama archivia le informazioni sui texel. Questa sezione descrive le trame usate in Direct3D 11 e i collegamenti alla documentazione basata su attività per scenari comuni.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introduzione alle trame in Direct3D 11](overviews-direct3d-11-resources-textures-intro.md)<br/> | Una risorsa trama è una raccolta strutturata di dati progettati per archiviare texel. Un texel rappresenta l'unità più piccola di una trama che può essere letta o scritta dalla pipeline. A differenza dei buffer, le trame possono essere filtrate in base ai campionatori di trama mentre vengono lette dalle unità shader. Il tipo di trama influisce sul modo in cui viene filtrata. Ogni texel contiene da 1 a 4 componenti, disposti in uno dei formati DXGI definiti dall'enumerazione DXGI \_ FORMAT.<br/> |
| [Compressione dei blocchi di trama in Direct3D 11](texture-block-compression-in-direct3d-11.md)<br/>      | Il supporto della compressione a blocchi per le trame è stato esteso in Direct3D 11 per includere gli algoritmi BC6H e BC7. BC6H supporta i dati di origine dei colori a intervalli dinamici elevati e BC7 offre una compressione di qualità migliore della media con meno artefatti per i dati di origine RGB standard.<br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedura: Creare una trama](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[Procedura: Inizializzare una trama a livello di codice](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[Procedura: Inizializzare una trama da un file](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[Risorse](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





