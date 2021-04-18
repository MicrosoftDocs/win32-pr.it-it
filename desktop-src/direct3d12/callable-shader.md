---
description: Shader richiamato da un altro shader con la funzione intrinseca CallShader.
ms.assetid: ''
title: Richiamabile shader
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- Callable Shader
api_type:
- NA
ms.openlocfilehash: 65df547c5e40a46cc4c35361b88ceb797c2e8852
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304595"
---
# <a name="callable-shader"></a>Richiamabile shader

Shader richiamato da un altro shader con la funzione intrinseca [**CallShader**](callshader-function.md) .

Nel sito di chiamata **CallShader** è presente una struttura di parametri che deve corrispondere alla struttura del parametro utilizzata nello shader chiamabile a cui fa riferimento l'indice richiesto nella tabella shader chiamabile fornita tramite il metodo [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) .  Lo shader chiamabile deve dichiarare questo parametro come *InOut*.  Inoltre, il Callable shader può leggere gli input dell'indice di avvio e della dimensione. Per ulteriori informazioni, vedere [**intrinseci dei valori di sistema**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md). 


## <a name="shader-type-attribute"></a>Attributo di tipo shader


```
[shader("callable")]
```



## <a name="example"></a>Esempio

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 




