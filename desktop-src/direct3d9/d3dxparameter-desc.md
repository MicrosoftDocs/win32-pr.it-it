---
description: Descrive un parametro usato per un oggetto effetto.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: Struttura D3DXPARAMETER_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 2256e24daa6dc8b6e5da1528e9a5e5aefce8ec99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234941"
---
# <a name="d3dxparameter_desc-structure"></a>\_Struttura D3DXPARAMETER DESC

Descrive un parametro usato per un oggetto effetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nome del parametro.

</dd> <dt>

**Semantica**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Significato semantico, detto anche utilizzo.

</dd> <dt>

**Classe**
</dt> <dd>

Tipo: **[ **\_ classe D3DXPARAMETER**](./d3dxparameter-class.md)**

</dd> <dd>

Classe Parameter. Impostare questa impostazione su uno dei valori nella [**\_ classe D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DXPARAMETER \_**](./d3dxparameter-type.md)**

</dd> <dd>

Tipo di parametro. Impostare questa impostazione su uno dei valori di [**\_ tipo D3DXPARAMETER**](./d3dxparameter-type.md).

</dd> <dt>

**prime righe**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di righe nella matrice.

</dd> <dt>

**Colonne**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di colonne nella matrice.

</dd> <dt>

**Elementi**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di elementi nella matrice.

</dd> <dt>

**annotazioni**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di annotazioni.

</dd> <dt>

**StructMembers**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di membri della struttura.

</dd> <dt>

**Flag**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Attributi di parametro. Vedere [costanti di effetto](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

**Byte**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensioni, in byte, del parametro.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture degli effetti](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
