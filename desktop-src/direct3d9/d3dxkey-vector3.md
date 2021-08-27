---
description: Descrive una chiave vettoriale da usare nell'animazione con fotogrammi chiave. Specifica un vettore in un determinato momento. Viene usato per le chiavi di scala e traslazione.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: D3DXKEY_VECTOR3 struttura (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0214582b3fb1267caeb30a6cca905cbf7243ecf5dd1af40365841b315359317f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119181"
---
# <a name="d3dxkey_vector3-structure"></a>Struttura D3DXKEY \_ VECTOR3

Descrive una chiave vettoriale da usare nell'animazione con fotogrammi chiave. Specifica un vettore in un determinato momento. Viene usato per le chiavi di scala e traslazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a>Members

<dl> <dt>

**Time**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Timestamp del fotogramma chiave.

</dd> <dt>

**Valore**
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)**

</dd> <dd>

[**Vettore 3D D3DXVECTOR3**](d3dxvector3.md) che fornisce valori di scala e/o traslazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
