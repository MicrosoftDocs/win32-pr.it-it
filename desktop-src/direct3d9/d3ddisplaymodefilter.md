---
description: Specifica i tipi di modalità di visualizzazione da filtrare.
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: Struttura D3DDISPLAYMODEFILTER (D3d9types.h)
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
ms.openlocfilehash: f59e2e095f7f0f1c6ee73fc940733e932efaef9af7ec05807ff1b38f35fe5189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751061"
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

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensione della struttura. Deve essere sempre impostato su sizeof(D3DDISPLAYMODEFILTER).

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Formato della modalità di visualizzazione da filtrare. Vedere [D3DFORMAT.](d3dformat.md)

</dd> <dt>

**ScanLineOrdering**
</dt> <dd>

Tipo: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**

</dd> <dd>

Indica se l'ordinamento della linea di analisi è interlacciato o progressivo. Vedere [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
