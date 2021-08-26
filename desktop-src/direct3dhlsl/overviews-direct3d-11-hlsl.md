---
title: Modello di shader HLSL 5
description: Modello di shader HLSL 5
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 537b2460b73f30397561dea37bcb3711b64a935c43d45662428585a47d6f6574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095351"
---
# <a name="hlsl-shader-model-5"></a>Modello di shader HLSL 5

Questa sezione contiene materiale di panoramica per il linguaggio High-Level Shader, in particolare le nuove funzionalità del modello di shader 5 introdotte in Microsoft Direct3D 11.

## <a name="in-this-section"></a>Contenuto della sezione



| Elemento                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Collegamento dinamico](overviews-direct3d-11-hlsl-dynamic-linking.md)<br/>                                 | Il collegamento dinamico consente al runtime di prendere una decisione in fase di disegno (anziché in fase di compilazione) sul percorso del codice da eseguire. In questo modo si riduce il problema di proliferazione degli shader causato dagli shader con firme di input quasi identiche.<br/>                                                                                                                         |
| <span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Funzionalità geometry shader](overviews-direct3d-11-hlsl-gs-features.md)<br/> | Nuove funzionalità di geometry shader, tra cui la creazione di istanze, che offre un miglioramento delle prestazioni quando l'ordine delle primitive nel flusso non è importante e flussi di output con più punti, in modo che uno shader possa eseguire l'output dei vertici in più flussi.<br/>                                                                                                                |
| <span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Mosaico](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)<br/>                                        | Il runtime Direct3D 11 supporta tre nuove fasi che implementano la suddivisione a fasi, che converte le superfici di suddivisione con dettagli bassi in primitive più dettagliate nella GPU. Tessere a tessere a tessere (o scomposizioni) superfici di ordine elevato in strutture adatte per il rendering. Le tre fasi a sfollamento sono le fasi hull-shader, tessellator e domain-shader.<br/> |



 

La sezione di riferimento illustra anche molti nuovi elementi [](d3d11-graphics-reference-sm5-attributes.md)API per il modello shader 5, tra cui [attributi,](d3d11-graphics-reference-sm5-intrinsics.md)funzioni intrinseche, oggetti e metodi del modello [shader 5](d3d11-graphics-reference-sm5-objects.md)e valori [di sistema.](d3d11-graphics-reference-sm5-system-values.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

