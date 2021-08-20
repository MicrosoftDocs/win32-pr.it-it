---
title: Comportamento del rasterizzatore con riquadri non mappati
description: Questa sezione descrive il comportamento del rasterizzatore con riquadri non mappati.
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16612e8538ec57178ed053ae1a6333c11fcaa6e4454b387408f3d99c6004eb47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608511"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a>Comportamento del rasterizzatore con riquadri non mappati

Questa sezione descrive il comportamento del rasterizzatore con riquadri non mappati.

## <a name="depthstencilview"></a>DepthStencilView

Il comportamento depth stencil lettura e scrittura DSV (Depth stencil View) dipende dal livello di supporto hardware. Per una suddivisione dei requisiti, vedere Il comportamento complessivo di lettura e scrittura per le funzionalità delle [risorse affiancate nei livelli](tiled-resources-features-tiers.md).

Ecco il comportamento ideale:

Se non viene eseguito il mapping di un riquadro in DepthStencilView, il valore restituito dalla profondità di lettura è 0, che viene quindi inserito in tutte le operazioni configurate per il valore di lettura della profondità. Le scritture nel riquadro di profondità mancante vengono eliminate. Questa definizione ideale per la gestione della scrittura non è richiesta dal [livello 2.](tier-2.md) le scritture in riquadri non mappati possono terminare in una cache che le successive operazioni di lettura potrebbero raccogliere.

## <a name="rendertargetview"></a>RenderTargetView

Il comportamento delle operazioni di lettura e scrittura della visualizzazione di destinazione di rendering (RTV) dipende dal livello di supporto hardware. Per una suddivisione dei requisiti, vedere Il comportamento complessivo di lettura e scrittura per le funzionalità delle [risorse affiancate nei livelli](tiled-resources-features-tiers.md).

In tutte le implementazioni, diversi RTV (e DSV) associati contemporaneamente possono avere aree diverse mappate rispetto a quelle non mappate e possono avere formati di superficie di dimensioni diverse (ovvero forme di riquadro diverse).

Ecco il comportamento ideale:

Le operazioni di lettura da RTV restituiscono 0 nei riquadri mancanti e le scritture vengono eliminate. Questa definizione ideale per la gestione della scrittura non è richiesta dal [livello 2.](tier-2.md) le scritture in riquadri non mappati possono terminare in una cache che le successive operazioni di lettura potrebbero raccogliere.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso della pipeline alle risorse affiancate](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




