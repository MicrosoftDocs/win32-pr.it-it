---
description: Descrive un passaggio per un oggetto effetto.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: Struttura D3DXPASS_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a147f737057a5b2cff6ea436d9d2e47920a67a4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354149"
---
# <a name="d3dxpass_desc-structure"></a>\_Struttura D3DXPASS DESC

Descrive un passaggio per un oggetto effetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore stringa utilizzato per il passaggio.

</dd> <dt>

**annotazioni**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Le annotazioni sono dati specifici dell'utente che possono essere collegati a qualsiasi tecnica, passaggio o parametro. Vedere [aggiungere informazioni ai parametri di effetto con le \_ annotazioni](using-an-effect.md).

</dd> <dt>

**pVertexShaderFunction**
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Puntatore alla funzione vertex shader. Se viene creato un effetto con [D3DXFX \_ non \_ clonabile](d3dxfx.md), questa struttura restituirà un puntatore **null** quando viene chiamato da [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).

</dd> <dt>

**pPixelShaderFunction**
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Puntatore alla funzione pixel shader. Se viene creato un effetto con [D3DXFX \_ non \_ clonabile](d3dxfx.md), questa struttura restituirà un puntatore **null** quando viene chiamato da [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture degli effetti](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
