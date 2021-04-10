---
description: Definisce un rettangolo.
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: Struttura D3DRECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9a22b74869afa16ca0c55ac50975eb36ba590c7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762100"
---
# <a name="d3drect-structure"></a>Struttura D3DRECT

Definisce un rettangolo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DRECT {
  LONG x1;
  LONG y1;
  LONG x2;
  LONG y2;
} D3DRECT;
```



## <a name="members"></a>Members

<dl> <dt>

**X1**
</dt> <dd>

Tipo: **[ **Long**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata x dell'angolo superiore sinistro del rettangolo.

</dd> <dt>

**Y1**
</dt> <dd>

Tipo: **[ **Long**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata y dell'angolo superiore sinistro del rettangolo.

</dd> <dt>

**X2**
</dt> <dd>

Tipo: **[ **Long**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata x dell'angolo inferiore destro del rettangolo.

</dd> <dt>

**Y2**
</dt> <dd>

Tipo: **[ **Long**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata y dell'angolo inferiore destro del rettangolo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Deselezionare**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
