---
description: Definisce le costanti che descrivono le modalità di ombreggiatura supportate.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: Enumerazione D3DSHADEMODE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9950e0074bef7a7b0c211177b3902cd69e2e112c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354539"
---
# <a name="d3dshademode-enumeration"></a>Enumerazione D3DSHADEMODE

Definisce le costanti che descrivono le modalità di ombreggiatura supportate.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ Flat**
</dt> <dd>

Modalità ombreggiatura piatta. Il colore e il componente speculare del primo vertice nel triangolo vengono utilizzati per determinare il colore e il componente speculare della faccia. Questi colori rimangono costanti nel triangolo; ovvero non vengono interpolate. Il Alpha speculare è interpolato. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**\_Gouraud D3DSHADE**
</dt> <dd>

Modalità di ombreggiatura Gouraud. Il colore e i componenti speculari della faccia sono determinati da un'interpolazione lineare tra tutti e tre i vertici del triangolo.

</dd> <dt>

<span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ Phong**
</dt> <dd>

Non supportata.

</dd> <dt>

<span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il primo vertice di un triangolo per la modalità ombreggiatura piatta viene definito nel modo seguente.

-   Per un elenco di triangolo, il primo vertice del triangolo i è \* 3.
-   Per una striscia di triangolo, il primo vertice del triangolo i è Vertex i.
-   Per una ventola del triangolo, il primo vertice del triangolo i è vertice i + 1.

I membri di questo tipo enumerato definiscono i vale per lo stato di \_ rendering MODOOMBRA di D3DRS.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
