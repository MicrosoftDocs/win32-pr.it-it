---
description: Specifica il glifo e la posizione di origine in una superficie monocromatica in cui copiare i glifi.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: Struttura D3DCOMPOSERECTDESTINATION (D3d9types. h)
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
ms.openlocfilehash: 56843bc78943a4c76fe4fe0f5e18242728a979c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322367"
---
# <a name="d3dcomposerectdestination-structure"></a>Struttura D3DCOMPOSERECTDESTINATION

Specifica il glifo e la posizione di origine in una superficie monocromatica in cui copiare i glifi.

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

Tipo: **[ **ushort**](../winprog/windows-data-types.md)**

</dd> <dd>

Indicizzare un glifo particolare dal buffer vertex contenente le strutture [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) .

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[ **ushort**](../winprog/windows-data-types.md)**

</dd> <dd>

Riservato a scopo di allineamento.

</dd> <dt>

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

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata nelle chiamate a [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) per indicare che i glifi del percorso devono essere copiati in e quale glifo particolare deve essere copiato. Un buffer dei vertici (vedere [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) riempito con queste strutture viene creato per contenere le posizioni dei glifi. I membri USHORT vengono usati per ridurre il più possibile il footprint di memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
