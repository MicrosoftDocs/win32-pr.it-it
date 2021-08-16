---
description: 'Struttura D3DXFLOAT16 (D3dx9math.h): descrive un vettore a virgola mobile a 16 bit.'
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: Struttura D3DXFLOAT16 (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: c6f1c204dfe674a2c2db995e158891ea03ca571b00c0fc4f49f4e52884042c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526065"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a>Struttura D3DXFLOAT16 (D3dx9math.h)

Descrive un vettore a virgola mobile a 16 bit.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a>Members

<dl> <dt>

**Valore**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dati a 16 bit.

</dd> </dl>

## <a name="remarks"></a>Commenti

I programmatori C++ possono sfruttare l'overload degli operatori e il cast dei tipi con le estensioni [**D3DXFLOAT16**](d3dxfloat16-extensions.md), che implementano costruttori di overload e operatori di assegnazione, unari e binari (inclusa l'uguaglianza).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
