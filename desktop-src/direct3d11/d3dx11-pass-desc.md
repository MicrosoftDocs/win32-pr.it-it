---
title: Struttura D3DX11_PASS_DESC (D3dx11effect. h)
description: Descrive un passaggio di effetto, che contiene lo stato della pipeline.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- Struttura D3DX11_PASS_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4d7f10268db0515b2f7e3772332b34427ba67a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982550"
---
# <a name="d3dx11_pass_desc-structure"></a>D3DX11 \_ pass \_ desc-struttura

Descrive un passaggio di effetto, che contiene lo stato della pipeline.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nome del passaggio (**null** se non anonimo).

</dd> <dt>

**annotazioni**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di annotazioni in questo passaggio.

</dd> <dt>

**pIAInputSignature**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)\***

</dd> <dd>

Firma da vertex shader o geometry shader (se non è presente alcun vertex shader) o **null** se non esiste alcun vertex shader.

</dd> <dt>

**IAInputSignatureSize**
</dt> <dd>

Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Dimensioni singature in byte.

</dd> <dt>

**StencilRef**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Il valore di riferimento stencil usato nello stato di stencil Depth.

</dd> <dt>

**SampleMask**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Maschera di esempio per lo stato di Blend.

</dd> <dt>

**BlendFactor**
</dt> <dd>

Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Fattori di Blend per componente (RGBA) per lo stato di Blend.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 \_ pass \_ desc viene usato con [**ID3DX11EffectPass:: getdesc**](id3dx11effectpass-getdesc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Effects 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

