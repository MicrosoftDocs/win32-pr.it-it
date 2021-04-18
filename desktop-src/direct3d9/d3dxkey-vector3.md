---
description: Descrive una chiave vettoriale da utilizzare nell'animazione con fotogramma chiave. Specifica un vettore in un determinato momento. Viene utilizzato per le chiavi di scala e di conversione.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: Struttura D3DXKEY_VECTOR3 (D3dx9anim. h)
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
ms.openlocfilehash: 41aec16da30a6e8742290b747b844b7fb22f6650
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322641"
---
# <a name="d3dxkey_vector3-structure"></a>\_Struttura D3DXKEY VECTOR3

Descrive una chiave vettoriale da utilizzare nell'animazione con fotogramma chiave. Specifica un vettore in un determinato momento. Viene utilizzato per le chiavi di scala e di conversione.

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

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Timestamp del fotogramma chiave.

</dd> <dt>

**Valore**
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)**

</dd> <dd>

Vettore 3D [**D3DXVECTOR3**](d3dxvector3.md) che fornisce valori di scala e/o di conversione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
