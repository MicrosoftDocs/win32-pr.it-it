---
description: Matrice di riga 4x4-principale.
ms.assetid: 2253f486-7bb6-4966-b3ec-dba47e53e372
title: Struttura D3DMATRIX (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 1df0d2171e828b14fba87f6587c604146360d0e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355489"
---
# <a name="d3dmatrix-structure"></a>Struttura D3DMATRIX

Matrice di riga 4x4-principale.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DMATRIX {
  float m[4][4];
} D3DMATRIX, *LPD3DMATRIX;
```



## <a name="members"></a>Members

<dl> <dt>

**m \[ 4 \] \[ 4\]**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Matrice della riga 4x4-Major.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 




