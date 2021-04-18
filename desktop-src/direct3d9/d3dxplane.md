---
description: Descrive un piano.
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: Struttura D3DXPLANE (D3dx9math. h)
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
- d3dx9math.h
ms.openlocfilehash: 260f9555313aea3443f0728f2b50189228429803
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322109"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a>Struttura D3DXPLANE (D3dx9math. h)

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

**un**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Il coefficiente del piano di ritaglio nell'equazione del piano generale. Vedere la sezione Osservazioni.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coefficiente b del piano di ritaglio nell'equazione del piano generale. Vedere la sezione Osservazioni.

</dd> <dt>

**c**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coefficiente c del piano di ritaglio nell'equazione del piano generale. Vedere la sezione Osservazioni.

</dd> <dt>

**d**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coefficiente d del piano di ritaglio nell'equazione del piano generale. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri della struttura **D3DXPLANE** prendono il formato dell'equazione generale del piano. Si adattano all'equazione del piano generale, in modo che **un** x + **b** y + **c** z + **d** w = 0.

I programmatori C++ possono sfruttare l'overload degli operatori e il cast dei tipi con le [**estensioni D3DXPLANE**](d3dxplane-extensions.md) che implementano costruttori di overload e operatori di assegnazione, unario e binari (inclusi uguaglianza).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
