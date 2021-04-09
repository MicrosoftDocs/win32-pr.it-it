---
description: Descrive un subset della mesh con lo stesso attributo e la stessa combinazione di osso.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: Struttura D3DXBONECOMBINATION (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 3553ba37d0d9376fa5912143fb58849f03c5a83a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058625"
---
# <a name="d3dxbonecombination-structure"></a>Struttura D3DXBONECOMBINATION

Descrive un subset della mesh con lo stesso attributo e la stessa combinazione di osso.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a>Members

<dl> <dt>

**AttribId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificatore della tabella degli attributi.

</dd> <dt>

**FaceStart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Faccia iniziale.

</dd> <dt>

**FaceCount**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Conteggio delle facce.

</dd> <dt>

**VertexStart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Vertice iniziale.

</dd> <dt>

**VertexCount**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Conteggio vertici.

</dd> <dt>

**BoneId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Puntatore a una matrice di valori che identificano ognuno degli ossicini che possono essere disegnati in una singola chiamata di disegno. Si noti che la matrice può avere una lunghezza variabile per supportare combinazioni di lunghezza variabile di [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).

Le dimensioni della matrice variano in base al tipo di mesh generato. Una dimensione della matrice di mesh non indicizzata è uguale al numero di pesi per vertice (pMaxVertexInfl in [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)). Una dimensione della matrice di mesh indicizzata è uguale al numero di voci della tavolozza della matrice ossea (paletteSize in [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile eseguire il rendering del subset della mesh descritta da **D3DXBONECOMBINATION** in una singola chiamata di disegno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
