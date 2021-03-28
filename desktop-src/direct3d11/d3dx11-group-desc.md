---
title: Struttura D3DX11_GROUP_DESC (D3dx11effect. h)
description: Descrive un gruppo di effetti.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- Struttura D3DX11_GROUP_DESC Direct3D 11
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
ms.openlocfilehash: 431daf0a14a465ee3533f1497278ddcd85b08a79
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058690"
---
# <a name="d3dx11_group_desc-structure"></a>\_Struttura Desc del gruppo D3DX11 \_

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

Nome del gruppo ( **null** solo se globale).

</dd> <dt>

**Tecniche**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di tecniche contenute nel gruppo.

</dd> <dt>

**annotazioni**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di annotazioni in questo gruppo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il \_ gruppo D3DX11 \_ desc viene usato con [**ID3DX11EffectTechnique:: getdesc**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Effects 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

