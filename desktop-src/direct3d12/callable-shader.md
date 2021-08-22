---
description: Shader richiamato da un altro shader con la funzione intrinseca CallShader.
ms.assetid: ''
title: Shader chiamabile
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
ms.openlocfilehash: b84ec6ea58fbc456db1747259f687a2fb6c8cb0fe3374b3d32396861dcd2f9b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461071"
---
# <a name="callable-shader"></a>Shader chiamabile

Shader richiamato da un altro shader con la funzione [**intrinseca CallShader.**](callshader-function.md)

Nel sito di chiamata **CallShader** è disponibile una struttura di parametri che deve corrispondere alla struttura dei parametri usata nello shader chiamabile a cui punta l'indice richiesto nella tabella di shader chiamabile fornita tramite il [**metodo DispatchRays.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays)  Lo shader chiamabile deve dichiarare questo parametro *come inout*.  Inoltre, lo shader chiamabile può leggere gli input dell'indice di avvio e della dimensione. Per altre informazioni, vedere [**Intrinseci dei valori di sistema.**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md) 


## <a name="shader-type-attribute"></a>Attributo Tipo shader


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

 

 




