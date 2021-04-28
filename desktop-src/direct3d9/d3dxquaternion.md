---
description: 'Struttura D3DXQUATERNION (D3dx9math.h): descrive un quaternione.'
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: Struttura D3DXQUATERNION (D3dx9math.h)
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
ms.openlocfilehash: f67acc6389ce809c1aa5f4987d9502735fe61e49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115679"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a>Struttura D3DXQUATERNION (D3dx9math.h)

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

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente x.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente y.

</dd> <dt>

**Z**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente z.

</dd> <dt>

**w**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente w.

</dd> </dl>

## <a name="remarks"></a>Commenti

I quaternioni aggiungono un quarto elemento ai valori x, y, z che definiscono un vettore, con conseguente vettori \[ \] 4D arbitrari. Tuttavia, l'esempio seguente illustra come ogni elemento di un quaternione di unità è correlato a una rotazione asse-angolo (dove q rappresenta un quaternione unità (x, y, z, w), l'asse viene normalizzato e theta è la rotazione CCW desiderata intorno all'asse:


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



I programmatori C++ possono sfruttare l'overload degli operatori e il cast dei tipi con le estensioni [**D3DXQUATERNION**](d3dxquaternion-extensions.md), che implementano costruttori di overload e operatori di assegnazione, unario e binario (inclusa l'uguaglianza).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[Vettori, vertici e quaternioni (Direct3D 9)](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
