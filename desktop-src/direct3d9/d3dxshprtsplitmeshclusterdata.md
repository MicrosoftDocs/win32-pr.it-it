---
description: Struttura D3DXSHPRTSPLITMESHCLUSTERDATA
ms.assetid: 6a53420c-06bc-4f52-ac2e-5adda5e34cb2
title: Struttura D3DXSHPRTSPLITMESHCLUSTERDATA (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHCLUSTERDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7b1bc23606dbf08f5a924860e12c9c09d719287
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322473"
---
# <a name="d3dxshprtsplitmeshclusterdata-structure"></a>Struttura D3DXSHPRTSPLITMESHCLUSTERDATA

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXSHPRTSPLITMESHCLUSTERDATA {
  UINT uVertStart;
  UINT uVertLength;
  UINT uFaceStart;
  UINT uFaceLength;
  UINT uClusterStart;
  UINT uClusterLength;
} D3DXSHPRTSPLITMESHCLUSTERDATA, *LPD3DXSHPRTSPLITMESHCLUSTERDATA;
```



## <a name="members"></a>Members

<dl> <dt>

**uVertStart**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Vertice iniziale in una matrice di vertici con mapping.

</dd> <dt>

**uVertLength**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di vertici in questo Supercluster.

</dd> <dt>

**uFaceStart**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Indice iniziale nella matrice della superficie.

</dd> <dt>

**uFaceLength**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di visi in questo Supercluster.

</dd> <dt>

**uClusterStart**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Indice iniziale nella matrice del cluster.

</dd> <dt>

**uClusterLength**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di cluster in questa matrice di Supercluster.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md)
</dt> </dl>

 

 
