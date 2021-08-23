---
description: 'Struttura D3DXQUATERNION (D3DX10Math.h): descrive un quaternione.'
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: Struttura D3DXQUATERNION (D3DX10Math.h)
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
ms.openlocfilehash: be04aa9345f8a5b932d1697dbd85c8f81072bd3087077163d4891b1c19aafbe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991161"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a>Struttura D3DXQUATERNION (D3DX10Math.h)

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

**z**
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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
