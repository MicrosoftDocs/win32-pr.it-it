---
description: Specifica il rettangolo utilizzato per racchiudere i glifi su una superficie monocromatica.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: Struttura D3DCOMPOSERECTDESC (D3d9types.h)
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
ms.openlocfilehash: 8c23868e8759b98898013ea70d8d62768f1e648eb6e5019eb52dd21ba55905b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733204"
---
# <a name="d3dcomposerectdesc-structure"></a>Struttura D3DCOMPOSERECTDESC

Specifica il rettangolo utilizzato per racchiudere i glifi su una superficie monocromatica.

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

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata sinistra da cui iniziare la copia.

</dd> <dt>

**S**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata superiore da cui iniziare la copia.

</dd> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di texel dalla coordinata sinistra.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di texel dalla coordinata superiore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata nelle chiamate [**a ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) per racchiudere i glifi sulla superficie di origine. Un vertex buffer (vedere [**IDirect3DVertexBuffer9)**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)riempito con queste strutture viene creato per contenere le posizioni dei glifi. I membri USHORT vengono usati per ridurre il più possibile il footprint di memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
