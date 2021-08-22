---
description: Descrive una superficie di rendering.
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: D3DXRTS_DESC struttura (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 838fc7d08eff0889049e7f0c73ae779239934e49049948b926fa956eeac3d40a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607631"
---
# <a name="d3dxrts_desc-structure"></a>Struttura DESC D3DXRTS \_

Descrive una superficie di rendering.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXRTS_DESC {
  UINT      Width;
  UINT      Height;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTS_DESC, *LPD3DXRTS_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza della superficie di rendering, in pixel.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza della superficie di rendering, in pixel.

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membro del tipo [enumerato D3DFORMAT,](d3dformat.md) che descrive il formato pixel della superficie di rendering.

</dd> <dt>

**DepthStencil**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Se **TRUE,** la superficie di rendering supporta una superficie depth-stencil; in caso contrario, questo membro è impostato su **FALSE.**

</dd> <dt>

**DepthStencilFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Se DepthStencil è impostato su **TRUE,** questo parametro è un membro del tipo enumerato [D3DFORMAT,](d3dformat.md) che descrive il formato depth-stencil della superficie di rendering.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9core.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**ID3DXRenderToSurface::GetDesc**](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
