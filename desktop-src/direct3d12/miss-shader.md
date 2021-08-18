---
description: Shader richiamato quando non vengono trovate o accettate intersezioni di raggi.
ms.assetid: ''
title: Miss Shader
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
ms.openlocfilehash: 30f7ce32e66a19984ce43737d9fc9cae83652c851174d7db350ca34628a33033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850824"
---
# <a name="miss-shader"></a>Miss Shader

Shader richiamato quando non vengono trovate o accettate intersezioni di raggi. Ciò è utile per l'ombreggiatura dello sfondo o del cielo.  Lo shader miss può usare [**CallShader**](callshader-function.md) e **TraceRay** per pianificare più lavoro.

Lo shader miss deve includere un parametro di payload tipico della struttura definito dall'utente corrispondente a quello fornito a [**TraceRay.**](traceray-function.md)


## <a name="shader-type-attribute"></a>Attributo Tipo shader


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

 

 




