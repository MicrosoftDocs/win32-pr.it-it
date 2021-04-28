---
description: 'Struttura D3DXPLANE (D3dx9math.h): descrive un piano.'
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: Struttura D3DXPLANE (D3dx9math.h)
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
ms.openlocfilehash: 3df0c94dbd49cf38d9230a2c5392df8497c64761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115719"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a>Struttura D3DXPLANE (D3dx9math.h)

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

I membri della struttura **D3DXPLANE** hanno la forma dell'equazione del piano generale. Rientrano nell'equazione del piano generale in **modo** che x + **b** y + **c** z + **d** w = 0.

I programmatori C++ possono sfruttare l'overload degli operatori e il cast dei tipi con le estensioni [**D3DXPLANE**](d3dxplane-extensions.md) che implementano costruttori di overload e operatori di assegnazione, unario e binario (inclusa l'uguaglianza).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
