---
description: Struttura D3DXSHPRTSPLITMESHVERTDATA
ms.assetid: 8799a680-bf5f-42cc-91aa-1a6aed164ca5
title: Struttura D3DXSHPRTSPLITMESHVERTDATA (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHVERTDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 55424929a3d415fc1b89f7a1af53be849cf90185
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762023"
---
# <a name="d3dxshprtsplitmeshvertdata-structure"></a>Struttura D3DXSHPRTSPLITMESHVERTDATA

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXSHPRTSPLITMESHVERTDATA {
  UINT uVertRemap;
  UINT uSubCluster;
  UINT ucVertStatus;
} D3DXSHPRTSPLITMESHVERTDATA, *LPD3DXSHPRTSPLITMESHVERTDATA;
```



## <a name="members"></a>Members

<dl> <dt>

**uVertRemap**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Vertice nella mesh originale a cui corrisponde.

</dd> <dt>

**uSubCluster**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Indice del cluster, relativo al Supercluster.

</dd> <dt>

**ucVertStatus**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

1 se il vertice contiene dati validi, 0 se è "full".

</dd> </dl>

## <a name="remarks"></a>Commenti

Allocato in [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
