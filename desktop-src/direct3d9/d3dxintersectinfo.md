---
description: "Struttura D3DXINTERSECTINFO: descrive un'intersezione di raggio-triangolo."
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: Struttura D3DXINTERSECTINFO (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINTERSECTINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6d7915178001e2449d385484dc23d206a126734cbd1a5074facca8b97c760a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525638"
---
# <a name="d3dxintersectinfo-structure"></a>Struttura D3DXINTERSECTINFO

Descrive l'intersezione di un triangolo di raggio.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**FaceIndex**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Indice del triangolo che ha raggiunto il raggio.

</dd> <dt>

**U**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata barycentrica all'interno del triangolo in cui si interseca il raggio.

</dd> <dt>

**V**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata barycentrica all'interno del triangolo in cui si interseca il raggio.

</dd> <dt>

**Dist**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Distanza lungo il raggio in cui si è verificata l'intersezione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più dettagliata delle coordinate barycentric, vedere Descrizione delle [coordinate barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
