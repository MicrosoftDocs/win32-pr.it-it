---
title: Risorse affiancate
description: Le risorse affiancate possono essere considerate come risorse logiche di grandi dimensioni che utilizzano piccole quantità di memoria fisica.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c7e6aaf60f58f55274c9d7a135b9107933f640
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855549"
---
# <a name="tiled-resources"></a>Risorse affiancate

Le risorse affiancate possono essere considerate come risorse logiche di grandi dimensioni che utilizzano piccole quantità di memoria fisica.

In questa sezione viene descritto il motivo per cui sono necessarie risorse affiancate e la modalità di creazione e utilizzo di risorse affiancate.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                   | Descrizione                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Perché sono necessarie risorse affiancate?](why-are-tiled-resources-needed-.md)<br/>       | Le risorse affiancate sono necessarie, in modo che la memoria dell'unità di elaborazione grafica (GPU) venga sprecata per l'archiviazione di aree di superfici che l'applicazione sa non sarà accessibile e l'hardware possa comprendere come filtrare tra i riquadri adiacenti.<br/>     |
| [Creazione di risorse affiancate](creating-tiled-resources.md)<br/>                     | Quando si crea una risorsa, le risorse affiancate vengono create specificando il flag di [**\_ \_ varie \_ risorse di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .<br/>                                                                                          |
| [API di risorse affiancate](tiled-resource-apis.md)<br/>                               | Le API descritte in questa sezione funzionano con le risorse affiancate e il pool di sezioni.<br/>                                                                                                                                                              |
| [Accesso alla pipeline alle risorse affiancate](pipeline-access-to-tiled-resources.md)<br/> | Le risorse affiancate possono essere usate in visualizzazioni di risorse shader (SRV), visualizzazioni di destinazione di rendering (RTV), viste depth stencil (DSV) e viste di accesso non ordinate (UAV), nonché alcuni punti di binding in cui non vengono usate le visualizzazioni, ad esempio le associazioni del buffer dei vertici. <br/> |
| [Livelli di funzionalità delle risorse affiancate](tiled-resources-features-tiers.md)<br/>         | Direct3D 11,2 espone il supporto di risorse affiancate in due livelli con i valori del [**\_ \_ \_ livello di risorse affiancati d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) . <br/>                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





