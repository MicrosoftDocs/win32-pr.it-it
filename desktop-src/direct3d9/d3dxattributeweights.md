---
description: Specifica gli attributi di peso mesh.
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: Struttura D3DXATTRIBUTEWEIGHTS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 49725e410fb700c7ecb93fd56a8db367d7f982a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322889"
---
# <a name="d3dxattributeweights-structure"></a>Struttura D3DXATTRIBUTEWEIGHTS

Specifica gli attributi di peso mesh.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="members"></a>Members

<dl> <dt>

**Position**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione.

</dd> <dt>

**Limite**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Spessore di Blend.

</dd> <dt>

**Normal**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Normale.

</dd> <dt>

**Diffusa**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore di illuminazione diffuso.

</dd> <dt>

**Speculare**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore di illuminazione speculare.

</dd> <dt>

**Texcoord**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Otto coordinate di trama.

</dd> <dt>

**Tangente**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangente.

</dd> <dt>

**Binormale**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura descrive il modo in cui un'operazione di semplificazione considererà i dati dei vertici quando si calcolano i costi relativi tra i bordi. Se, ad esempio, il campo normale è 0,0, l'operazione di semplificazione ignorerà il componente normale vertice durante il calcolo dell'errore per la compressione. Tuttavia, se il campo normale è 1,0, l'operazione di semplificazione utilizzerà il componente normale vertice. Se il campo normale è 2,0, raddoppiare la quantità di errori; Se il campo normale è 4,0, moltiplicare il numero di errori e così via.

Il tipo LPD3DXATTRIBUTEWEIGHTS è definito come un puntatore alla struttura **D3DXATTRIBUTEWEIGHTS** .


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSimplifyMesh**](d3dxsimplifymesh.md)
</dt> </dl>

 

 
