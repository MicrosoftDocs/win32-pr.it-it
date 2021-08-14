---
description: Struttura helper contenente informazioni sulla struttura dei membri.
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: D3DXSHADER_STRUCTMEMBERINFO struttura (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 6f41c3d1911a046165d929bee50ef4e0b5691cebee9d90007bc367636e343731
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524214"
---
# <a name="d3dxshader_structmemberinfo-structure"></a>Struttura \_ STRUCTMEMBERINFO D3DXSHADER

Struttura helper contenente informazioni sulla struttura dei membri.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio di questa struttura, in byte, alla stringa che contiene il nome del membro della struttura.

</dd> <dt>

**Typeinfo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio di questa struttura, in byte, alla stringa che contiene le informazioni sul tipo. Vedere [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
