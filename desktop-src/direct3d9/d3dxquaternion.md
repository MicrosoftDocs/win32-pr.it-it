---
description: Descrive un quaternione.
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: Struttura D3DXQUATERNION (D3dx9math. h)
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
- d3dx9math.h
ms.openlocfilehash: 59d3f147e8eb233b9197394bad738d19d9ceba5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322499"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a>Struttura D3DXQUATERNION (D3dx9math. h)

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



I programmatori C++ possono sfruttare l'overload degli operatori e il cast dei tipi con le [**estensioni D3DXQUATERNION**](d3dxquaternion-extensions.md), che implementano costruttori di overload e operatori di assegnazione, unario e binari (inclusi uguaglianza).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[Vettori, vertici e quaternioni (Direct3D 9)](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
