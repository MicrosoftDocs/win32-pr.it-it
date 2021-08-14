---
description: Struttura D3DXSHPRTSPLITMESHCLUSTERDATA
ms.assetid: 6a53420c-06bc-4f52-ac2e-5adda5e34cb2
title: Struttura D3DXSHPRTSPLITMESHCLUSTERDATA (D3dx9mesh.h)
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
ms.openlocfilehash: c4405b383e0403326c3cb84f43c97f4c7da826872b62cb21c94b3edb9ef0e475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298290"
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

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Vertice iniziale in matrice di vertici mappata nuovamente.

</dd> <dt>

**uVertLength**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di vertici in questo supercluster.

</dd> <dt>

**uFaceStart**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Indice iniziale nella matrice del viso.

</dd> <dt>

**uFaceLength**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di visi in questo supercluster.

</dd> <dt>

**uClusterStart**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Indice iniziale nell'array cluster.

</dd> <dt>

**uClusterLength**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di cluster in questa matrice di cluster supercluster.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md)
</dt> </dl>

 

 
