---
title: Modello Shader 5
description: Questa sezione contiene le pagine di riferimento per HLSL Shader Model 5.
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f379301008190367a40959a319d01cfad127f6b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399221"
---
# <a name="shader-model-5"></a>Modello Shader 5

Questa sezione contiene le pagine di riferimento per HLSL Shader Model 5.

Shader Model 5 è un superset di funzionalità in [Shader Model 4](dx-graphics-hlsl-sm4.md). È stato progettato usando un core di shader comune che fornisce un set comune di funzionalità a tutti gli shader programmabili, che sono programmabili solo con HLSL.



| Caratteristica                   | Funzionalità                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Set di istruzioni           | [**Funzioni intrinseche HLSL**](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| Vertex shader max         | Nessuna restrizione                                                                                                                                         |
| Pixel shader max          | Nessuna restrizione                                                                                                                                         |
| Nuovi profili shader aggiunti | cs \_ 4 \_ 0, GS \_ 4 \_ 0 \* , PS \_ 4 \_ 0 \* , vs \_ 4 \_ 0, \* cs \_ 4 \_ 1, GS \_ 4 \_ 1 \* , PS \_ 4 \_ 1 \* , vs \_ 4 \_ 1 \* , cs \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 \_ 0, vs \_ 5 \_ 0 |



 

\* -GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 e vs \_ 4 \_ 1 sono stati introdotti nel modello Shader 4,0, tuttavia, DirectX 11 aggiunge il supporto per [buffer strutturati](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) e buffer di indirizzi di byte al modello Shader 4 in esecuzione su hardware DirectX 10.

Shader Model 5 introduce il [compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) che fornisce un calcolo ad alta velocità per utilizzo generico.

Un elenco più completo delle funzionalità di Shader Model 5 è incluso in un elenco delle [funzionalità di Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features).

La sezione di [assembly Shader Model 5](shader-model-5-assembly--directx-hlsl-.md) descrive le istruzioni di assembly supportate dal modello di shader 5.

## <a name="in-this-section"></a>Contenuto della sezione



| Elemento                                                                                                                                                                                                                                                        | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Attributi del modello di shader 5](d3d11-graphics-reference-sm5-attributes.md)<br/>                                     | Pagine di riferimento per gli attributi dello shader model 5.<br/>          |
| <span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Funzioni intrinseche del modello shader 5](d3d11-graphics-reference-sm5-intrinsics.md)<br/> | Pagine di riferimento per le funzioni intrinseche del modello shader 5.<br/> |
| <span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Oggetti Shader Model 5](d3d11-graphics-reference-sm5-objects.md)<br/>                                                    | Pagine di riferimento per oggetti e metodi dello shader model 5.<br/> |
| <span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Valori di sistema di Shader Model 5](d3d11-graphics-reference-sm5-system-values.md)<br/>                      | Pagine di riferimento per i valori del sistema Shader Model 5.<br/>       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modelli shader rispetto ai profili shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

