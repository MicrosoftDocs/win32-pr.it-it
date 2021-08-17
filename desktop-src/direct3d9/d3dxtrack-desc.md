---
description: Descrive una traccia di animazione e specifica il peso, la velocità e la posizione di fusione per la traccia in un determinato momento.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: D3DXTRACK_DESC struttura (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: cddabb3ea79951e35831c2cdc32e11baeb5c7c1c4ce174fd29d9382edb391953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731118"
---
# <a name="d3dxtrack_desc-structure"></a>Struttura D3DXTRACK \_ DESC

Descrive una traccia di animazione e specifica il peso, la velocità e la posizione di fusione per la traccia in un determinato momento.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Priorità**
</dt> <dd>

Tipo: **[ **D3DXPRIORITY \_ TYPE**](./d3dxpriority-type.md)**

</dd> <dd>

Tipo di priorità, come definito in [**D3DXPRIORITY \_ TYPE**](./d3dxpriority-type.md).

</dd> <dt>

**Weight**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore del peso. Il peso determina la proporzione di questa traccia da unire ad altre tracce.

</dd> <dt>

**Velocità**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore della velocità. Viene usato in modo analogo a un moltiplicatore per ridimensionare il periodo della traccia.

</dd> <dt>

**Position**
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione temporale della traccia, nell'intervallo di tempo locale del set di animazioni corrente.

</dd> <dt>

**Abilita**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Tenere traccia dell'abilitazione/disabilitazione. Per abilitarla, impostare su **TRUE.** Per disabilitare, impostare su **FALSE.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Le tracce con la stessa priorità vengono combinate tra loro e i due valori risultanti vengono quindi sfusi usando il fattore di blend di priorità. A una traccia deve essere associato un set di animazioni (archiviato separatamente).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
