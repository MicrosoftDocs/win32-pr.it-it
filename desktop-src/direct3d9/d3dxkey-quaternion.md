---
description: Descrive una chiave Quaternion per l'uso nell'animazione con fotogramma chiave. Una chiave Quaternion è un valore quaternione in un determinato momento.
ms.assetid: 8f5b74a3-f712-40ac-942c-a2189c2327c8
title: Struttura D3DXKEY_QUATERNION (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_QUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12e4deead606c1a2c5b103ed9fd0e31e23515982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354809"
---
# <a name="d3dxkey_quaternion-structure"></a>\_Struttura QUATERNION D3DXKEY

Descrive una chiave Quaternion per l'uso nell'animazione con fotogramma chiave. Una chiave Quaternion è un valore quaternione in un determinato momento.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXKEY_QUATERNION {
  FLOAT          Time;
  D3DXQUATERNION Value;
} D3DXKEY_QUATERNION, *LPD3DXKEY_QUATERNION;
```



## <a name="members"></a>Members

<dl> <dt>

**Time**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore temporale.

</dd> <dt>

**Valore**
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)**

</dd> <dd>

Quaternione [**D3DXQUATERNION**](d3dxquaternion.md) che fornisce valori di rotazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
