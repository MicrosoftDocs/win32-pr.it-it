---
description: 'Struttura D3DXATTRIBUTEWEIGHTS: specifica gli attributi del peso della mesh.'
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: Struttura D3DXATTRIBUTEWEIGHTS (D3dx9mesh.h)
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
ms.openlocfilehash: 7a833d2a58db0f434f836126926e461cd2ee3ea0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115969"
---
# <a name="d3dxattributeweights-structure"></a>Struttura D3DXATTRIBUTEWEIGHTS

Specifica gli attributi del peso della mesh.

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

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione.

</dd> <dt>

**Limite**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Spessore della blend.

</dd> <dt>

**Normal**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Normale.

</dd> <dt>

**Diffusa**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore di illuminazione diffusa.

</dd> <dt>

**Speculare**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore di illuminazione speculare.

</dd> <dt>

**Texcoord**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Otto coordinate di trama.

</dd> <dt>

**Tangente**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangente.

</dd> <dt>

**Binormale**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura descrive in che modo un'operazione di semplificazione considererà i dati dei vertici durante il calcolo dei costi relativi tra gli bordi che comprimono. Ad esempio, se il campo Normale è 0,0, l'operazione di semplificazione ignorerà il componente normale del vertice durante il calcolo dell'errore per la compressione. Tuttavia, se il campo Normal è 1.0, l'operazione di semplificazione userà il componente normale del vertice. Se il campo Normale è 2,0, raddoppiare la quantità di errori. se il campo Normal è 4.0, quadruplicare il numero di errori e così via.

Il tipo LPD3DXATTRIBUTEWEIGHTS è definito come puntatore alla **struttura D3DXATTRIBUTEWEIGHTS.**


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSimplifyMesh**](d3dxsimplifymesh.md)
</dt> </dl>

 

 
