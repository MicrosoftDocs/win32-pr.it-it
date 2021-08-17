---
description: Struttura D3DXSHADER \_ CONSTANTINFO
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: D3DXSHADER_CONSTANTINFO struttura (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 34a9238ac7ab401a25874d65390ccfacb4dba68a9ccc4438500a1171e25e5e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122831"
---
# <a name="d3dxshader_constantinfo-structure"></a>Struttura D3DXSHADER \_ CONSTANTINFO

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio di questa struttura, in byte, alla stringa che contiene le informazioni sulle costanti.

</dd> <dt>

**RegisterSet**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Set di registri. Vedere [**D3DXREGISTER \_ SET**](./d3dxregister-set.md).

</dd> <dt>

**RegisterIndex**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Indice del registro.

</dd> <dt>

**RegisterCount**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di registri.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Riservato.

</dd> <dt>

**Typeinfo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio di questa struttura, in byte, alla stringa che contiene le informazioni [**\_ TYPEINFO D3DXSHADER.**](d3dxshader-typeinfo.md)

</dd> <dt>

**DefaultValue**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio di questa struttura, in byte, alla stringa che contiene il valore predefinito.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
