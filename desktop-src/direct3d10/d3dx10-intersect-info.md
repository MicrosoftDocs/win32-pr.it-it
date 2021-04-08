---
description: Descrive un'intersezione tra i triangoli.
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: Struttura D3DX10_INTERSECT_INFO (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_INTERSECT_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 87490e734299cba57952bb43d1ee4ffad8e014c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762113"
---
# <a name="d3dx10_intersect_info-structure"></a>\_ \_ Struttura info Intersect d3dx10

Descrive un'intersezione tra i triangoli.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**FaceIndex**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Indice del triangolo che raggiunge il raggio.

</dd> <dt>

**U**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata baricentrica all'interno del triangolo in cui si interseca il raggio.

</dd> <dt>

**V**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata baricentrica all'interno del triangolo in cui si interseca il raggio.

</dd> <dt>

**Dist**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Distanza lungo il raggio in cui si è verificata l'intersezione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
