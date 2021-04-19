---
description: Richiama un altro shader dall'interno di uno shader.
ms.assetid: ''
title: CallShader (funzione)
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
ms.openlocfilehash: 8c5cdf4e0a71430d6375fd75ca553f92ca9539b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304707"
---
# <a name="callshader-function"></a>CallShader (funzione)

Richiama un altro shader dall'interno di uno shader.

## <a name="syntax"></a>Sintassi
Questa definizione di funzione intrinseca è equivalente al modello di funzione seguente:

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a>Parametri

`ShaderIndex`

Unsigned Integer che rappresenta l'indice nella tabella [shader chiamabile](callable-shader.md) specificata nella chiamata a [**DispatchRays**] (/Windows/Desktop/API/d3d12/NF-d3d12-id3d12graphicscommandlist4-dispatchrays.

`Parameter`

Parametri definiti dall'utente da passare allo shader chiamabile.  Questa struttura di parametri deve corrispondere alla struttura del parametro utilizzata nello shader chiamabile a cui punta la tabella shader.


## <a name="return-value"></a>Valore restituito

**void**

## <a name="remarks"></a>Commenti

Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:

* [**Richiamabile shader**](callable-shader.md)
* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Lo shader manca**](miss-shader.md)
* [**Shader di generazione del Ray**](ray-generation-shader.md)



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




