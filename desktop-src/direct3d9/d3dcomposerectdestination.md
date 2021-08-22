---
description: Specifica il glifo di origine e la posizione in una superficie monocromatica in cui copiare i glifi.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: Struttura D3DCOMPOSERECTDESTINATION (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e6d859cb0bfd47c9be21f37feef287b38cdce4cc64360dd312b2b52bb825a23e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123311"
---
# <a name="d3dcomposerectdestination-structure"></a>Struttura D3DCOMPOSERECTDESTINATION

Specifica il glifo di origine e la posizione in una superficie monocromatica in cui copiare i glifi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a>Members

<dl> <dt>

**SrcRectIndex**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Indicizzare un particolare glifo dal vertex buffer [**contenente strutture D3DCOMPOSERECTDESC.**](d3dcomposerectdesc.md)

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Riservato ai fini dell'allineamento.

</dd> <dt>

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

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata nelle chiamate a [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) per indicare la posizione in cui copiare i glifi e in quale particolare glifo deve essere copiato. Un vertex buffer (vedere [**IDirect3DVertexBuffer9)**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)riempito con queste strutture viene creato per contenere le posizioni dei glifi. I membri USHORT vengono usati per ridurre il più possibile il footprint di memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
