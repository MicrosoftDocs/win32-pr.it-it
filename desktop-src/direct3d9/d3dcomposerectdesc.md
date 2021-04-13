---
description: Specifica il rettangolo utilizzato per racchiudere i glifi in una superficie monocromatica.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: Struttura D3DCOMPOSERECTDESC (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cf9ad5f1c075f4dc52d68b894b37c7d0f0a7b310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401938"
---
# <a name="d3dcomposerectdesc-structure"></a>Struttura D3DCOMPOSERECTDESC

Specifica il rettangolo utilizzato per racchiudere i glifi in una superficie monocromatica.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a>Members

<dl> <dt>

**X**
</dt> <dd>

Tipo: **[ **ushort**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata sinistra in cui iniziare la copia.

</dd> <dt>

**S**
</dt> <dd>

Tipo: **[ **ushort**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata superiore per iniziare la copia in.

</dd> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **ushort**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di Texel dalla coordinata sinistra.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **ushort**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di Texel dalla coordinata superiore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata nelle chiamate a [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) per racchiudere i glifi nell'area di origine. Un buffer dei vertici (vedere [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) riempito con queste strutture viene creato per contenere le posizioni dei glifi. I membri USHORT vengono usati per ridurre il più possibile il footprint di memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
