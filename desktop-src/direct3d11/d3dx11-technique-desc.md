---
title: Struttura D3DX11_TECHNIQUE_DESC (D3dx11effect. h)
description: Descrive una tecnica di effetto.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- Struttura D3DX11_TECHNIQUE_DESC Direct3D 11
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
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762179"
---
# <a name="d3dx11_technique_desc-structure"></a>\_Struttura D3DX11 Technique \_ DESC

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di passaggi contenuti nella tecnica.

</dd> <dt>

**annotazioni**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di annotazioni su questa tecnica.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 \_ Technique \_ desc viene usato con [**ID3DX11EffectTechnique:: getdesc**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Effects 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

