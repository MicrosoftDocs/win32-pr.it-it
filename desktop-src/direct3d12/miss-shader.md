---
description: Shader richiamato quando non vengono rilevate o accettate intersezioni di raggio.
ms.assetid: ''
title: Lo shader manca
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: fe8e2ec9cdbb8ef7567b9327ae5af1128597a601
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305246"
---
# <a name="miss-shader"></a>Lo shader manca

Shader richiamato quando non vengono rilevate o accettate intersezioni di raggio. Questa operazione è utile per l'ombreggiatura di background o Sky.  Lo shader mancante può usare [**CallShader**](callshader-function.md) e **TraceRay** per pianificare altre operazioni.

Il mancato shader deve includere un parametro di payload tipizzato della struttura definito dall'utente corrispondente a quello fornito a [**TraceRay**](traceray-function.md).


## <a name="shader-type-attribute"></a>Attributo di tipo shader


```
[shader("miss")]
```



## <a name="example"></a>Esempio

```
[shader("anyhit")]
void miss_main(inout MyPayload payload)
{
    // Use ray system values to compute contributions of background, sky, etc...
    // Combine contributions into ray payload
    CallShader( ... );  // if desired
    TraceRay( ... );    // if desired
    // this ray query is now complete
}

```

 

 




