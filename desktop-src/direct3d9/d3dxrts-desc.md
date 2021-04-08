---
description: Descrive una superficie di rendering.
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: Struttura D3DXRTS_DESC (D3dx9core. h)
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
ms.openlocfilehash: 3a0b52f258956f7b62734ca97cc5d1bf5ed00ac3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969345"
---
# <a name="d3dxrts_desc-structure"></a>\_Struttura D3DXRTS DESC

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza della superficie di rendering, in pixel.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza della superficie di rendering, in pixel.

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel della superficie di rendering.

</dd> <dt>

**DepthStencil**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Se **true**, la superficie di rendering supporta una superficie di stencil profondità; in caso contrario, questo membro è impostato su **false**.

</dd> <dt>

**DepthStencilFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Se DepthStencil è impostato su **true**, questo parametro è un membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato di stencil depth della superficie di rendering.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**ID3DXRenderToSurface:: getdesc**](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
