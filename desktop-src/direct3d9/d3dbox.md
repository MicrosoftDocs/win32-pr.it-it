---
description: Definisce un volume.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: Struttura D3DBOX (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9b7e01641348594e962f546a431700db799600a08571bbb7cfaf13396e671036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805514"
---
# <a name="d3dbox-structure"></a>Struttura D3DBOX

Definisce un volume.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a>Members

<dl> <dt>

**Sinistra**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione del lato sinistro della casella sull'asse x.

</dd> <dt>

**Top**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione della parte superiore della casella sull'asse y.

</dd> <dt>

**va bene**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione del lato destro della casella sull'asse x.

</dd> <dt>

**Ultimo**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione della parte inferiore della casella sull'asse y.

</dd> <dt>

**Front**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione della parte anteriore della casella sull'asse z.

</dd> <dt>

**Back**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione della parte posteriore della casella sull'asse z.

</dd> </dl>

## <a name="remarks"></a>Commenti

**D3DBOX** include i bordi sinistro, superiore e anteriore; Tuttavia, i bordi destro, inferiore e posteriore non sono inclusi. Ad esempio, una casella larga 100 unità e che inizia da 0 (inclusi i punti fino a e inclusi 99) viene espressa con un valore pari a 0 per il membro Left e un valore pari a 100 per il membro Right. Si noti che il valore 99 non viene usato per il membro Right.

Le restrizioni relative all'ordinamento laterale osservate per **D3DBOX** sono da sinistra a destra, dall'alto verso il basso e dalla parte anteriore alla parte posteriore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
