---
description: Struttura D3DXSHPRTSPLITMESHVERTDATA
ms.assetid: 8799a680-bf5f-42cc-91aa-1a6aed164ca5
title: Struttura D3DXSHPRTSPLITMESHVERTDATA (D3dx9mesh.h)
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
ms.openlocfilehash: cc32ee70cd1685351f8cca8860d9d45ab4ea597affed2fbe7cf078d44a8ed437
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027061"
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

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Vertice nella mesh originale a cui corrisponde.

</dd> <dt>

**uSubCluster**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Indice cluster, relativo al supercluster.

</dd> <dt>

**ucVertStatus**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

1 se il vertice contiene dati validi, 0 se è "completo".

</dd> </dl>

## <a name="remarks"></a>Commenti

Allocato in [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
