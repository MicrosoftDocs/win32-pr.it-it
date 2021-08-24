---
description: 'Struttura D3DXPLANE (D3DX10Math.h): descrive un piano.'
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: Struttura D3DXPLANE (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ccdc8644f63bdb048f6caa97ef635165a11a4473f549214410558583c8f807c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754261"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a>Struttura D3DXPLANE (D3DX10Math.h)

Descrive un piano.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a>Members

<dl> <dt>

**Un**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coefficiente del piano di ritaglio nell'equazione del piano generale. Vedere la sezione Osservazioni.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coefficiente b del piano di ritaglio nell'equazione del piano generale. Vedere la sezione Osservazioni.

</dd> <dt>

**c**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coefficiente c del piano di ritaglio nell'equazione del piano generale. Vedere la sezione Osservazioni.

</dd> <dt>

**d**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coefficiente d del piano di ritaglio nell'equazione del piano generale. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri della struttura **D3DXPLANE** hanno la forma dell'equazione del piano generale. Si adattano all'equazione del piano generale in modo che ax + by + cz + dw = 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
