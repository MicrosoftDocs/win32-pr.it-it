---
title: Comportamento del rasterizzatore con riquadri non mappati
description: Questa sezione descrive il comportamento di rasterizzazione con riquadri non mappati.
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54230321f4286b92a3444e3f74167ee7b8711c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992813"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a>Comportamento del rasterizzatore con riquadri non mappati

Questa sezione descrive il comportamento di rasterizzazione con riquadri non mappati.

## <a name="depthstencilview"></a>DepthStencilView

Il comportamento delle letture e scritture di depth stencil (DSV) dipende dal livello di supporto hardware. Per una suddivisione dei requisiti, vedere il comportamento complessivo di lettura e scrittura per [le risorse affiancate livelli di funzionalità](tiled-resources-features-tiers.md).

Ecco il comportamento ideale:

Se non è stato eseguito il mapping di un riquadro in DepthStencilView, il valore restituito dalla profondità di lettura è 0, che viene quindi inserito in qualsiasi operazione configurata per il valore di lettura profondità. Le Scritture nel riquadro di profondità mancante vengono rimosse. Questa definizione ideale per la gestione delle Scritture non è richiesta dal [livello 2](tier-2.md). le scritture nei riquadri non mappati possono finire in una cache che le letture successive potrebbero prelevare.

## <a name="rendertargetview"></a>RenderTargetView

Il comportamento delle letture e scritture di visualizzazione della destinazione di rendering (RTV) dipende dal livello di supporto hardware. Per una suddivisione dei requisiti, vedere il comportamento complessivo di lettura e scrittura per [le risorse affiancate livelli di funzionalità](tiled-resources-features-tiers.md).

In tutte le implementazioni, i diversi RTVs (e vista origine dati) associati simultaneamente possono avere aree diverse mappate rispetto a quelle non mappate e possono avere formati di superficie di dimensioni diverse, ovvero diverse forme affiancate.

Ecco il comportamento ideale:

Le letture da RTVs restituiscono 0 nei riquadri mancanti e le scritture vengono rimosse. Questa definizione ideale per la gestione delle Scritture non è richiesta dal [livello 2](tier-2.md). le scritture nei riquadri non mappati possono finire in una cache che le letture successive potrebbero prelevare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alla pipeline alle risorse affiancate](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




