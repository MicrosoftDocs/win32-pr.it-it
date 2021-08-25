---
description: Descrive un passaggio per un oggetto effetto.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: D3DXPASS_DESC struttura (D3dx9effect.h)
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
ms.openlocfilehash: 9666f0385c592adbc4378cbc693a5ce7a628092bbbb1695fd39527817c7ca04e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894051"
---
# <a name="d3dxpass_desc-structure"></a>Struttura D3DXPASS \_ DESC

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

Valore stringa usato per il passaggio.

</dd> <dt>

**Annotazioni**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Le annotazioni sono dati specifici dell'utente che possono essere collegati a qualsiasi tecnica, passaggio o parametro. Vedere [Aggiungere informazioni ai parametri degli effetti con \_ annotazioni.](using-an-effect.md)

</dd> <dt>

**pVertexShaderFunction**
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Puntatore alla funzione vertex shader. Se viene creato un effetto [con D3DXFX \_ NOT \_ CLONEABLE,](d3dxfx.md)questa struttura restituirà un **puntatore NULL** quando viene chiamata da [**GetPassDesc.**](id3dxbaseeffect--getpassdesc.md)

</dd> <dt>

**pPixelShaderFunction**
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Puntatore alla pixel shader funzione. Se viene creato un effetto [con D3DXFX \_ NOT \_ CLONEABLE,](d3dxfx.md)questa struttura restituirà un **puntatore NULL** quando viene chiamata da [**GetPassDesc.**](id3dxbaseeffect--getpassdesc.md)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture degli effetti](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
