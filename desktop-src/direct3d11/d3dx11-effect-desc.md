---
title: Struttura D3DX11_EFFECT_DESC (D3dx11effect. h)
description: Descrive un effetto.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- Struttura D3DX11_EFFECT_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d43b37d13a8b3f076cc3c5967dac9a95ed18a5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982587"
---
# <a name="d3dx11_effect_desc-structure"></a>D3DX11 \_ effetto \_ desc struttura

Descrive un effetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**ConstantBuffers**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di buffer costanti in questo effetto.

</dd> <dt>

**GlobalVariables**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di variabili globali in questo effetto.

</dd> <dt>

**InterfaceVariables**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di interfacce globali in questo effetto.

</dd> <dt>

**Tecniche**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di tecniche in questo effetto.

</dd> <dt>

**Gruppi**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di gruppi in questo effetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 \_ Effect \_ desc viene usato con [**ID3DX11Effect:: getdesc**](id3dx11effect-getdesc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Effects 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

