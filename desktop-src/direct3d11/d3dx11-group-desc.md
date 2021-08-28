---
title: D3DX11_GROUP_DESC struttura (D3dx11effect.h)
description: Descrive un gruppo di effetti.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- D3DX11_GROUP_DESC struttura Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a189417b997647fd9c48a55010e96b32053c64031a03a8ac845e48c9a8e870a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096311"
---
# <a name="d3dx11_group_desc-structure"></a>Struttura DESC D3DX11 \_ GROUP \_

Descrive un gruppo di effetti.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nome del gruppo (solo **NULL se** globale).

</dd> <dt>

**Tecniche**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di tecniche contenute nel gruppo.

</dd> <dt>

**Annotazioni**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di annotazioni nel gruppo.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 GROUP DESC viene usato \_ con \_ [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Effetti 11 Strutture](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

