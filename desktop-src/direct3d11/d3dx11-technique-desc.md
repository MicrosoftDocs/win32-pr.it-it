---
title: D3DX11_TECHNIQUE_DESC struttura (D3dx11effect.h)
description: Descrive una tecnica di effetto.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- D3DX11_TECHNIQUE_DESC struttura Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2266737a04b28940eeaa3758f5bd3909ec815745cb060836c499cfd4b3142266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124926"
---
# <a name="d3dx11_technique_desc-structure"></a>Struttura DESC D3DX11 \_ TECHNIQUE \_

Descrive una tecnica di effetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nome di questa tecnica (NULL se non anonimo).

</dd> <dt>

**Passa**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di passaggi contenuti nella tecnica.

</dd> <dt>

**Annotazioni**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di annotazioni su questa tecnica.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 \_ TECHNIQUE \_ DESC viene usato con [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Effetti 11 Strutture](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

