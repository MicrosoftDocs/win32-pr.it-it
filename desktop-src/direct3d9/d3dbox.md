---
description: Definisce un volume.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: Struttura D3DBOX (D3D9Types. h)
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
ms.openlocfilehash: 882f6aadf0d49284b30132d4f08a9c583e5c9d73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234967"
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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione del lato sinistro della casella sull'asse x.

</dd> <dt>

**Top**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione della parte superiore della casella sull'asse y.

</dd> <dt>

**Ok**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione del lato destro della casella sull'asse x.

</dd> <dt>

**Ultimo**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione della parte inferiore della casella sull'asse y.

</dd> <dt>

**Front**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione della parte anteriore della casella sull'asse z.

</dd> <dt>

**Back**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione della parte posteriore della casella sull'asse z.

</dd> </dl>

## <a name="remarks"></a>Commenti

**D3DBOX** include i bordi sinistro, superiore e anteriore; Tuttavia, i bordi destro, inferiore e indietro non sono inclusi. Ad esempio, una casella di 100 unità di misura e inizia da 0 (quindi, inclusi i punti fino a 99) viene espressa con un valore pari a 0 per il membro sinistro e il valore 100 per il membro destro. Si noti che il valore 99 non viene utilizzato per il membro destro.

Le restrizioni sull'ordinamento laterale osservato per **D3DBOX** sono da sinistra a destra, dall'alto verso il basso e viceversa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
