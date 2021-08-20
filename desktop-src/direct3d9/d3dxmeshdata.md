---
description: Struttura dei dati della mesh.
ms.assetid: 9164b956-95b7-4bc0-bf7e-feed2e3b4a2b
title: Struttura D3DXMESHDATA (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATA
api_type:
- HeaderDef
api_location:
- D3dx9anim.h
ms.openlocfilehash: ba2f4df1b5234103916929d85dca24153b2f08b882e8566094276a9514699cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095532"
---
# <a name="d3dxmeshdata-structure"></a>Struttura D3DXMESHDATA

Struttura dei dati della mesh.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXMESHDATA {
  D3DXMESHDATATYPE Type;
  union {
    LPD3DXMESH      pMesh;
    LPD3DXPATCHMESH pPatchMesh;
  };
} D3DXMESHDATA, *LPD3DXMESHDATA;
```



## <a name="members"></a>Members

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**

</dd> <dd>

Definisce il tipo di dati mesh. Vedere [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).

</dd> <dt>

**pMesh**
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

</dd> <dd>

Puntatore a una mesh. Vedere [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

**pPatchMesh**
</dt> <dd>

Tipo: **LPD3DXPATCHMESH**

</dd> <dd>

Puntatore a una mesh di patch. Vedere [**ID3DXPatchMesh**](id3dxpatchmesh.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)
</dt> </dl>

 

 
