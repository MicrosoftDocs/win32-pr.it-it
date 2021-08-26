---
description: Descrive un subset della mesh con la stessa combinazione di attributo e osso.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: Struttura D3DXBONECOMBINATION (D3dx9mesh.h)
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
ms.openlocfilehash: 72d60b5c87d43763be4700ba7931c61c41cf0101d80390afb737c7f4afda83a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952491"
---
# <a name="d3dxbonecombination-structure"></a>Struttura D3DXBONECOMBINATION

Descrive un subset della mesh con la stessa combinazione di attributo e osso.

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

Viso iniziale.

</dd> <dt>

**FaceCount**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di viso.

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

Numero di vertici.

</dd> <dt>

**Id di base**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Puntatore a una matrice di valori che identificano ogni osso che può essere disegnato in una singola chiamata di disegno. Si noti che la matrice può essere di lunghezza variabile per supportare le combinazioni di osso a lunghezza variabile [**di ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).

Le dimensioni della matrice variano in base al tipo di mesh generato. Le dimensioni di una matrice mesh non indicizzata sono uguali al numero di pesi per vertice (pMaxVertexInfl in [**ConvertToBlendedMesh).**](id3dxskininfo--converttoblendedmesh.md) Le dimensioni di una matrice mesh indicizzata sono uguali al numero di voci del riquadro della matrice di osso (paletteSize in [**ConvertToIndexedBlendedMesh).**](id3dxskininfo--converttoindexedblendedmesh.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Il subset della mesh descritto da **D3DXBONECOMBINATION** può essere sottoposto a rendering in una singola chiamata di disegno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
