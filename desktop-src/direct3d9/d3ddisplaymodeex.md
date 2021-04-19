---
description: Informazioni sulle proprietà di una modalità di visualizzazione.
ms.assetid: df9d12b9-7acb-435b-9d54-0b095c871f0e
title: Struttura D3DDISPLAYMODEEX (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEEX
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5906b6b23cc83e6d2379f0c5923b08b220285708
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322394"
---
# <a name="d3ddisplaymodeex-structure"></a>Struttura D3DDISPLAYMODEEX

Informazioni sulle proprietà di una modalità di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  UINT                Size;
  UINT                Width;
  UINT                Height;
  UINT                RefreshRate;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEEX;
```



## <a name="members"></a>Members

<dl> <dt>

**Dimensioni**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensione della struttura. Questo deve essere sempre impostato su sizeof (D3DDISPLAYMODEEX).

</dd> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza della modalità di visualizzazione.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza della modalità di visualizzazione.

</dd> <dt>

**RefreshRate**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Frequenza di aggiornamento della modalità di visualizzazione.

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Formato della modalità di visualizzazione. Vedere [D3DFORMAT](d3dformat.md).

</dd> <dt>

**ScanLineOrdering**
</dt> <dd>

Tipo: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**

</dd> <dd>

Indica se l'ordine scanline è progressivo o interlacciato. Vedere [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata in vari metodi per creare e gestire i dispositivi Direct3D 9Ex ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) e le catene ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
