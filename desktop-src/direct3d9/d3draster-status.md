---
description: Descrive lo stato raster.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: Struttura D3DRASTER_STATUS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e77ab0e6ee164eadae862ed03df5652c21ba7040
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322916"
---
# <a name="d3draster_status-structure"></a>\_Struttura di stato D3DRASTER

Descrive lo stato raster.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a>Members

<dl> <dt>

**InVBlank**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

**True** se il raster è nel periodo vuoto verticale. **False** se il raster non è nel periodo di blanking verticale.

</dd> <dt>

**ScanLine**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Se InVBlank è **false**, questo valore è un Integer approssimativamente corrispondente alla riga di analisi corrente disegnata dal raster. Le righe di analisi sono numerate nello stesso modo delle coordinate di superficie Direct3D: 0 è la parte superiore della superficie primaria, estendendo al valore (altezza della superficie-1) nella parte inferiore dello schermo.

Se InVBlank è **true**, questo valore è impostato su zero e può essere ignorato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
