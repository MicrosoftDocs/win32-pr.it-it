---
title: Risorse affiancate
description: Le risorse affiancate possono essere ritenute come risorse logiche di grandi dimensioni che usano piccole quantità di memoria fisica.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73835d6603d1d8d7e708cd422e3991bb88ac1f91cebf016ccce36f2466270c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124089"
---
# <a name="tiled-resources"></a>Risorse affiancate

Le risorse affiancate possono essere ritenute come risorse logiche di grandi dimensioni che usano piccole quantità di memoria fisica.

Questa sezione descrive perché sono necessarie risorse affiancate e come creare e usare le risorse affiancate.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                   | Descrizione                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Perché sono necessarie risorse affiancate?](why-are-tiled-resources-needed-.md)<br/>       | Le risorse affiancate sono necessarie in modo che meno memoria gpu (Graphics Processing Unit) sia sprecata archiviando aree di superfici che l'applicazione sa non saranno accessibili e l'hardware può comprendere come filtrare tra riquadri adiacenti.<br/>     |
| [Creazione di risorse affiancate](creating-tiled-resources.md)<br/>                     | Le risorse affiancate vengono create specificando il flag [**D3D11 \_ RESOURCE \_ MISC \_ TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) quando si crea una risorsa.<br/>                                                                                          |
| [API delle risorse affiancate](tiled-resource-apis.md)<br/>                               | Le API descritte in questa sezione funzionano con le risorse affiancate e il pool di riquadri.<br/>                                                                                                                                                              |
| [Accesso della pipeline alle risorse affiancate](pipeline-access-to-tiled-resources.md)<br/> | Le risorse affiancate possono essere usate nelle visualizzazioni delle risorse shader (SRV), nelle viste di destinazione di rendering (RTV), nelle viste depth stencil (DSV) e nelle viste di accesso non ordinate (UAV), nonché in alcuni punti di associazione in cui le viste non vengono usate, ad esempio le associazioni al buffer dei vertici. <br/> |
| [Livelli di funzionalità delle risorse affiancate](tiled-resources-features-tiers.md)<br/>         | Direct3D 11.2 espone il supporto delle risorse affiancate in due livelli con i valori [**D3D11 \_ TILED \_ RESOURCES \_ TIER.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) <br/>                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





