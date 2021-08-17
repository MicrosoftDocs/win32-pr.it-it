---
title: Shader HLSL Direct3D 12 Raytracing
description: Visualizzare i collegamenti ad articoli che descrivono shader HLSL (High-Level Shader Language) che supportano la pipeline di raytracing Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc2321511be2ef912a6dce6710b233cb59dcc7712e9e8f63db890d8707822c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733774"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a>Shader HLSL Direct3D 12 Raytracing

Gli shader HLSL seguenti supportano la pipeline di raytracing Direct3D 12. Questi shader sono funzioni compilate in una libreria, con modello di destinazione lib_6_3 e identificate da un attributo *[shader("shadertype")]* nella funzione shader. Vedere **Intrinseci e** **Valori di sistema** per vedere cosa è consentito per ogni tipo di shader.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                       | Descrizione                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Qualsiasi hit shader**](any-hit-shader.md)<br/>                              | Shader richiamato quando le intersezioni di raggi non sono opache.<br/>                                                                                                                                                                                                                                              |
| [**Shader chiamabile**](callable-shader.md)<br/>                              | Shader richiamato da un altro shader con la funzione **intrinseca CallShader.**<br/>                                                                                                                                                                                                                                              |
| [**Hit Shader più vicino**](closest-hit-shader.md)<br/>                              | Shader richiamato quando è abilitato ed è stato determinato l'hit più vicino o la ricerca dell'intersezione dei raggi è terminata.<br/>                                                                                                                                                                                                                                              |
| [**Shader di intersezione**](intersection-shader.md)<br/>                              | Shader usato per implementare primitive di intersezione personalizzate per i raggi che intersecano un volume di delimitazione associato (rettangolo di selezione).<br/>                                                                                                                                                                                                                                              |
| [**Miss Shader**](miss-shader.md)<br/>                              | Shader richiamato quando non vengono trovate o accettate intersezioni di raggi.<br/>                                                                                                                                                                                                                                              |
| [**Shader di generazione di raggi**](ray-generation-shader.md)<br/>                              | Shader che chiama [**TraceRay per**](traceray-function.md) generare raggi.<br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento di base](direct3d-12-core-reference.md)
</dt> <dt>

[Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





