---
title: D3DX11_PASS_DESC struttura (D3dx11effect.h)
description: Descrive un passaggio dell'effetto, che contiene lo stato della pipeline.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- D3DX11_PASS_DESC struttura Direct3D 11
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
ms.openlocfilehash: 6f00cc28e6ab901073e30abd2554046d61144c42af2217869c0b87dc6c19d29d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124946"
---
# <a name="d3dx11_pass_desc-structure"></a>Struttura D3DX11 \_ PASS \_ DESC

Descrive un passaggio dell'effetto, che contiene lo stato della pipeline.

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

Nome di questo passaggio (**NULL** se non anonimo).

</dd> <dt>

**Annotazioni**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di annotazioni in questo passaggio.

</dd> <dt>

**pIAInputSignature**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)\***

</dd> <dd>

Firma dal vertex shader o geometry shader (se non è presente alcun vertex shader) o **NULL** se non esiste.

</dd> <dt>

**IAInputSignatureSize**
</dt> <dd>

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Dimensioni della singature in byte.

</dd> <dt>

**StencilRef**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore di riferimento dello stencil utilizzato nello stato depth-stencil.

</dd> <dt>

**SampleMask**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Maschera di esempio per lo stato di fusione.

</dd> <dt>

**BlendFactor**
</dt> <dd>

Tipo: **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Fattori di blend per componente (RGBA) per lo stato di blend.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 \_ PASS \_ DESC viene usato con [**ID3DX11EffectPass::GetDesc**](id3dx11effectpass-getdesc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Effetti 11 Strutture](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

