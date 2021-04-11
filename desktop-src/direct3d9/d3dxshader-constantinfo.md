---
description: '\_Struttura D3DXSHADER CONSTANTINFO'
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: Struttura D3DXSHADER_CONSTANTINFO (D3dx9shader. h)
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
ms.openlocfilehash: e90c0085035e78b9bc3ce1c48642157d8badc924
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235000"
---
# <a name="d3dxshader_constantinfo-structure"></a>\_Struttura D3DXSHADER CONSTANTINFO

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

Offset dall'inizio della struttura, in byte, alla stringa che contiene le informazioni sulle costanti.

</dd> <dt>

**Registro**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Set di registrazione. Vedere [**D3DXREGISTER \_ set**](./d3dxregister-set.md).

</dd> <dt>

**RegisterIndex**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Indice del registro.

</dd> <dt>

**RegisterCount**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di registri.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Riservato.

</dd> <dt>

**TypeInfo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio della struttura, in byte, alla stringa che contiene le informazioni di [**\_ TYPEINFO D3DXSHADER**](d3dxshader-typeinfo.md) .

</dd> <dt>

**DefaultValue**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio della struttura, in byte, alla stringa che contiene il valore predefinito.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
