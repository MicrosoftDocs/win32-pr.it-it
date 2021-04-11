---
description: Struttura di supporto che contiene informazioni sul tipo di membro.
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: Struttura D3DXSHADER_TYPEINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354714"
---
# <a name="d3dxshader_typeinfo-structure"></a>\_Struttura D3DXSHADER TYPEINFO

Struttura di supporto che contiene informazioni sul tipo di membro.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Classe**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo di oggetto shader. Vedere [**la \_ classe D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo di dati. Vedere [**D3DXPARAMETER \_ Type**](./d3dxparameter-type.md).

</dd> <dt>

**prime righe**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di righe matrice (matrici).

</dd> <dt>

**Colonne**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di colonne (vettori e matrici).

</dd> <dt>

**Elementi**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensione della matrice.

</dd> <dt>

**StructMembers**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di membri della struttura.

</dd> <dt>

**StructMemberInfo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matrice di informazioni sui membri di struttura, D3DXSHADER \_ STRUCTMEMBERINFO \[ *StructMembers* \] . Vedere [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Le informazioni sul tipo fanno parte di [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**\_CONSTANTINFO D3DXSHADER**](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
