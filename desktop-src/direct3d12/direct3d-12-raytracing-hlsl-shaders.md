---
title: Shader HLSL Raytracing Direct3D 12
description: Visualizzare i collegamenti agli articoli che descrivono gli shader HLSL (High-Level Shader Language) che supportano la pipeline di raytracing Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca19081b1ea963851e82d18912153434c3e38d1
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394836"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a>Shader HLSL Raytracing Direct3D 12

Gli shader HLSL seguenti supportano la pipeline di raytracing Direct3D 12. Questi shader sono funzioni compilate in una libreria, con modello di destinazione lib_6_3 e identificati da un attributo *[shader("shadertype")]* nella funzione shader. Vedere **Intrinseci e** **valori di sistema** per vedere cosa è consentito per ogni tipo di shader.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                       | Descrizione                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Qualsiasi hit shader**](any-hit-shader.md)<br/>                              | Shader richiamato quando le intersezioni dei raggi non sono opache.<br/>                                                                                                                                                                                                                                              |
| [**Shader chiamabile**](callable-shader.md)<br/>                              | Shader richiamato da un altro shader con la funzione **intrinseca CallShader.**<br/>                                                                                                                                                                                                                                              |
| [**Hit shader più vicino**](closest-hit-shader.md)<br/>                              | Shader richiamato quando è abilitato ed è stato determinato l'hit più vicino o è terminata la ricerca di intersezione dei raggi.<br/>                                                                                                                                                                                                                                              |
| [**Intersection Shader**](intersection-shader.md)<br/>                              | Shader usato per implementare primitive di intersezione personalizzate per i raggi che intersecano un volume di delimitazione associato (rettangolo di selezione).<br/>                                                                                                                                                                                                                                              |
| [**Miss Shader**](miss-shader.md)<br/>                              | Shader richiamato quando non vengono trovate o accettate intersezioni di raggi.<br/>                                                                                                                                                                                                                                              |
| [**Ray Generation Shader**](ray-generation-shader.md)<br/>                              | Shader che chiama [**TraceRay per**](traceray-function.md) generare raggi.<br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento di base](direct3d-12-core-reference.md)
</dt> <dt>

[Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





