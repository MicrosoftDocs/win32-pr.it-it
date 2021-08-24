---
description: Descrive lo stato raster.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: D3DRASTER_STATUS struttura (D3D9Types.h)
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
ms.openlocfilehash: fc8a1e2995a9353a02df120b109eb32ad0914821e5690440c7228fbc8e7b6c8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676401"
---
# <a name="d3draster_status-structure"></a>Struttura D3DRASTER \_ STATUS

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

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

**TRUE** se il raster si trova nel punto vuoto verticale. **FALSE** se il raster non si trova nel punto vuoto verticale.

</dd> <dt>

**ScanLine**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Se InVBlank è **FALSE,** questo valore è un numero intero approssimativamente corrispondente alla linea di analisi corrente disegnata dal raster. Le linee di digitalizzazione sono numerate nello stesso modo delle coordinate della superficie Direct3D: 0 è la parte superiore della superficie primaria, che si estende fino al valore (altezza della superficie - 1) nella parte inferiore dello schermo.

Se InVBlank è **TRUE,** questo valore è impostato su zero e può essere ignorato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
