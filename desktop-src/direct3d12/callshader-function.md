---
description: Richiama un altro shader dall'interno di uno shader.
ms.assetid: ''
title: Funzione CallShader
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: e411ef61c34eafcef71f3e68f6700651e4b3073423afd40451f139f02826e504
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119280351"
---
# <a name="callshader-function"></a>Funzione CallShader

Richiama un altro shader dall'interno di uno shader.

## <a name="syntax"></a>Sintassi
Questa definizione di funzione intrinseca equivale al modello di funzione seguente:

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a>Parametri

`ShaderIndex`

Intero senza segno che rappresenta l'indice nella tabella [shader](callable-shader.md) chiamabile specificata nella chiamata a [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays.

`Parameter`

Parametri definiti dall'utente da passare allo shader chiamabile.  Questa struttura dei parametri deve corrispondere alla struttura dei parametri usata nello shader chiamabile a cui punta nella tabella shader.


## <a name="return-value"></a>Valore restituito

**void**

## <a name="remarks"></a>Commenti

Questa funzione può essere chiamata dai tipi di shader raytracing seguenti:

* [**Shader chiamabile**](callable-shader.md)
* [**Hit Shader più vicino**](closest-hit-shader.md)
* [**Miss Shader**](miss-shader.md)
* [**Shader di generazione di raggi**](ray-generation-shader.md)



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su Direct3D 12 Raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




