---
description: Specifica i tipi di modalità di visualizzazione da filtrare.
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: Struttura D3DDISPLAYMODEFILTER (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b60c283405bead7b2618b91d6de76158841ff27f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354464"
---
# <a name="d3ddisplaymodefilter-structure"></a>Struttura D3DDISPLAYMODEFILTER

Specifica i tipi di modalità di visualizzazione da filtrare.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a>Members

<dl> <dt>

**Dimensioni**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensione della struttura. Questo deve essere sempre impostato su sizeof (D3DDISPLAYMODEFILTER).

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Formato della modalità di visualizzazione da filtrare. Vedere [D3DFORMAT](d3dformat.md).

</dd> <dt>

**ScanLineOrdering**
</dt> <dd>

Tipo: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**

</dd> <dd>

Indica se l'ordinamento scanline è interlacciato o progressivo. Vedere [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
