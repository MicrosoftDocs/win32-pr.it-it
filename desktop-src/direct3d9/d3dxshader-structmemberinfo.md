---
description: Struttura di supporto che contiene informazioni sulla struttura del membro.
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: Struttura D3DXSHADER_STRUCTMEMBERINFO (D3dx9shader. h)
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
ms.openlocfilehash: 01782331459956c0878b46861db0d4f11e19c7dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354624"
---
# <a name="d3dxshader_structmemberinfo-structure"></a>\_Struttura D3DXSHADER STRUCTMEMBERINFO

Struttura di supporto che contiene informazioni sulla struttura del membro.

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

Offset dall'inizio della struttura, in byte, alla stringa che contiene il nome del membro della struttura.

</dd> <dt>

**TypeInfo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio della struttura, in byte, alla stringa che contiene le informazioni sul tipo. Vedere [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**\_TYPEINFO D3DXSHADER**](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
