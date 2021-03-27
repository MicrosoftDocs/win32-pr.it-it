---
title: HLSL Shader Model 5
description: HLSL Shader Model 5
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b33b0e2f009b796eb0b8828cc195fb9543ba2b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872657"
---
# <a name="hlsl-shader-model-5"></a>HLSL Shader Model 5

Questa sezione contiene informazioni generali sulla High-Level Shader Language, in particolare le nuove funzionalità di Shader Model 5 introdotte in Microsoft Direct3D 11.

## <a name="in-this-section"></a>Contenuto della sezione



| Elemento                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Collegamento dinamico](overviews-direct3d-11-hlsl-dynamic-linking.md)<br/>                                 | Il collegamento dinamico consente al runtime di prendere una decisione in fase di creazione, anziché in fase di compilazione, sul percorso del codice da eseguire. In questo modo si riduce il problema di proliferazione dello shader causato da shader con firme di input quasi identiche.<br/>                                                                                                                         |
| <span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Funzionalità di Geometry shader](overviews-direct3d-11-hlsl-gs-features.md)<br/> | Nuove funzionalità di Geometry shader, tra cui: istanza, che fornisce un miglioramento delle prestazioni quando l'ordine delle primitive nel flusso non è rilevante e più flussi di output del punto in modo che uno shader possa restituire i vertici su più di un flusso.<br/>                                                                                                                |
| <span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Tassellatura](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)<br/>                                        | Il runtime di Direct3D 11 supporta tre nuove fasi che implementano lo schema a mosaico, che converte le aree di sottodivisione con dettagli più bassi in primitive di dettaglio nella GPU. Tessere a mosaico (o suddividere) superfici di ordine superiore in strutture appropriate per il rendering. Le tre fasi a mosaico sono le fasi Hull-shader, mosaico e Domain-shader.<br/> |



 

Inoltre, la sezione di riferimento copre molti nuovi elementi API per il modello di shader 5, tra cui: [attributi](d3d11-graphics-reference-sm5-attributes.md), [funzioni intrinseche](d3d11-graphics-reference-sm5-intrinsics.md), [oggetti e metodi dello shader model 5](d3d11-graphics-reference-sm5-objects.md)e [valori di sistema](d3d11-graphics-reference-sm5-system-values.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

