---
title: Accesso alla pipeline alle risorse affiancate
description: Le risorse affiancate possono essere usate in visualizzazioni di risorse shader (SRV), visualizzazioni di destinazione di rendering (RTV), viste depth stencil (DSV) e viste di accesso non ordinate (UAV), nonché alcuni punti di binding in cui non vengono usate le visualizzazioni, ad esempio le associazioni del buffer dei vertici.
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4a183fcaee90d84985a09c83826a4ad0b6d646
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729255"
---
# <a name="pipeline-access-to-tiled-resources"></a>Accesso alla pipeline alle risorse affiancate

Le risorse affiancate possono essere usate in visualizzazioni di risorse shader (SRV), visualizzazioni di destinazione di rendering (RTV), viste depth stencil (DSV) e viste di accesso non ordinate (UAV), nonché alcuni punti di binding in cui non vengono usate le visualizzazioni, ad esempio le associazioni del buffer dei vertici. Per l'elenco dei binding supportati, vedere [parametri di creazione di risorse affiancati](tiled-resource-creation-parameters.md). \*Le operazioni di copia funzionano anche con le risorse affiancate.

Se più coordinate del riquadro in una o più visualizzazioni sono vincolate alla stessa posizione di memoria, le letture e le Scritture da percorsi diversi alla stessa memoria si verificheranno in un ordine non deterministico e non ripetibile di accessi alla memoria.

Se tutti i riquadri dietro un footprint di accesso alla memoria da uno shader vengono mappati a tessere univoche, il comportamento è identico in tutte le implementazioni della superficie con lo stesso contenuto della memoria in modalità non affiancata.

In questa sezione vengono fornite ulteriori informazioni sull'accesso alla pipeline per le risorse affiancate.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                              | Descrizione                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comportamento di SRV con riquadri non mappati](srv-behavior-with-non-mapped-tiles.md)<br/>                            | Il comportamento delle letture di visualizzazione risorse shader (SRV) che coinvolgono i riquadri non mappati dipende dal livello di supporto hardware. <br/>                                          |
| [Comportamento di UAV con riquadri non mappati](uav-behavior-with-non-mapped-tiles.md)<br/>                            | Il comportamento delle letture e scritture degli accessi (UAV) non ordinati dipende dal livello di supporto hardware. <br/>                                                            |
| [Comportamento del rasterizzatore con riquadri non mappati](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | Questa sezione descrive il comportamento di rasterizzazione con riquadri non mappati.<br/>                                                                                              |
| [Limitazioni di accesso ai riquadri con mapping duplicati](tile-access-limitations-with-duplicate-mappings-.md)<br/> | Questa sezione descrive le limitazioni di accesso ai riquadri con mapping duplicati.<br/>                                                                                        |
| [Funzionalità di campionamento della trama delle risorse affiancate](tiled-resources-texture-sampling-features.md)<br/>              | Questa sezione descrive le funzionalità di campionamento delle trame di risorse affiancate.<br/>                                                                                              |
| [Esposizione delle risorse affiancate HLSL](hlsl-tiled-resources-exposure.md)<br/>                                      | Per supportare le risorse affiancate nel [modello di shader 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)è necessaria la nuova sintassi Microsoft High Level Shader Language (HLSL). <br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse affiancate](tiled-resources.md)
</dt> </dl>

 

