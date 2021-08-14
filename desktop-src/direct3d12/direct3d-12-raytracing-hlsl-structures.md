---
title: Strutture HLSL raytracing (Direct3D 12)
description: Le strutture HLSL seguenti supportano la pipeline di raytracing Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c4227c2a0a1c99929a1025d0410ba6c769c932a740d6ed0a6c4b5f721f3fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045549"
---
# <a name="raytracing-hlsl-structures-direct3d-12"></a>Strutture HLSL raytracing (Direct3D 12)

Le strutture HLSL seguenti supportano la pipeline di raytracing Direct3D 12.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                       | Descrizione                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Struttura dei parametri di chiamata**](call-parameter-structure.md)<br/>                              | Struttura definita dall'utente fornita come argomento inout per una chiamata CallShader e come parametro inout per lo shader chiamabile.<br/>                                                                                                                                                                                                                                              |
| [**Struttura degli attributi di intersezione**](intersection-attributes.md)<br/>                              | Struttura definita dall'utente fornita come argomento inout in una chiamata [**TraceRay**](traceray-function.md) e come parametro inout nei tipi shader che possono accedere al payload ray.<br/>                                                                                                                                                                                                                                              |
| [**Struttura del payload ray**](ray-payload.md)<br/>                              | Struttura definita dall'utente fornita come argomento inout in una chiamata [**TraceRay**](traceray-function.md) e come parametro inout nei tipi shader che possono accedere al payload ray.<br/>                                                                                                                                                                                                                                              |
| [**Struttura RayDesc**](raydesc.md)<br/>                              | Flag passati alla [**funzione TraceRay**](traceray-function.md) per eseguire l'override di trasparenza, culling e comportamento di pre-out.<br/>                                                                                                                                                                                                                                              |





 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento di base](direct3d-12-core-reference.md)
</dt> <dt>

[Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





