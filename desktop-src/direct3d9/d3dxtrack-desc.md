---
description: Descrive una traccia di animazione e specifica il peso, la velocità e la posizione della traccia in un determinato momento.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: Struttura D3DXTRACK_DESC (D3dx9anim. h)
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
ms.openlocfilehash: 12f1604cf954bcdd6a2a898fec5410804112e498
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322574"
---
# <a name="d3dxtrack_desc-structure"></a>\_Struttura D3DXTRACK DESC

Descrive una traccia di animazione e specifica il peso, la velocità e la posizione della traccia in un determinato momento.

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

Tipo: **[ **D3DXPRIORITY \_**](./d3dxpriority-type.md)**

</dd> <dd>

Tipo di priorità, come definito [**nel \_ tipo D3DXPRIORITY**](./d3dxpriority-type.md).

</dd> <dt>

**Weight**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore del peso. Il peso determina la percentuale di questa traccia da unire con altre tracce.

</dd> <dt>

**Velocità**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore della velocità. Viene usato in modo analogo a un moltiplicatore per ridimensionare il periodo della traccia.

</dd> <dt>

**Position**
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione temporale della traccia nell'intervallo di tempo locale del set di animazioni corrente.

</dd> <dt>

**Attiva**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Tenere traccia dell'abilitazione o disabilitazione. Per abilitare, impostare su **true**. Per disabilitare, impostare su **false**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le tracce con la stessa priorità vengono combinate insieme e i due valori risultanti vengono combinati utilizzando il fattore di sfumatura della priorità. A una traccia deve essere associato un set di animazioni (archiviato separatamente).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
