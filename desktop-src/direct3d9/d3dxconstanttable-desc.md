---
description: Descrizione della tabella delle costanti.
ms.assetid: 848b328a-95a4-4fd0-a7d4-4fb0e5d14f64
title: Struttura D3DXCONSTANTTABLE_DESC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANTTABLE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7c53023952518182f68cf4a671ec47c6056a92a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762095"
---
# <a name="d3dxconstanttable_desc-structure"></a>\_Struttura D3DXCONSTANTTABLE DESC

Descrizione della tabella delle costanti.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXCONSTANTTABLE_DESC {
  LPCSTR Creator;
  DWORD  Version;
  UINT   Constants;
} D3DXCONSTANTTABLE_DESC, *LPD3DXCONSTANTTABLE_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Autore**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nome del creatore della tabella di costanti.

</dd> <dt>

**Versione**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Versione shader.

</dd> <dt>

**Costanti**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di costanti nella tabella delle costanti.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 
