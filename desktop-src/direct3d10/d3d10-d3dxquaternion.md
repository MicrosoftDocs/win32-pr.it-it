---
description: Descrive un quaternione.
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: Struttura D3DXQUATERNION (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 405e48c99d7298708af193016930a8defdf9d600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355329"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a>Struttura D3DXQUATERNION (D3DX10Math. h)

Descrive un quaternione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a>Members

<dl> <dt>

**x**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente x.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente y.

</dd> <dt>

**z**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente z.

</dd> <dt>

**w**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Il componente w.

</dd> </dl>

## <a name="remarks"></a>Commenti

I quaternioni aggiungono un quarto elemento ai \[ valori x, y, z \] che definiscono un vettore, ottenendo vettori 4D arbitrari. Tuttavia, di seguito viene illustrato il modo in cui ogni elemento di un quaternione dell'unità è correlato a una rotazione dell'angolo dell'asse (dove q rappresenta un quaternione di unità (x, y, z, w), l'asse viene normalizzato e theta è la rotazione di CCW desiderata sull'asse):


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
