---
title: Shader HLSL raytracing Direct3D 12
description: Gli shader HLSL seguenti supportano la pipeline raytracing di Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1dd545532208095781f6fbca25480a6dbfd31e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300884"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a>Shader HLSL raytracing Direct3D 12

Gli shader HLSL seguenti supportano la pipeline raytracing di Direct3D 12. Questi shader sono funzioni compilate in una libreria, con il modello di destinazione lib_6_3 e identificati da un attributo *[shader ("shadertype")]* nella funzione shader. Vedere elementi **intrinseci** e **valori di sistema** per vedere cosa è consentito per ogni tipo di shader.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                       | Descrizione                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Qualsiasi hit shader**](any-hit-shader.md)<br/>                              | Shader richiamato quando le intersezioni del raggio non sono opache.<br/>                                                                                                                                                                                                                                              |
| [**Richiamabile shader**](callable-shader.md)<br/>                              | Shader richiamato da un altro shader con la funzione intrinseca **CallShader** .<br/>                                                                                                                                                                                                                                              |
| [**Hit shader più vicino**](closest-hit-shader.md)<br/>                              | Uno shader che viene richiamato quando è abilitato e l'hit più vicino è stato determinato o la ricerca di intersezione del raggio è terminata.<br/>                                                                                                                                                                                                                                              |
| [**Intersezione shader**](intersection-shader.md)<br/>                              | Shader utilizzato per implementare primitive di intersezione personalizzate per i raggi che intersecano un volume di delimitazione associato (rettangolo di delimitazione).<br/>                                                                                                                                                                                                                                              |
| [**Lo shader manca**](miss-shader.md)<br/>                              | Shader richiamato quando non vengono rilevate o accettate intersezioni di raggio.<br/>                                                                                                                                                                                                                                              |
| [**Shader di generazione del Ray**](ray-generation-shader.md)<br/>                              | Shader che chiama [**TraceRay**](traceray-function.md) per generare raggi.<br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento principale](direct3d-12-core-reference.md)
</dt> <dt>

[Guida di riferimento a Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





