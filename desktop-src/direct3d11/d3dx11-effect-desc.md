---
title: D3DX11_EFFECT_DESC struttura (D3dx11effect.h)
description: Descrive un effetto.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- D3DX11_EFFECT_DESC struttura Direct3D 11
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
ms.openlocfilehash: d3f2c3a205a4849aed755bee01302da813cccf77bbf8255036f287d488b76591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989991"
---
# <a name="d3dx11_effect_desc-structure"></a>Struttura DESC D3DX11 \_ EFFECT \_

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

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di buffer costanti in questo effetto.

</dd> <dt>

**Variabili globali**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di variabili globali in questo effetto.

</dd> <dt>

**InterfaceVariables**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di interfacce globali in questo effetto.

</dd> <dt>

**Tecniche**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di tecniche in questo effetto.

</dd> <dt>

**Gruppi**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di gruppi in questo effetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 \_ EFFECT \_ DESC viene usato con [**ID3DX11Effect::GetDesc**](id3dx11effect-getdesc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Effetti 11 Strutture](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

