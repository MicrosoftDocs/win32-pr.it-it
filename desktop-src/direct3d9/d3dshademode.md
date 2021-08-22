---
description: Definisce costanti che descrivono le modalità di ombreggiatura supportate.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: Enumerazione D3DSHADEMODE (D3d9types.h)
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
ms.openlocfilehash: 6a8c937000912eb203986bed4889785b9484afec7682418aed43fcc58c438e58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241561"
---
# <a name="d3dshademode-enumeration"></a>Enumerazione D3DSHADEMODE

Definisce costanti che descrivono le modalità di ombreggiatura supportate.

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

<span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ FLAT**
</dt> <dd>

Modalità ombreggiatura flat. Il colore e il componente speculare del primo vertice del triangolo vengono usati per determinare il colore e il componente speculare del viso. Questi colori rimangono costanti sul triangolo; in altri, non sono interpolati. Il valore alfa speculare è interpolato. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE \_ GOURAUD**
</dt> <dd>

Modalità ombreggiatura gouraud. Il colore e i componenti speculari del viso sono determinati da un'interpolazione lineare tra tutti e tre i vertici del triangolo.

</dd> <dt>

<span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ PHONG**
</dt> <dd>

Non supportata.

</dd> <dt>

<span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il primo vertice di un triangolo per la modalità ombreggiatura piatta è definito nel modo seguente.

-   Per un elenco di triangoli, il primo vertice del triangolo i è i \* 3.
-   Per una striscia triangolare, il primo vertice del triangolo i è vertice i.
-   Per una ventola triangolare, il primo vertice del triangolo i è vertice i + 1.

I membri di questo tipo enumerato definiscono le vales per lo stato di rendering D3DRS \_ SHADEMODE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
